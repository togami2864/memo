## every()  
**配列**が条件をすべて満たす場合にtrueを返す  
## some()  
**配列**が条件を一つでも満たしていればtrueを返す  
## 空かどうかの判定

```
career = {
  company: ""
  endAt: ""
  position: ""
  startAt: ""
}

  Object.values(career)
  //結果: ["","","",""]
```  
引数に渡されたobject(career)の**値**を配列に格納する  
配列にした上でメソッドを使う

```
const isEmptyCareer = (career: Career) => {
  return Object.values(career).every((v) => !v);
};
```  
""はJSにおいてfalseと判定される  
->全て空の時!vは全てtrue  
->isEmptyCareerがtrueを返す(全て空と認識)

