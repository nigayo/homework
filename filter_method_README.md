
# array filter method syntax

array.filter(function(currentValue, index, arr), thisValue)
// 배열 안의 각각의 원소마다 함수를 적용한 후 그 결과값을 리턴하는 함수
___
#example
```javascript
<!DOCTYPE html>
<html>
<body>

<p>Click the button to get every element in the array that has a value of 18 or more.</p>

<button onclick="myFunction()">Try it</button>

<p id="demo"></p>

<script>
var ages = [32, 33, 16, 40];

function checkAdult(age) {
    return age >= 18;
}

function myFunction() {
    document.getElementById("demo").innerHTML = ages.filter(checkAdult);
}
</script>

</body>
</html>
___
