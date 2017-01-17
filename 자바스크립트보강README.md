
# 1.홀수의 합을 구하는 함수
```javascript
function sumOdd(n){
  var sum=0;
  for(var i=1; i<=n; i+=2){
    if(i%2!==0){
      sum=sum+i;
    };
  };return sum;
};
// 임의의 수 n까지의 홀수의 합을 구하는 함수는 구했는데 그냥 홀수의 합을 구하는 함수...??
```
___
# 2.1~100 중 7의 배수를 구하는 함수
```javascript
function chkseven(){
  for(var i=1; i<=100; i++){
    if(i%7===0){
      console.log(i);
    };
  };
};
```
___
# 3.삼각형 넓이 구하는 함수
```javascript
function getTriArea(){
  arguments.length=2;
  var recArea=1
  for(var i=0; i<arguments.length; i++){
    recArea=recArea*arguments[i];
  }var triArea=recArea*1/2;
  return triArea;
}
```
___
# 4. 1 부터 n까지 더하는 함수
```javascript
function getSum(n){
  var sum=0
  for(var i=1; i<=n; i++){
    sum = sum+i;
  }return sum;
}
```
___
# 5. 짝수만 출력하는 함수
```javascript
var arr = [1,2,3,100,40,50,88,23,"23"];
function getEven(arry){
  for(var i=0; i<arry.length; i++){
    if(arry[i]%2===0){
      console.log(arry[i]);
    }
  }
}
```
___
# 6. 문자열만 출력하는 함수
```javascript
var arr = [1,2,3,100,40,"50",88,23,"23"];
function getStr(arry){
  for(var i=0; i<arry.length; i++){
    if(typeof arry[i]==="string"){
      console.log(arry[i]);
    }
  }
}
```
___
# 7. 10 보다 크고 80 보다 작은 숫자만 새로운 배열로 반환하는 함수
```javascript
var arr = [1,92,53,100,40,"50",88,23,"23"];
var maxNum = 80
var minNum = 10
function getArry(arry){
  newArry=[];
  for(var i=0; i<arry.length; i++){
    if((arry[i]>minNum) & (arry[i]<maxNum)){
      newArry.push(arry[i]);
    }
  }return newArry;
}
getArry(arr);
```
___
# 8. 10 보다 크고 80 보다 작은 숫자를 제외한 배열로 변경
```javascript
var arr = [1,2,3,100,40,"50",88,23,"23"];
var maxNum = 80
var minNum = 10

function getArry(arry){
  newArry=[];
  for(var i=0; i<arry.length; i++){
    if(!(arry[i]>minNum & arry[i]<maxNum)){
      newArry.push(arry[i]);
    }
  }return newArry;
}
getArry(arr);
```
___
# 9. 배열 원소 앞에 "kim" 이라는 문자열을 추가해 새로운 배열 반환
```javascript
var arr = ["jehee", "hewon", "miji", "jungho"];
var newArr = appendKim(arr);
function appendKim(arry){
  newArry=[];
  for(var i=0; i<arry.length; i++){
    getKim="kim"+arr[i];
    newArry.push(getKim);
  }return newArry;
}
console.log(newArr);
```
___
# 10. url 만 뽑아서 새로운 배열로 만들어 반환하는 함수
```javascript
var data = [
{"name":"youtube", "url":"www.youtube.com","since":2000},
{"name":"google", "url":"www.google.com", "since":1999},
{"name":"naver", "url":"www.naver.com", since:2001},
{"name":"daum", "url":"www.daum.com", since:2003}
]
function getUrl(arry){
  newArry=[];
  for(var i=0; i<arry.length; i++){
    newArry.push(arry[i].url);
  }return newArry;
}
getUrl(data);
```
___
# 11. 출력결과가 html 이 나와야 하는데 css가 나오는 이유
```javascript
name = "javascript";
function a() {
  var name = "html";
  function b(){
    name = "css";
  }
  b();
  console.log("my name is html -> ", name);
}
a();

// 처음 name은 "javascript"였는데 함수 a 를 호출하면서 "html"로 바뀌고
// a 함수 내의 b 함수가 호출되면서 name 값이 css 로 바뀌기 때문에?
```
