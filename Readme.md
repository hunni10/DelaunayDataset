# Delaunay Triangulation Dataset for Pointer Networks

Made by Jibum Kim (jibumkim@inu.ac.kr), Woojin Choi (john1920@inu.ac.kr), and Jaeseung Lee (hunni10@inu.ac.kr) for [our paper](https://arxiv.org/abs/2107.01759) experiment



These dataset follow the format of [dataset of Vinyals et al.](http://goo.gl/NDcOIG), like

    0.91628828 0.94290589 0.80433114 0.65371073 0.98110507 0.91290117 0.42115179 0.24321800 0.59974391 0.89575023 output 2 4 5 1 2 5 1 2 3
It means that first point is `(0.91628828, 0.94290589)`, second point is `(0.80433114, 0.65371073)`, and so on, and expected output (label) sequence is `2 4 5 1 2 5 1 2 3`.


* `delaunay_(n)_(ordering_type).txt` contain `n` points in one sample.
  * `delaunay_(n)_random.txt` are used for experiment of random ordering
  * `delaunay_(n)_sorted.txt` are used for experiment of proposed ordering
* Every file has 1M lines (1M sample).
* Input points are chosen randomly in \[0\~1\] X \[0\~1\].
