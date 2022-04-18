# gitflow-test

## 測試

 - 在結束feature時，不要rebase到Develop
 - feature 完成時，有無Delete branch的差異
 - feature完成前後，PR的差別
 - pull request時，merge到其他分支?

1. 新建`feature1`(不要rebase、不要delete)
    - 結束`feature1`後push上去
    - 在repository上有PR，是從develop merge到master的請求
2. 新建`feature5`(不要rebase、不要delete)
    - 尚未結束feature5時push上去
3. 新建`feature2`(不要rebase)
    - 尚未結束`feature2`時push上去，PR會多一個請求
    - 在分支上會多一個feature2的分支可選
4. 新建`feature3`(一樣不要rebase)
    - 結束`feature2`後再push上去
    - 沒有PR
5. 新建`feature4`(不要delete、但rebase)
    - 尚未結束`feature2`時push上去


## 結論