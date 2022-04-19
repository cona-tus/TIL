# 연산자 (Operator)

<br/>

## 표현식 (Expression)

<br/>

- 표현식은 리터럴, 식별자, 연산자, 함수 등의 조합으로 이루어진다.
- 값으로 평가될 수 있는 문!

```javascript
// 변수 선언문은 표현식이 아닌 문
let a;

// 할당문은 표현식인 문
x = 2;
let a = (b = 100);
```

<br/>

---

<br/>

## 산술 연산자 (arithmetic operator)

<br/>

### 이항 산술 연산자(binary operator)

```
+ 덧셈
- 뺄셈
* 곱셈
/ 나눗셈
% 나머지값
** 지수(거듭제곱) es7
```

```javascript
4 + 2; // 6
4 - 2; // 2
4 * 2; // 8
4 / 2; // 2
4 % 2; // 0
4 ** 2; // 16
Math.pow(4, 2); // 16
```

<br/>

### 단항 산술 연산자 (unary operator)

```
+ 양
- 음
! 부정
```

```javascript
let x = 5;

x = -x; // -1 * 5
console.log(x); // -5

x = -x;
console.log(x); // 5

x = +x;
console.log(x); // 5

x = -x;
console.log(x); // -5

x = +x;
console.log(x); // +(-5)
```

<br/>

### 증가 & 감소 연산자 (increment & decrement operator)

```javascript
let x = 1;
x++; // x = x + 1;
console.log(x); // 2

x--; // x = x - 1;
console.log(x); // 1
```

<br/>

증가/감소(++/--) 연산자는 위치에 따라 의미가 바뀐다.

> `x++ / x--` : 필요한 연산을 수행하고, 그 뒤 값을 증가/감소시킴  
> `++x / --x` : 값을 먼저 증가/감소시킨 후, 연산을 수행

```javascript
x = 0;
let y = x++; // x에 0을 할당
console.log(y); // 0 위 코드가 끝나면 x의 값을 증가
console.log(x); // x = 1

x = 0;
y = ++x; // 값 먼저 증가
console.log(y); // 1 증가된 값을 할당
console.log(x); // 1
```

<br/>

---

<br/>

## 문자열 연결 연산자

> 숫자와 문자열을 더하면 + `문자열`로 동작한다.

```javascript
string = '1' + 1;
console.log(string); // '11'
console.log(typeof string); // string
```

<br/>

---

<br/>

## 할당 연산자 (assignment operator)

```
=
+=
-=
*=
/=
%=
```

```javascript
let x;

x = 10;
console.log(x); // 10

x += 5; // x = x + 5;
console.log(x); // 15

x -= 5; // x = x - 5;
console.log(x); // 10

x *= 5; // x = x * 5;
console.log(x); // 50

x /= 5; // x = x / 5;
console.log(x); // 10

x %= 5; // x = x % 5;
console.log(x); // 0
```

<br/>

---

<br/>

## 비교 연산자 (comparison operator)

<br/>

### 동등/일치 비교 연산자(equality operator)

```
== 값이 같음
!= 값이 다름
=== 값과 타입이 둘다 같음
!== 값과 타입이 둘다 다름
```

```javascript
// 동등비교
2 == 2; // true
2 != 2; // false
2 != 3; // true
2 == 3; // false
2 == '2'; // true
true == 1; // true
false == 0; // true
0 == -0; // true

// 일치비교
2 === '2'; // false
true === 1; // false
false === 0; // false
0 === -0; // true
NaN === NaN; // false
```

```javascript
const objA = {
  name: 'js',
};

const objB = {
  name: 'js',
};

objA == objB; // false 메모리 주소가 다름
objA === objB; // false

objA.name == objB.name; // true
objA.name === objB.name; // true

let objC = objB;
objC == objB; // true 동일한 메모리 주소라서 값과 타입이 같음
objC === objB; // true
```

<br/>

### 대소 관계 비교 연산자 (relational operator)

> 특정 값과 값을 비교하여 불리언 값을 반환한다.

<br/>

```javascript
> 크다
< 작다
>= 크거나 같다
<= 작거나 같다

2 > 0; // true
2 > 2; // false
2 >= 2; // true
2 <= 2; // true
```

<br/>

---

<br/>

## 삼항 조건 연산자 (ternary operator)

```
조건식 ? 조건식이 true일 때 반환할 값 : 조건식이 false일 때 반환할 값
```

```javascript
let x = 5;

let result = x % 2 ? '홀수' : '짝수';
console.log(result); // 홀수
```

<br/>

---

<br/>

## 논리 연산자(logical operator)

```
|| 또는
&& 그리고
! 부정
!! 불리언 값으로 변환
```

```javascript
// && (and)
true && true; // true
true && false; // false
false && true; // false
false && false; // false

// || (or)
true || true; // true
true || false; // true
false || true; // true
false || false; // false

// ! (not)
!'text'; // false
!true; // false
!1; // false

// !! (boolean)
!!'text'; // true
!!true; // true
!!1; // true
```

<br/>

---

<br/>

## typeof 연산자

> `데이터 타입 확인!`  
> 피연산자의 데이터 타입을 문자열로 반환한다.

```
string
number
boolean
undefined
symbol
object
function
```

```javascript
typeof ''; // string
typeof 1234; // number
typeof NaN; // number
typeof true; // boolean
typeof undefined; // undefined
typeof Symbol(); // symbol
typeof null; // object
typeof []; // object
typeof {}; // object
typeof function () {}; // function
```

```javascript
// 숫자가 아닌 타입을 숫자로 변환하면?
console.log(+false); // 0
console.log(+null); // 0
console.log(+''); // 0
console.log(+true); // 1
console.log(+'text'); // NaN
console.log(+undefined); // NaN
```

<br/>

---

<br/>

## 연산자 우선순위 (priority)

> 여러 개의 연산자로 이루어졌을 때, 연산자가 실행되는 순서

```javascript
let a = 2;
let b = 3;

let result = a + b * 4; // 2 + ( 3 * 4 )
console.log(result); // 14

result = a++ + b * 4; // 2 + ( 3 * 4 )
console.log(result); // 14
console.log(a); // 3

// 우선하고 싶은 것을 괄호로 묶어주기
result = ((a + b) * 4) / 5;
console.log(result);
```
