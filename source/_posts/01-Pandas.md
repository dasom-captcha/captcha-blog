---
title: 01_Pandas
date: 2019-04-04 13:35:51
tags: Python
categories: Python
---
## 1. Pandas

Python Data Analysis Library

+ 파이썬에서 사용하는 데이터분석 라이브러리

+ 행과 열로 이루어진 데이터 객체를 만들어 다룰 수 있게 함.

+ 보다 안정적으로 대용량의 데이터들을 처리하는데 매우 편리한 도구


## 2. Pandas 자료 구조 

+ 1차원 자료구조 : Series

+ 2차원 자료구조 : DataFrame

+ 3차원 자료구조 : Panel


### (1) Series

 Series is a one-dimensional labeled array capable of holding any data type (integers, strings, floating point numbers, Python objects, etc.). 

+ 가장 간단한 1차원 자료구조

+ Series는 배열/리스트와 같은 일련의 시퀀스 데이타를 받아들인다.

+ 별도의 인덱스 레이블을 지정하지 않으면 자동적으로 0부터 시작되는 디폴트 정수 
인덱스를 사용한다.

+ 선언 >>> s = pd.Series(data, index=index)

```
import pandas as pd

obj = pd.Series([4, 7, -5, 3])
```

### (2) DataFrame

 DataFrame is a 2-dimensional labeled data structure with columns of potentially different types. You can think of it like a spreadsheet or SQL table, or a dict of Series objects. It is generally the most commonly used pandas object. 

+ 2차원 자료구조

+ DataFrame는 행과 열이 있는 테이블 데이타(Tabular Data)를 받아들인다. 

+ 이는 python의 dictionary 또는 numpy의 array로 정의할 수 있다.

```
data = {'name' : ['Beomwoo', 'Beomwoo', 'Beomwoo', 'Kim', 'Park'], 'year':[2016, 2014, 2015, 2016, 2017]}, 'points' : [1.5, 1.7, 3.6, 2.4, 2.9]}

df = pd.DataFrame(data)
```
|  <center>name</center> |  <center>year</center> |  <center>points</center> |
|:--------|:--------:|--------:|
|Beomwoo | <center>2016 </center> |1.5 |
|Beomwoo | <center>2014 </center> |1.7 |
|Beomwoo | <center>2015 </center> |3.6 |
|Kim | <center>2016 </center> |2.4 |
|Park | <center>2017 </center> |2.9 |

### (3) Panel

 Panel is a somewhat less-used, but still important container for 3-dimensional data. The term panel data is derived from econometrics and is partially responsible for the name pandas: pan(el)-da(ta)-s. The names for the 3 axes are intended to give some semantic meaning to describing operations involving panel data and, in particular, econometric analysis of panel data.

+ 3차원 자료구조

+ Panel은 Axis 0 (items), Axis 1 (major_axis), Axis 2 (minor_axis) 등 3개의 축을 가지고 있다

+ Axis 0은 그 한 요소가 2차원의 DataFrame 에 해당되며, Axis 1은 DataFrame의 행(row)에 해당되고, Axis 2는 DataFrame의 열(column)에 해당된다.

+아래 예제는 numpy를 사용하여 3차원 난수를 발생시킨 후, 이를 pandas.Panel()에 적용한 예이다.
```
data = np.random.rand(2,3,4)
p = pd.Panel(data)
```
2(items) * 3(major axis) * 4(miner axis)  크기의 Panel 객체가 생성되었음을 알 수 있다.
Panel 객체 p로부터 p[0]을 조회하면, Axis 0의 첫번째 요소인 DataFrame이 출력됨을 볼 수 있다.


## 3. 데이터 액세스

+ Indexing, arrtibute 사용 
```
df['year'] #year column 출력 
df.year #위에와 같은 의미
```
+ Boolean indexing : 특정 조건의 데이터만 필터링 
```
df[df['year']>2016] #df자료에서 year이 2016보다 큰 행만 출력 
```
+ 데이터 양이 많은 경우
```
df.head() #기본적으로 앞 5개, 데이터의 개수를 인자로 넣으면 그 만큼의 데이터를 보여준다.
df.tail() #기본적으로 뒤 5개, 위와 같다.
```
+ 다양한 연산 함수 : sum(), mean(), max(), min(), describe() ...

+ 1주차 피드백 : 첫번째 행에서 첫번째 열 뽑기 
```
print(df.loc[df.index[0], df.columns[0]]) #.loc는 [인덱스(행)명, 칼럼(열)명]으로 접근 가능하다
print(df.iloc[0,0]) #.iloc는 index숫자로써 가져온다.
```


## 4. 외부 데이터 읽고 쓰기

 + pandas는 CSV 파일, 텍스트 파일, 엑셀 파일, SQL 데이타베이스, HDF5 포맷 등 다양한 외부 리소스에 데이타를 읽고 쓸 수 있는 기능을 제공

```
df = pd.read_excel('foo.xlsx', 'Sheet1', index_col=None, na_values=['NA']) #읽기
df = pd.to_excel('foo.xlsx', sheet_name='Sheet1') #쓰기

```

## 참고 출처 

+ [예제로 배우는 Python 프로그래밍 : Pandas데이터 분석](http://pythonstudy.xyz/python/article/408-pandas-%EB%8D%B0%EC%9D%B4%ED%83%80-%EB%B6%84%EC%84%9D)

+ [Pandas 기초 정리](https://doorbw.tistory.com/172)

+ [pandas 데이터 구조 소개](https://pandas.pydata.org/pandas-docs/stable/getting_started/dsintro.html)
