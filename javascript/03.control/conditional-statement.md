# 제어문 (Control)

<br/>

## 조건문 (conditional statement)

<br/>

### if ... else 문

> `불리언` 값으로 평가된다.

```javascript
if (조건식1) {
  // 조건식1이 참일 때
} else if (조건식2) {
  // 조건식2가 참일 떄
} else {
  // 조건식1과 조건식2가 거짓일 때
}
```

```javascript
if ((false, 0, '', null, undefined)) {
  console.log('출력되지 않음!');
  // true 일 경우 실행이 됨
}
```

<br/>

### switch 문

> 정해진 범위 안의 값에 대해 특정한 일을 해야 하는 경우.  
> 불리언보다는 상황(case)에 따라 실행할 코드를 결정한다.

```javascript
switch (표현식) {
    case 표현식1:
        표현식과 표현식1이 일치하면 실행될 문;
        break // 사용하지 않으면 마지막 문을 실행
    case 표현식2:
        표현식과 표현식2가 일치하면 실행될 문;
        break
    default:
        표현식과 일치하는 case문이 없을 때 실행될 문;
}
```

```javascript
let day = 6;
let dayName;

switch (day) {
  case 0:
    dayName = '월요일';
    break;
  case 1:
    dayName = '화요일';
    break;
  case 2:
    dayName = '수요일';
    break;
  case 3:
    dayName = '목요일';
    break;
  case 4:
    dayName = '금요일';
    break;
  case 5:
    dayName = '토요일';
    break;
  case 6:
    dayName = '일요일';
    break;
  default:
    console.log('해당하는 요일이 없음!');
}
console.log(dayName); // 일요일

// break를 사용하지 않는 경우
let mood = 'happy';
let text;
switch (mood) {
  case 'happy':
  case 'nice':
    text = 'Wonderful day!';
    break;
  case 'bad':
    text = 'It will be alright..';
    break;
}
console.log(text); // wonderful day
```
