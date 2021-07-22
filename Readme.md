# Delaunay Triangulation Dataset for Pointer Networks

Made by Jibum Kim (jibumkim@inu.ac.kr), Woojin Choi (john1920@inu.ac.kr), and Jaeseung Lee (hunni10@inu.ac.kr) for [our paper](https://arxiv.org/abs/2107.01759) experiment

## Data Structure

Our dataset contains 1M training samples of a Delaunay triangulation. It follows the same format as [Vinyal’s “Pointer Network” dataset](http://goo.gl/NDcOIG)

Input: 2D Cartesian coordinates of the points (x, y)

Output: sequences representing the Delaunay triangulation of the input

For example,


    0.91628828 0.94290589 0.80433114 0.65371073 0.98110507 0.91290117 0.42115179 0.24321800 0.59974391 0.89575023 output 2 4 5 1 2 5 1 2 3

In this example, the inputs are planar point sets {P1,…, P5}. The first point, P1=(0.91628828, 0.94290589), second point, P2=(0.80433114, 0.65371073),…, P5=(0.59974391 0.89575023). The output, (2, 4, 5), (1, 2, 5), (1, 2, 3), is a sequence that represents the Delaunay triangulation of its input. It has three triangles and these three triangles form the Delaunay triangulation. Here, (2, 4, 5) means P2, P4, and P5 forms a triangle. 

* `delaunay_(n)_(ordering_type).txt` contain `n` points in one sample.
  * `delaunay_(n)_random.txt` are used for experiment of random ordering.
  * `delaunay_(n)_sorted.txt` are used for experiment of our proposed ordering.
* Every file has 1M lines (1M sample).
* Input points are chosen randomly in \[0\~1\] X \[0\~1\].

## Citation
If you use our dataset in your research, please consider citing

    @misc{lee2021learning,
         title={Learning Delaunay Triangulation using Self-attention and Domain Knowledge}, 
         author={Jaeseung Lee and Woojin Choi and Jibum Kim},
         year={2021},
         eprint={2107.01759},
         archivePrefix={arXiv},
         primaryClass={cs.CG}
    }
