 # 非同期処理関連  
 ## async
 非同期関数を定義する関数宣言のこと。  
以下のように関数の前にasyncを宣言することにより、非同期関数（async function）を定義できる。

```
async function hoge() {}
```

## await  
async function内でPromiseの結果が返されるまで待機する（処理を一時停止する）演算子をさす。  
```
async function hoge() {
    const result = await hogePromise();

    // Promiseの結果が返ってくるまで以下は実行されない
    console.log(result);
}
```

## fetch  
返り値はPromise  
先頭に awaitをつければ  
```
await fetch("https://hogehoge.com/api/v2/items");
```  
Responese が得られる(Promiseの中身)  
.json()メソッドを使えばjsonで帰ってくる
