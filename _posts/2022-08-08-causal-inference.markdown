---
layout: post
title:  "List of resources for learning causal inference"
author: yduan
date:   2022-08-08 00:00:00 +0200
categories: machine_learning
tags: Machine learning
---
Causal inference is a statistical method that aims at determining the causal effect of a factor on an outcome. While common statistical tools (e.g. regression) describe the *correlative* relationship between variables, causal inference goes beyond correlation and tries to estimate the *causal* influence of one variable on the other. What *causal* actually means could be a difficult philosophy question, but we can simply say that variable A (called an 'interference') has a causal effect on variable B (called an 'outcome') if B would be different without A. *Counterfactual* is thus a useful way to think about causal effects. Nowadays, data scientists may need causal inference to answer questions about the influence of an interference variable from observational data, if an A/B test of that interference is not available or too expensive.

A famous example that illustrates the drawbacks of only looking at correlational relationships between variables in data is the [Simpson's paradox][simpson_url]. Since confounding factors widely exist in observational data, misinterpretations based on correlation are very likely. It may not be a problem if the task is not to interpret, and the task of prediction may actually benefit from correlative features as long as the data and the model can generalize. But if interpretation is what one really concerns, then they should look for the causal effect of the interference on the outcome. Whenever possible, an A/B test should be carried out and conclusions should be based on these experimental data, as this approach provides a gold standard of the interference's effect. If an A/B test is not possible, such as studying the influence of a state-wise policy, or studying some economic phenomena, then causal inference should be adopted instead of other commonly-used statistical tools. Even so, one should always be cautious when they draw causal interpretations from observational data, as prerequisites of a causal inference method may or may not be satisfied.

Here is a list for beginners who may want to use causal inference in their work:

* I highly recommend one starts with this [series of blog posts][ms_causal], as these posts are very beginner-friendly and give an overview of causal inference.

* For a high-level understanding of causal inference, I recommend *[The Book of Why][the_book_of_why]* by Judea Pearl. You may also check out the author's page for more books/tutorials on related topics.

* There are many powerful Python and R packages. Here are my picks:
    * [CausalML][causalml], a Python package from Uber. Easy to use, with many causal inference methods.
    * [EconML][econml] and [DoWhy][dowhy], two Python packages from Microsoft. Great documentation and theoretical explanations.
    * [grf][grfr], an R package that implements a tree-based algorithm called 'causal forest'. See these papers for more details ([paper1][athey2016],[paper2][wager2018]).

* The above-mentioned packages provide good tutorials and examples. In addition, this [page][kdd2021] lists several industrial use cases with slides and code as presented in KDD 2021. This [page][metalearners] shows a detailed example of running meta-learners using CausalML.

* Some resources in Chinese:
    * This [blog][ylblog] for introduction to causal inference, especially propensity score matching.
    * This [series of notes][zhihu_ladder] for a glimpse of *The Book of Why* and more illustrations of the theory.
    * This [talk][b_talk] for a general introduction to causal inference.

[simpson_url]: https://en.wikipedia.org/wiki/Simpson%27s_paradox
[ms_causal]: https://medium.com/data-science-at-microsoft/causal-inference-part-1-of-3-understanding-the-fundamentals-816f4723e54a
[the_book_of_why]: http://bayes.cs.ucla.edu/WHY/
[causalml]: https://github.com/uber/causalml
[econml]: https://github.com/microsoft/EconML
[dowhy]: https://github.com/py-why/dowhy
[grfr]: https://grf-labs.github.io/grf/
[athey2016]: https://www.pnas.org/doi/abs/10.1073/pnas.1510489113
[wager2018]: https://arxiv.org/pdf/1510.04342.pdf
[kdd2021]: https://causal-machine-learning.github.io/kdd2021-tutorial/
[metalearners]: https://chowdera.com/2021/10/20211025135953201q.html
[ylblog]: https://dango.rocks/blog/
[zhihu_ladder]: https://www.zhihu.com/column/c_1217887302124773376
[b_talk]: https://www.bilibili.com/video/BV1A3411k7tD