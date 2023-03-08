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

## 2.Run Apriori Algorithm

**Part 1 : Function**
- [x] Calculate support
- [x] Calculate confidence
- [x] Answer form - here you can change the location of output file
- [x] Main : Apriori algorithm

**Part 2 : Apriori Algorithm**
* Input file preprocessing
  * Read input : [Input](https://github.com/podo47/Apriori-Algorithm/blob/main/input.txt)
  
  
  ``` python
  path = 'filename.txt'
  ```

  * Modify input format and store in list
  
* Output 
``` python
test = Apriori() # Please enter min support and min confidence 
```
## 3. Output:"output.csv"

Example : [Output](https://github.com/podo47/Apriori-Algorithm/blob/main/output.csv)
* min support : 0.001
* min confidence : 0.05

| Rule:left       | → | Rule:right | Confidence           |
|-----------------|---|------------|----------------------|
| 32              | → | 38         | 0.18678710358014108  |
| 32              | → | 39         | 0.5574602755983386   |
| 32              | → | 41         | 0.2107206435023406   |
| 32              | → | 48         | 0.5297026438979363   |
| ...             | → | ...        | ... |
| "{48, 41, 38}"  | → | 39         | 0.8386689132266217   |
| "{48, 170, 38}" | → | 39         | 0.7756827048114434   |
| "{48, 110, 38}" | → | 39         | 0.7575312270389419   |
| "{48, 41, 39}"  | → | 32         | 0.22345913657344557  |
| "{48, 41, 39}"  | → | 38         | 0.2702959543850122   |
| "{48, 170, 39}" | → | 38         | 0.9892205638474295   |
| "{48, 110, 39}" | → | 38         | 0.9942140790742526   |


## 3. Reference
[1] Apriori Algorithm from Scratch

https://www.kaggle.com/code/bismakhan08/apriori-algorithm-from-scratch/notebook

[2] Apriori Algorithm from Scratch - Python

http://www.vucreations.com/articles/apriori-algorithm-from-scratch-Python.html
