# 마크다운 (문법)

# 제목 (Header)

```
# 제목 1
## 제목 2
### 제목 3
### 제목 4
##### 제목 5
###### 제목 6
```

```
제목 1
======

제목 2
------
```

# 문장 (Paragraph)

동해물과 백두산이 마르고 닳도록 하느님이 보우하사 우리나라 만세

<br/>

# 줄바꿈 (Line Breaks)

동해물과 백두산이 마르고 닳도록  
하느님이 보우하사 우리나라 만세<br />
무궁화 삼천리 화려 강산

<br/>

# 강조 (Emphasis)

_이탤릭_  
**두껍게**  
**_이탤릭 + 두껍게_**  
~~취소선~~  
<u>밑줄</u>

<br/>

# 목록 (List)

1. 순서가 필요한 목록
2. 순서가 필요한 목록
   1. 순서가 필요한 목록
3. 순서가 필요한 목록

- 순서가 필요하지 않은 목록
  - 순서가 필요하지 않은 목록

* 순서가 필요하지 않은 목록
  - 순서가 필요하지 않은 목록

- 순서가 필요하지 않은 목록
  - 순서가 필요하지 않은 목록

<br/>

# 링크 (Links)

[GOOGLE](https://google.com)  
[NAVER](https://www.naver.com/ 'Naver로 이동!')

<br/>

# 이미지

![NAVER](https://image.rocketpunch.com/company/5466/naver_logo.png?s=400x400&t=inside)
[![NAVER](https://image.rocketpunch.com/company/5466/naver_logo.png?s=400x400&t=inside)](https://www.naver.com/)

<br/>

# 인용문 (BlockQuote)

> 남의 말이나 글에서 직접 또는 간접으로 따온 문장.
> _(네이버 국어 사전)_
>
> > 인용문을 작성하세요!
> >
> > > 중첩된 인용문
> > >
> > > > 중중첩된 인용문 1

<br/>

# 인라인(inline) 코드 강조

CSS에서 `background` 혹은 `background-image` 속성으로 요소에 배경 이미지를 삽입할 수 있습니다.

<br/>

# 블록(block) 코드 강조

```html
<a href="https://www.google.co.kr/" target="_blank">GOOGLE</a>
```

```css
.list > li {
  position: absolute;
  top: 40px;
}
```

```javascript
function add() {
  const a = '123';
  return a;
}
```

```bash
$ git commit -m ‘Study Markdown’
```

```plaintext
동해물과 백두산이 마르고 닳도록
```

<br/>

# 표(Table)

Position 속성
값 | 의미 | 기본값
--|:--:|--:
Static | 기준없음 | O
Relative | 요소 자신 | X
Absolute | 위치 상 부모 요소 | X
Fixed | 뷰포트 | X

<br/>

# 원시 HTML (Raw HTML)

동해물과 <u>백두산</u>이 마르고 닳도록<br />
<span style=“text-decoration:underline;”>백두산</span>

<a href="naver.com" title="네이버로 이동!" target="_blank">Naver</a>

<img width="20px" src="https://image.rocketpunch.com/company/5466/naver_logo.png?s=400x400&t=inside" alt="NAVER" />

<br/>

# 수평선

<br/>

---

(Hyphens)

<br/>

---

(Asterisks)

<br/>

---

(Underscores)

<br />
