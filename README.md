# Sequential-Pattern-Mining-AprioriAll

Given a input DB, mining sequential Pattern from the input DB with user-defined min_supp.
[Click to read the code](https://github.com/podo47/Sequential-Pattern-Mining-AprioriAll/blob/main/Sequential_Pattern_Mining_Algorithm.ipynb)

## Input DB : [Input](https://github.com/podo47/Sequential-Pattern-Mining-AprioriAll/blob/main/seqdata.dat.txt)
- [x] The first number of each sequence is the sequence ID
- [x] The pair of number such as 11 166 is the transaction time and the item ID. Transaction time just shows the order of transactions.
- [x] The first sequence can be transfer to the following format
  
  ◦ (166 4103 8715) (4103 8715)(166 3704 6568 8375 8715)(166 9406)
  

## 1.Import library
``` python
from itertools import combinations
import csv
from collections import Counter
import pandas as pd
```

## 2.Run AprioriAll Algorithm

**Part 1 : Function**
- [x] Calculate support
- [x] Litemset Phase
- [x] Transformation Phase
- [x] Maximal phase
- [x] Answer form - here you can change the location of output file
- [x] Main : Apriori algorithm

**Part 2 : AprioriAll  Algorithm**
* Input file preprocessing
  * Read input : [Input](https://github.com/podo47/Sequential-Pattern-Mining-AprioriAll/blob/main/seqdata.dat.txt)
  
  
  ``` python
  path = 'filename.txt'
  ```

  * Modify input format and store in list
  
* Output 
``` python
test = Sequential() # Please enter min support
```
## 3. Output:"output.csv"

Example : [Output](https://github.com/podo47/Sequential-Pattern-Mining-AprioriAll/blob/main/output.csv)
* min support : 0.01

| pattern                                                                                  | → | Support |
|------------------------------------------------------------------------------------------|---|---------|
| "({3488}, {1566}, {3488, 1566})"                                                         | → | 326     |
| "({5447}, {5493}, {5493, 5447})"                                                         | → | 406     |
| "({7160}, {6549}, {7160, 6549})"                                                         | → | 240     |
| "({552}, {4811}, {552, 4811})"                                                           | → | 348     |
| "({7125}, {2240, 7125}, {2240})"                                                         | → | 318     |
| "({8208, 7775}, {7775}, {8208})"                                                         | → | 255     |
| "({1946, 4683}, {1946}, {4683})"                                                         | → | 262     |
| "({8969, 2652}, {8969}, {2652})"                                                         | → | 349     |
| "({2722, 1503}, {2722}, {1503})"                                                         | → | 264     |
| "({6312, 1807}, {6312}, {1807})"                                                         | → | 297     |
| "({7088, 9126}, {7088}, {9126})"                                                         | → | 566     |
| "({3308}, {5343}, {3308, 5343}, {7931, 5343}, {7931, 3308}, {7931, 3308, 5343}, {7931})" | → | 249     |



## 3. Reference
[1] 序列模式挖掘-AprioriAll算法详解(附python源码)

https://www.tanglei.name/blog/aprioriall-algorithm-in-python.html

