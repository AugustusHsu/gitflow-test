# gitflow-test

 - 在結束feature時，不要rebase到Develop
 - feature 完成時，有無Delete branch的差異
 - feature完成前後，PR的差別
 - pull request時，merge到其他分支?

1. 新建feature1(不要rebase、不要delete)
    - 在repository上有PR，是從develop merge到master的請求
2. 新建feature2(不要rebase)
    - 尚未結束feature2時push上去，PR會多一個請求
    - 