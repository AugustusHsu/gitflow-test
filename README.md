# gitflow-test

## 測試

 - 在結束feature時，不要rebase到Develop
 - feature 完成時，有無Delete branch的差異
 - feature完成前後，PR的差別
 - pull request時，merge到其他分支?

1. 新建`feature1`(不要rebase、不要delete)
    - 結束`feature1`後push上去
    - 在repository上有PR

2. 新建`feature5`(不要rebase、不要delete)
    - 尚未結束`feature5`時push上去
    - 在分支上會多一個`feature5`的分支可選
    - 在repository上有PR

3. 新建`feature2`(不要rebase)
    - 尚未結束`feature2`時push上去
    - 在分支上會多一個`feature2`的分支可選
    - 在repository上有PR

4. 新建`feature3`(不要rebase)
    - 結束`feature2`後再push上去
    - 沒有PR

5. 新建`feature4`(不要delete、但rebase)
    - 尚未結束`feature4`時push上去
    - 在分支上會多一個`feature4`的分支可選
    - 在本地端graph上不會出現分支
6. 新建`feature6`(不要delete、但rebase)
    - 結束`feature6`後再push上去


## 結論

|  |  尚未結束就push上去   | 結束才push上去  | 
|  ----  | ----  | ----  |
|  都不要  | `feature5`  | `feature1`  |
| delete  | `feature2` | `feature3`  |
| rebase  | `feature4` | `feature5`  |
| delete & rebase  | `feature5` | `feature5`  |
