---
title: 03-BaekShin-Git
date: 2019-04-04 16:38:33
tags: Git
categories: Git
---
### 1. Git Branch 사용하기

---

```bash
$ git branch #현재 존재하는 branch 조회
$ git checkout #현재 작업중인 brach 조회
$ git checkout branch1 #전환
```



```bash
$ git branch branch1 master
```

+ master에서 branch1이름의 branch 만들기



```bash
$ git checkout -b branch1 master
```

+ master에서 branch1이름의 branch 만들고 checkout함(전환)



```bash
$ git branch -d branch1 #삭제(github는 유지)
$ git push origin -delete branch1 #삭제(github는 삭제)
```



#### 1.1 merge와 rebase

- merge, rebase 차이
- merge시 fast-forward 충돌 해결법 또는 ff 가 무엇인지

