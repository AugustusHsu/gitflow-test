# gitflow-test

使用GitKraken測試

## feature測試

 - 在結束feature時，不要rebase到Develop
 - feature 完成時，有無Delete branch的差異
 - feature完成前後，PR的差別
 - pull request時，merge到其他分支?

1. 新建`feature1`(不要rebase、不要delete)
    - 結束`feature1`後push上去
    - 沒有可選分支
    - graph有分支
    - 有PR

2. 新建`feature5`(不要rebase、不要delete)
    - 尚未結束`feature5`時push上去
    - 遠端有分支出現
    - graph有分支
    - 有PR 

3. 新建`feature2`(不要rebase、但delete)
    - 尚未結束`feature2`時push上去
    - 遠端有分支出現
    - graph有分支
    - 有PR

4. 新建`feature3`(不要rebase、但delete)
    - 結束`feature3`後再push上去
    - 沒有可選分支
    - graph有分支
    - 沒有PR

5. 新建`feature4`(不要delete、但rebase)
    - 尚未結束`feature4`時push上去
    - 遠端有分支出現
    - graph沒分支
    - 有PR

6. 新建`feature6`(不要delete、但rebase)
    - 結束`feature6`後再push上去
    - 遠端有分支出現
    - graph沒分支
    - 有PR

7. 新建`feature7`(delete、rebase)
    - 尚未結束`feature7`時push上去
    - 遠端有分支出現
    - graph沒分支
    - 有PR

8. 新建`feature8`(delete、rebase)
    - 結束`feature8`後再push上去
    - 沒有可選分支
    - graph沒分支
    - 沒有PR

## hotfix測試

1. 不刪除分支
    - graph沒分支
2. 刪除分支
    - 尚未結束就push上去、結束才push上去(似乎沒差別)
    - graph有分支

## release測試

1. 不刪除分支
    - 會留分支在本地
2. 刪除分支
    - 建議刪除分支


## 結論

### feature結論

|  |  尚未結束就push上去   | 結束才push上去  | 
|  ----  | ----  | ----  |
|  都不要  | `feature5` graph有分支 有PR 遠端有分支出現 | `feature1` graph有分支 有PR 遠端不會有分支出現|
| delete  | `feature2` graph有分支 有PR 遠端有分支出現| `feature3` graph有分支 沒有PR 遠端不會有分支出現|
| rebase  | `feature4` graph沒分支 有PR 遠端有分支出現 | `feature6` graph沒分支 有PR 遠端有分支出現 |
| delete & rebase  | `feature7` graph沒分支 有PR 遠端有分支出現 | `feature8` graph沒分支 有PR 遠端不會有分支出現 |

 - 不要rebase分支到develop，不然graph不會有分支圖示
 - PR較不重要，在遠端不要接受就好
 - 分支再到遠端刪除就好
 - delete分支的狀況下，不要結束才push上去，不然不會有graph
 - **graph上有分支、結束feature開發後在遠端刪除分支、有無PR不重要(刪除分支，PR就會消失)**
 - 故在**delete分支**、**不要接受PR**的情況下開發就行

    ## 個人開發狀況下PR都不要接受!!!!

### hotfix結論

**刪除hotfit分支**

### release結論

**刪除分支，在github上新增release和tag**