# 初めの１０問  
## 第０問  
```
a = int(input())
b, c = (int(x) for x in input().split())
print(a+b+c, input())
// 実行結果
10
10 10
asd
30 asd
//
```
・int()　　
整数に変換したい時に使う　　
float()とかもある。  
・input()  
ユーザーが入力。特に指定しない限り型はstr(:文字列)みたい。　　
整数にしたきゃint()の中に入れる。  
・.split()  
複数の入力が欲しいとき使う  
・b, c = (int(x) for x in input().split())　　
リスト内包表記。input().split()でえた値をintに変換する。

## 第１問  
```
a, b = (int(x) for x in input().split())
if (a*b) % 2:
    print("Odd")
else:
    print("Even")
```
数値は0以外はtrue  

## 第２問  
```
print(input().count("1"))
```  

## 第３問  
```
n = input()
a = (int(x) for x in input().split())
ans = float("inf")
for i in a:
    ans = min(ans, len(bin(i)) - bin(i).rfind("1") - 1)
print(round(ans))
```
