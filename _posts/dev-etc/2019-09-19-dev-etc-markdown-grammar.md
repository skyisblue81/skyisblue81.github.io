---
layout: post
title: "[MarkDown] MarkDown 사용법 정리"
subtitle: ""
categories: dev
tags: etc
---



제목(Header)
-----

`<h1>` 부터 `<h6>` 까지 제목을 표현  

```md
# 제목 1
## 제목 2
### 제목 3
#### 제목 4
```

제목1(<h1>)과 제목2(<h2>)는 다르게도 표현 가능

```md
제목 1
======

제목 2
------
```



<br><br>

---

<br><br>



줄바꿈(Line Breaks)
-----

‘2번의 띄어쓰기’나 `<br>` 사용

```md
동해물과 백두산이 마르고 닳도록 
하느님이 보우하사 우리나라 만세   <!--띄어쓰기 2번-->
무궁화 삼천리 화려 강산<br>
대한 사람 대한으로 길이 보전하세
```

동해물과 백두산이 마르고 닳도록  
하느님이 보우하사 우리나라 만세   
무궁화 삼천리 화려 강산<br>
대한 사람 대한으로 길이 보전하세



<br><br>

---

<br><br>



강조(Emphasis)
-----

각각 `<em>`, `<strong>`, `<del>` 태그로 변환  
밑줄을 입력하고 싶다면 `<u></u>` 태그를 사용

```md
이텔릭체 : *별표(asterisks)* , _언더바(underscore)_
볼드체 : **별표(asterisks)** , __언더바(underscore)__
취소선 : ~~물결표시(tilde)~~
<u>밑줄</u>은 `<u></u>`를 사용
```

이텔릭체 :  *별표(asterisks)* , _언더바(underscore)_  
볼드체 : **별표(asterisks)** , __언더바(underscore)__  
취소선 : ~~물결표시(tilde)~~  
<u>밑줄</u>은 `<u></u>`를 사용



<br><br>

---

<br><br>



목록(List)
-----

`<ol>`, `<ul>` 목록 태그로 변환

```md
1. 순서가 필요한 목록
1. 순서가 필요한 목록
  - 순서가 필요하지 않은 목록(서브) 
  - 순서가 필요하지 않은 목록(서브) 
1. 순서가 필요한 목록

- 순서가 필요하지 않은 목록에 사용 가능한 기호
  - 대쉬(hyphen)
  * 별표(asterisks)
  + 더하기(plus sign)
```

1. 순서가 필요한 목록
1. 순서가 필요한 목록
  - 순서가 필요하지 않은 목록(서브) 
  - 순서가 필요하지 않은 목록(서브) 
1. 순서가 필요한 목록

- 순서가 필요하지 않은 목록에 사용 가능한 기호
  - 대쉬(hyphen)
  * 별표(asterisks)
  + 더하기(plus sign)



<br><br>

---

<br><br>



링크(Links)
-----

`<a>`로 변환

```md
[GOOGLE](https://google.com)
[NAVER](https://naver.com "링크 설명(title) 작성")
[GitHub][1]

문서 안에서 [참조 링크]를 그대로 사용

문서 내 꺾쇠 괄호(`< >`, Angle Brackets)안의 URL은 자동으로 링크를 사용  
네이버 홈페이지: <https://naver.com>  

[1]: https://github.com
[참조 링크]: https://naver.com "네이버"
```

[GOOGLE](https://google.com)  
[NAVER](https://naver.com "링크 설명(title) 작성")  
[GitHub][1]

문서 안에서 [참조 링크]를 그대로 사용

문서 내 꺾쇠 괄호(`< >`, Angle Brackets)안의 URL은 자동으로 링크를 사용  
네이버 홈페이지: <https://naver.com>  

[1]: https://github.com
[참조 링크]: https://naver.com "네이버"



<br><br>

---

<br><br>



이미지(Images)
-----

`<img>`로 변환
링크과 비슷하지만 앞에 `!`가 추가됨

```md
![대체 텍스트(alternative text)]({{site.url}}/assets/img/post/dev-etc/2019-09-19-dev-etc-markdown-grammar/GitKraken-logo.png "링크 설명(title)")

![GitKarken][logo]

[logo]: {{site.url}}/assets/img/post/dev-etc/2019-09-19-dev-etc-markdown-grammar/GitKraken-logo.png "GitKarken - Legendary Dev Tools"
```

![대체 텍스트(alternative text)]({{site.url}}/assets/img/post/dev-etc/2019-09-19-dev-etc-markdown-grammar/GitKraken-logo.png "링크 설명(title)")

![GitKarken][logo]

[logo]: {{site.url}}/assets/img/post/dev-etc/2019-09-19-dev-etc-markdown-grammar/GitKraken-logo.png "GitKarken - Legendary Dev Tools"


<br><br>

---

<br><br>



코드(Code)
-----

`<pre>`, `<code>`로 변환  
숫자 1번 키 왼쪽에 있는 `(Grave)를 입력

####인라인(inline) 코드 강조

```md
`background`혹은 `background-image` 속성으로 요소에 배경 이미지를 삽입
```

`background`혹은 `background-image` 속성으로 요소에 배경 이미지를 삽입

####블록(block) 코드 강조

`를 3번 이상 입력하고 코드 종류 추가

```md
코드종류 : html, css, javascript, bash, python, md (생략가능)
```

```java
public class Test {
    public Test(){

    }
}
```



<br><br>

---

<br><br>



표(Table)
-----

`<table>` 태그로 변환
헤더 셀을 구분할 때 3개 이상의 `-`(hyphen/dash) 기호가 필요  
헤더 셀을 구분하면서 `:`(Colons) 기호로 셀(열/칸) 안에 내용을 정렬  
가장 좌측과 가장 우측에 있는 `|`(vertical bar) 기호는 생략 가능

```md
| 값 | 의미 | 기본값 |
|---|:---:|---:|
| `static` | 유형(기준) 없음 / 배치 불가능 | `static` |
| `relative` | 요소 자신을 기준으로 배치 |  |
| `absolute` | 위치 상 부모(조상)요소를 기준으로 배치 |  |
| `fixed` | 브라우저 창을 기준으로 배치 |  |

값 | 의미 | 기본값
---|:---:|---:
`static` | 유형(기준) 없음 / 배치 불가능 | `static`
`relative` | 요소 **자신**을 기준으로 배치 |
`absolute` | 위치 상 **_부모_(조상)요소**를 기준으로 배치 |
`fixed` | **브라우저 창**을 기준으로 배치 |
```

| 값 | 의미 | 기본값 |
|---|:---:|---:|
| `static` | 유형(기준) 없음 / 배치 불가능 | `static` |
| `relative` | 요소 자신을 기준으로 배치 |  |
| `absolute` | 위치 상 부모(조상)요소를 기준으로 배치 |  |
| `fixed` | 브라우저 창을 기준으로 배치 |  |

값 | 의미 | 기본값
---|:---:|---:
`static` | 유형(기준) 없음 / 배치 불가능 | `static`
`relative` | 요소 **자신**을 기준으로 배치 |
`absolute` | 위치 상 **_부모_(조상)요소**를 기준으로 배치 |
`fixed` | **브라우저 창**을 기준으로 배치 |



<br><br>

---

<br><br>



인용문(BlockQuote)
-----

`<blockquote>` 태그로 변환

```md
인용문(blockQuote)

> 남의 말이나 글에서 직접 또는 간접으로 따온 문장.
> _(네이버 국어 사전)_

BREAK!

> 인용문을 작성하세요!
>> 중첩된 인용문(nested blockquote)
>>> 중중첩된 인용문 1
>>> 중중첩된 인용문 2
>>> 중중첩된 인용문 3
```

인용문(blockQuote)

> 남의 말이나 글에서 직접 또는 간접으로 따온 문장.  
> _(네이버 국어 사전)_

BREAK!

> 인용문을 작성하세요!  
>> 중첩된 인용문(nested blockquote)
>>> 중중첩된 인용문 1  
>>> 중중첩된 인용문 2  
>>> 중중첩된 인용문 3  



<br><br>

---

<br><br>



원시 HTML(Raw HTML)
-----

마크다운 문법이 아닌 원시 HTML 문법을 사용
마크다운에서 지원하지 않는 기능을 사용할 때 유용

```md
<figure>
  <img data-action="zoom" src="{{site.url}}/assets/img/post/dev-etc/2019-09-19-dev-etc-markdown-grammar/GitKraken-logo.png" alt="GitKarken">
  <figcaption>GitKarken - Legendary Dev Tools</figcaption>
</figure>
```

<figure>
  <img data-action="zoom" src="{{site.url}}/assets/img/post/dev-etc/2019-09-19-dev-etc-markdown-grammar/GitKraken-logo.png" alt="GitKarken">
  <figcaption>GitKarken - Legendary Dev Tools</figcaption>
</figure>



<br><br>

---

<br><br>



수평선(Horizontal Rule)
-----

각 기호를 3개 이상 입력

```md
---
(Hyphens)

***
(Asterisks)

___
(Underscores)
```
---
(Hyphens)

***
(Asterisks)

___
(Underscores)



<br><br>

---

<br><br>



특수문자(Special Character)
-----

### 예약어
`\`를 앞에 붙임

```md
\*볼드체? 특수문자!\*
```

\*볼드체? 특수문자!\*

### HTML문자
HTML Number 또는 HTML Name 사용

```md
&#42;볼드체? 특수문자!&#42;
```

&#42;볼드체? 특수문자!&#42;

<br>

### 자주 사용하는 특수문자

| Symbol | HTML Number | HTML Name |
|:---:|:---:|:---:|
| `!` | `&#33;` |  |
| `"` | `&#34;` | `&quot;` |
| `&` | `&#38;` | `&amp;` |
| `(` | `&#40;` |  |
| `)` | `&#41;` |  |
| `*` | `&#42;` |  |
| `/` | `&#47;` |  |
| `:` | `&#58;` |  |
| `;` | `&#59;` |  |
| `<` | `&#60;` | `&lt;` |
| `=` | `&#61;` |  |
| `>` | `&#62;` | `&gt;` |
| `@` | `&#64;` |  |
| `[` | `&#91;` |  |
| `]` | `&#93;` |  |
| `{` | `&#123;` |  |
| `}` | `&#125;` |  |
| `|` | `&#124;` |  |
| `-` | `&#8211;` |  |


