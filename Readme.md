# Dataset for Training Delaunay Triangulation and TSP


### Brief Description of Our Dataset

Our dataset contains 1M training samples of a Delaunay Triangulation (DT) and Traveling Salesman Problem (TSP). DT Dataset follows the same format as [Vinyal’s “Pointer Network” dataset](http://goo.gl/NDcOIG). This dataset is used for training and evaluation of the proposed neural network model (https://arxiv.org/abs/2107.01759).

#### DT Dataset Description

Input: 2D Cartesian coordinates of the points (x, y)

Output: sequences representing the Delaunay triangulation of the input

For example,


    0.91628828 0.94290589 0.80433114 0.65371073 0.98110507 0.91290117 0.42115179 0.24321800 0.59974391 0.89575023 output 2 4 5 1 2 5 1 2 3

In this example, the inputs are planar point sets {P1,…, P5}. The first point, P1=(0.91628828, 0.94290589), second point, P2=(0.80433114, 0.65371073),…, P5=(0.59974391, 0.89575023). The output, (2, 4, 5), (1, 2, 5), (1, 2, 3), is a sequence that represents the Delaunay triangulation of its input. It has three triangles and these three triangles form the Delaunay triangulation. Here, (2, 4, 5) means P2, P4, and P5 forms a triangle. 

* `delaunay_(n)_(ordering_type).txt` contain `n` points in one sample.
  * `delaunay_(n)_random.txt` are used for experiment of random ordering.
  * `delaunay_(n)_sorted.txt` are used for experiment of our proposed ordering.
* Every file has 1M lines (1M sample).
* Input points are chosen randomly in \[0\~1\] X \[0\~1\].

#### TSP Dataset Description

Input: 2D Cartesian coordinates of the points (x, y). These mean cities in TSP.

Output: sequence of city that represents TSP Tour (acquired from [Christofides’ algorithm](https://github.com/beckysag/traveling-salesman)).

For example,

    0.36377419 0.59624464 0.37839254 0.18816579 0.44284963 0.29181516 0.59764034 0.81147296 0.95521193 0.94703185 output 1 2 3 5 4 

In this example, the inputs are planar point sets {P1,…, P5}. The first point, P1=(0.36377419, 0.59624464), second point, P2=(0.37839254, 0.18816579),…, P5=(0.95521193, 0.94703185). The output, (1, 2, 3, 5, 4), is a sequence that represents the TSP Tour of its input. Note that it suppose traveler to go back at last city to first city.

* Output sequences are obtained from [Christofides’ algorithm](https://github.com/beckysag/traveling-salesman)
* `tsp_50_random.txt` are used for experiment of random ordering.
* `tsp_50_sorted.txt` are used for experiment of our proposed ordering.
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
## Contact
If you have any questions regarding this dataset, please contact to Jibum Kim (jibumkim@inu.ac.kr) or Jaeseung Lee (hunni10@inu.ac.kr).
