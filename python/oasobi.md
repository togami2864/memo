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
float(),str()とかもある。  
・input()  
ユーザーが入力。特に指定しない限り型はstr(:文字列)みたい  　
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
*pythonはこのての処理は強い  

## 第３問  
```
n = input()
a = (int(x) for x in input().split())
ans = float("inf")
for i in a:
    ans = min(ans, len(bin(i)) - bin(i).rfind("1") - 1)
print(round(ans))
```

## 第４問  
```
a, b, c, x = map(int, [input() for i in range(4)])
ans = 0
for i in range(a+1):
    for j in range(b+1):
        for k in range(c+1):
            if i * 500 + j * 100 + k * 50 == x:
                ans += 1
print(ans)
```
・range("int")  
決まった回数回したい時に。　　
今回入力は４つなので、4。  

・リスト内包表記(頻出)  
[式 for 任意の変数名 in イテラブルオブジェクト]  
＊イテラブルオブジェクト:for 文で繰り返せるオブジェクトまたはそのクラス  
リストやタプルなどのイテラブルオブジェクトの各要素を任意の変数名で取り出し式で評価、その結果が要素となる新たなリストが返される。  
今回の場合input()を単純に４回繰り返す。(式自体にiは関与してない)  






