---
title: 02_Park_Git
date: 2019-04-04 13:52:54
tags: Git
categories: Git
---
## 💡 Intro
Git Branch 관련된 자료 

___
## 💡 Index

👉 Git  

👉 Branch CMD

👉 Branch Practice

___

## 💡 Git Base
### 👉 PDF Attached
**[📃 PDF FILE ](../pdf/Git.pdf)** 
{% asset_link Git.pdf 📃 PDF FILE %}
___

## 💡 Branch CMD
### 👉 Why Using the Branch system ?
["A successful Git branching model" 컬럼](https://backlog.com/git-tutorial/kr/stepup/stepup1_5.html)

원문 : http://nvie.com/posts/a-successful-git-branching-model/
### 👉 CRUD
```bash
### Create and Switch 
$ git branch iss53 # 브런치 만들고 
$ git checkout iss53 # 전환
# 두개를 하나로 줄이면
$ git checkout -b iss53

### Push
$ git checkout iss53
$ git add -u 
$ git commit -m "YOUR MESSAGE"
$ git push origin iss53

### Merge
$ git checkout master
$ git merge iss53

### Branch List
$ git Branch

### Delete
$ git branch -d iss53
```
___

## 💡 Branch Practice
### 👉 To-Do
1. Master 에서 아무 Py 파일 하나 만들어서 tracking 후
2. dev 브런치를 판다. 
3. 이동해서 1번에서 만든 파일을 수정 
4. master Branch에 merge 
___

## 💡 Ref Link
* [누구나 쉽게 이해할수있는 Git 입문](https://backlog.com/git-tutorial/kr/stepup/stepup1_1.html)
* [Git-scm](https://git-scm.com/book/ko/v1/Git-%EB%B8%8C%EB%9E%9C%EC%B9%98-%EB%B8%8C%EB%9E%9C%EC%B9%98%EC%99%80-Merge%EC%9D%98-%EA%B8%B0%EC%B4%88)

