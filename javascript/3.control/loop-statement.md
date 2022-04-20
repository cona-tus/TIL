# 제어문 (Control)

<br/>

## 반복문 (loop statement)

> 조건식이 `참`일 경우 코드 블록을 실행한다.  
> 그 후 조건식을 다시 평가하여 `거짓이 될 때까지 반복`한다.

<br/>

### for 문

> 반복 횟수가 명확할 때 사용한다.

```javascript
for (변수 선언문 또는 할당문; 조건식; 증감식){
    조건식이 참인 경우 반복 실행될 문;
}

for (let i = 0; i < 4; i++){
    console.log(i);
}

for (let i = 2; i < 5; i = i + 2) {
  console.log(i);
}
```

```
실행 순서
 1. 변수 선언문(let i = 0)을 실행해서 변수를 초기화
 2. 조건식의 값이 참이면 코드 블록 수행
 3. 증감식(i++) 실행되어 값 증가
 4. 다시 조건식 시작 (변수 선언문은 한번만 실행)
 5. 조건식이 거짓이 될 때까지 2번과 3번을 반복
```

```javascript
// 중첩 사용할 수 있다.
for (let i = 0; i <= 4; i++) {
  for (let j = 0; j <= 4; j++) {
    if (i + j === 4) console.log({ i }, { j });
  }
}
// [0, 4] [1, 3] [2, 2] [3, 1] [4, 0]


// 무한루프
for (;;) { ... }
```

<br/>

### while 문

> 반복 횟수가 불명확할 때 사용한다.

```javascript
while (조건){
   // 조건식이 false가 될 때까지 코드블록 반복 실행
}


let num = 0;
while (num < 4) {
    console.log(num); // 0 1 2 3
    num++;
}


let isTrue = true;
let i = 0;
while (isTrue) {
  console.log('It is True!', i);
  i++;
  if (i === 5) {
    break;
  }
} // i = 0, 1, 2, 3, 4


// 무한루프
while (true) { ... }
```

<br/>

### do ... while 문

> `while`은 `조건이 true`일 때만 코드블록이 실행된다.  
> `do while`은 `코드블록을 먼저 실행`하고, 조건식을 평가한다.  
> 코드블록은 무조건 한 번 이상 실행된다!

<br/>

```javascript
let num = 0;

do {
  console.log(num); // 0 1 2 3
  num++;
} while (num < 4);
```

<br/>

---

## 반복문 제어

### break 문, continue 문

> `break`는 코드 블록을 탈출한다.  
> `continue`는 코드블록을 중단하고 반복문의 증감식

```javascript
for (let i = 0; i < 6; i++) {
  if (i === 3) {
    continue; // 아래 코드를 무시하고 반복문으로 이동
    // 0 1 2 3 4 5
    console.log('Best of three!');
    // 0 1 2 Best of three!
    break; // 반복문을 특정한 조건에 중지할 경우
  }
  console.log(i);
  // continue 문을 사용하지 않으면 if 문 내에 코드를 작성해야한다.
  // continue 문을 사용하면 if 문 밖에 코드 작성 가능!
}
```

<br/>
