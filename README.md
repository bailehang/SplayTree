# SplayTree
Simple implementation of Splay tree. All functions has similar calling as STL map functions.

## Details
This implementation was made for educational purposes. Basic testing was made on this library. If you find a bug please report it and I will try to fix it.

## Features
- C++11 components
- forward iterator and const_iterator
- STL like function calls
- templated

## Missing features
- better allocation of the tree nodes - more cash sensitive

## Comparison to std::map test
Test was carried out by this simple metrics.
1. Program generates both trees in sizes 10, 10^2, 10^3, 10^4, 10^5, 10^6 elements
2. For each size is selected range of reading. Range is slowly increasing in powers of 2 (reason: not too fast rising, HW is aligning to the powers of 2).
3. For each range  is done 10 ^ 6 reedings from this range. Small repetions like 1024 cause that trees are both in the cash and results are unconsisten and undeterministic. Results depend on the fact wheather range stays in the cash or not.

## Range was selected from the minimum in the tree and increasing to the maximum


init of splaytree: elements: 10 time: 0
init of r-b tree: elements: 10 time: 0
SplayTree is faster than RB: range: 2 splay_time: 2296 RB_time: 4140
SplayTree is faster than RB: range: 4 splay_time: 3437 RB_time: 4203
SplayTree is faster than RB: range: 8 splay_time: 2343 RB_time: 4218
init of splaytree: elements: 100 time: 0
init of r-b tree: elements: 100 time: 0
SplayTree is faster than RB: range: 2 splay_time: 2203 RB_time: 5187
SplayTree is faster than RB: range: 4 splay_time: 3296 RB_time: 5171
SplayTree is faster than RB: range: 8 splay_time: 4718 RB_time: 5125
RB is faster than SplayTree: range: 16 splay_time: 6390 RB_time: 5109
init of splaytree: elements: 1000 time: 0
init of r-b tree: elements: 1000 time: 15
SplayTree is faster than RB: range: 2 splay_time: 2203 RB_time: 6312
SplayTree is faster than RB: range: 4 splay_time: 3296 RB_time: 6359
SplayTree is faster than RB: range: 8 splay_time: 4718 RB_time: 6406
RB is faster than SplayTree: range: 16 splay_time: 6421 RB_time: 6312
init of splaytree: elements: 10000 time: 15
init of r-b tree: elements: 10000 time: 125
SplayTree is faster than RB: range: 2 splay_time: 2250 RB_time: 7531
SplayTree is faster than RB: range: 4 splay_time: 3312 RB_time: 7484
SplayTree is faster than RB: range: 8 splay_time: 4734 RB_time: 7531
SplayTree is faster than RB: range: 16 splay_time: 6359 RB_time: 7562
RB is faster than SplayTree: range: 32 splay_time: 8156 RB_time: 7609
init of splaytree: elements: 100000 time: 218
init of r-b tree: elements: 100000 time: 1578
SplayTree is faster than RB: range: 2 splay_time: 2312 RB_time: 8453
SplayTree is faster than RB: range: 4 splay_time: 3328 RB_time: 8531
SplayTree is faster than RB: range: 8 splay_time: 5046 RB_time: 8484
SplayTree is faster than RB: range: 16 splay_time: 6390 RB_time: 8453
SplayTree is faster than RB: range: 32 splay_time: 8156 RB_time: 8500
RB is faster than SplayTree: range: 64 splay_time: 10031 RB_time: 8500
init of splaytree: elements: 1000000 time: 2156
init of r-b tree: elements: 1000000 time: 17890
SplayTree is faster than RB: range: 2 splay_time: 3359 RB_time: 9421
SplayTree is faster than RB: range: 4 splay_time: 3406 RB_time: 9453
SplayTree is faster than RB: range: 8 splay_time: 4781 RB_time: 9421
SplayTree is faster than RB: range: 16 splay_time: 6421 RB_time: 9468
SplayTree is faster than RB: range: 32 splay_time: 8187 RB_time: 9562
RB is faster than SplayTree: range: 64 splay_time: 10031 RB_time: 9468



## Range has started at the root of the tree and increasing to both sides 


init of splaytree: elements: 10 time: 0
init of r-b tree: elements: 10 time: 0
SplayTree is faster than RB: range: 2 splay_time: 14500 RB_time: 40172
SplayTree is faster than RB: range: 4 splay_time: 22894 RB_time: 41133
SplayTree is faster than RB: range: 8 splay_time: 33359 RB_time: 41109
init of splaytree: elements: 100 time: 0
init of r-b tree: elements: 100 time: 0
SplayTree is faster than RB: range: 2 splay_time: 14281 RB_time: 53201
SplayTree is faster than RB: range: 4 splay_time: 23092 RB_time: 51641
SplayTree is faster than RB: range: 8 splay_time: 33484 RB_time: 52146
SplayTree is faster than RB: range: 16 splay_time: 47610 RB_time: 52798
RB is faster than SplayTree: range: 32 splay_time: 64641 RB_time: 51031
init of splaytree: elements: 1000 time: 0
init of r-b tree: elements: 1000 time: 15
SplayTree is faster than RB: range: 2 splay_time: 14062 RB_time: 65266
SplayTree is faster than RB: range: 4 splay_time: 21812 RB_time: 64297
SplayTree is faster than RB: range: 8 splay_time: 32781 RB_time: 63032
SplayTree is faster than RB: range: 16 splay_time: 50126 RB_time: 63668
RB is faster than SplayTree: range: 32 splay_time: 64744 RB_time: 63413
init of splaytree: elements: 10000 time: 31
init of r-b tree: elements: 10000 time: 140
SplayTree is faster than RB: range: 2 splay_time: 14062 RB_time: 76294
SplayTree is faster than RB: range: 4 splay_time: 22453 RB_time: 74500
SplayTree is faster than RB: range: 8 splay_time: 32625 RB_time: 74547
SplayTree is faster than RB: range: 16 splay_time: 46563 RB_time: 74438
SplayTree is faster than RB: range: 32 splay_time: 62953 RB_time: 75219
RB is faster than SplayTree: range: 64 splay_time: 80704 RB_time: 75063
init of splaytree: elements: 100000 time: 218
init of r-b tree: elements: 100000 time: 1515
SplayTree is faster than RB: range: 2 splay_time: 14109 RB_time: 83657
SplayTree is faster than RB: range: 4 splay_time: 21797 RB_time: 83563
SplayTree is faster than RB: range: 8 splay_time: 32656 RB_time: 83454
SplayTree is faster than RB: range: 16 splay_time: 46781 RB_time: 83563
SplayTree is faster than RB: range: 32 splay_time: 62688 RB_time: 83235
SplayTree is faster than RB: range: 64 splay_time: 81190 RB_time: 83891
RB is faster than SplayTree: range: 128 splay_time: 99235 RB_time: 83813
init of splaytree: elements: 1000000 time: 2078
init of r-b tree: elements: 1000000 time: 17687
SplayTree is faster than RB: range: 2 splay_time: 15031 RB_time: 93469
SplayTree is faster than RB: range: 4 splay_time: 22000 RB_time: 93407
SplayTree is faster than RB: range: 8 splay_time: 32812 RB_time: 93954
SplayTree is faster than RB: range: 16 splay_time: 46751 RB_time: 92289
SplayTree is faster than RB: range: 32 splay_time: 61984 RB_time: 92794
SplayTree is faster than RB: range: 64 splay_time: 79657 RB_time: 92547
RB is faster than SplayTree: range: 128 splay_time: 98395 RB_time: 94311

## Conclusion
This implementation of the Splay tree in convinient when you need to do many reading on the small range. Range depends on the size of the tree.  