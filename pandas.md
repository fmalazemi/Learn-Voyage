### 👇🏼 Table A
|   | Animal  | ExpAge| 
|---|-------- | ------- | 
| 0 | Dog     | 10      | 
| 3 | Cat     | 15      |
| 1 | Wolf    | 7       | 
| 2 | Tiger   | 12      |



### Slicing
- `.iloc[]` takes only integers and similar to list slicing. 
  - `A.iloc[0:3]` return the whole A.
- `.loc[]` takes label only and slice based on given labels postision.
  - `A.loc[0:3]` return first two rows. NOT the whole A. i.e. `A.loc[0:3] = A.iloc[0:2]`.
  - **CAUTION**: If labels are integers and not in-order then `iloc[]` and `loc[]` give different outputs. 
### idxmax
- 
  
### Misc
- `.idxmax()` returns the index label largest values in a series (or column.) 
  -`A['ExpAge'].idxmax()` returns label 3 for cat. 
- `.mean()` 
- `.median()`
- `.apply(func, arg*)` Similar to built-in `map` but on dataFrames instead.  
