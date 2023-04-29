# ***마크 다운( markdown )***

_**마크 다운이란?**_

마크다운(MarkDown)은 산문을 읽고, 쓰고, 편집하기 쉬운 목적으로 만들어진 문서 작성을 위한 형식으로 사용되며 문법이 간결하고 HTML삽입이 가능합니다.
이때 마크다운을 작성한 문서의 표현 방식은 CSS의 설정에 따라 달라집니다. 그래서 본 강좌는 깃헙 마크다운 css 기준으로 진행합니다. 따라서 밸로그 마크다운 프리뷰와 약간의 차이가 있을 수도 있습니다.

 [마크다운 장점 ]

1.문법이 간결하고 쉽다.
 2.마크다운은 모든 것에 사용할 수 있습니다. (웹 사이트, 문서, 메모, 기술 문서 등)
  3.마크다운은 지원하는 플랫폼이 많습니다. ( Github, Discord 등)
   4.마크다운은 대부분의 환경에서 편집, 작성이 가능합니다. (메모장에서도 가능)
    5.텍스트로 저장되기 때문에 용량이 적어 보관이 용이합니다.

[ 마크다운 단점 ]

1.모든 HTML의 문법을 대신하지 못합니다.
 2.표준이 없기 때문에 도구에 따라 변환방식 또는 생성물이 다릅니다.
  3.마크다운으로 파일 업로드하는 경우 저장한 다음 파일 경로를 입력해야되는 불편함
    4.tistory, naver blog, notion과는 다르게 문법들을 하나하나 입력해야되는 경우가 있어 귀찮음이 조금 있습니다.

 


# 1. 마크 다운 언어 문법

+ #으로 시작하는 텍스트.
 + #은 하나부터 여섯개까지 가능.
 + #이 늘어날때마다 제목의 스케일 낮아집니다.
 + H1은 ===로도 만들 수 있습니다.
 + H2는 ---로도 만들 수 있습니다.

  This is an H1
===
This is an H2
---
----------------------  
  # This is an H1
## This is an H2
### This is an H3
#### This is an H4
##### This is an H5
###### This is an H6
---------------------

# 2. Horizontal Rules 수평선
 
* ' -  또는 * 또는  _ 을 3개 이상 작성.'
<br/>
   + ' 단, -을 사용할 경우 header로 인식할 수 있으니 이 전 라인은 비워두어야 합니다. '

* * *
***
*****
- - -
-------------------

**________________________________**
# 3. Line Breaks 줄바꿈
 
* ` <br>를 활용해서 줄바꿈을 할 수 있습니다.`
<br/>
*` 엔터로 칸을 띄면 다음 행으로 넘어가게 됩니다. <br>은 하나의 문장에서 줄바꿈`

Oh my my my oh my my my
You got me high so fast <br>
네 전부를 함께하고 싶어
Oh my my my oh my my my

You got me fly so fast <br>
이제 조금은 나 알겠어

---------------------------------
# 4. Emphasis 강조

* `기울여 쓰기(italic) : * 또는 _로 감싼 텍스트'
   <br>
 '두껍게 쓰기(bold) : ** 또는 __로 감싼 텍스트.'
 <br>
' 취소선 : ~~로 감싼 텍스트." '
<br>
`이탤릭체와 두껍게를 같이 사용할 수 있습니다.`

_This will also be italic_

**This will also be bold**

~~This is canceled~~

_You **can** ~~combine~~ them_

-----------------------------------
# 5. Blockquotes 인용
 
* `>으로 시작하는 텍스트.`
<br/>
  *`>는 3개까지 가능합니다.`

As Grace Hopper said:
> I’ve always been more interested in the future than in the past.    
> This is a first blockquote.
> > This is a second blockquote.
> > > This is a third blockquote.

-------------------------------------
# 6. Lists 목록
 **Unordered lists 순서가 없는 목록**
 `*, +, - 를 이용해서 순서가 없는 목록을 만들 수 있습니다.`
<br>
`들여쓰기를 하면 모양이 바뀝니다.`

* 머리
  * 코
    * 입
      

+ 머리
  + 코
    + 입
      * 입

- 머리
- 코
- 입

----------------------------------
# 7. Ordered lists 순서가 있는 목록
-숫자를 기입하면 순서가 있는 목록이 됩니다.
-들여쓰기를 하면 모양이 바뀝니다.
-숫자를 무엇을 쓰느냐는 그다지 큰 의미가 없고 순서대로 알아서 숫자를 매깁니다

_This will also be italic_

**This will also be bold**

~~This is canceled~~

_You **can** ~~combine~~ them_

----------------------------------
# 8. Emphasis 강조

'기울여 쓰기(italic) : * 또는 _로 감싼 텍스트.'
<br>
'두껍게 쓰기(bold) : ** 또는 __로 감싼 텍스트.'
<br>
`취소선 : ~~로 감싼 텍스트.'
<br>
`이탤릭체와 두껍게를 같이 사용할 수 있습니다.`

_This will also be italic_

**This will also be bold**

~~This is canceled~~

_You **can** ~~combine~~ them_

-------------------------------
# 9. 이미지
* 링크와 비슷하지만 앞에 !가 붙습니다.
* 인라인 이미지 ` ![alt text](/test.png)`
* 링크 이미지 `![alt text](image_URL)`
* 이미지의 사이즈를 변경하기 위해서는 <img width="OOOpx" height="OOOpx"></img>와 같이 표현합니다.
------
`![텍스트](이미지파일경로.jpg)`
`![텍스트](이미지파일URL)`

------
+ 이미지 파일에 마우스를 올렸을 때 커서 옆에 나오는 텍스트 설정

`![텍스트](이미지파일경로.jpg "이미지이름") `
`![텍스트](이미지파일URL "이미지이름")`

------
+ 링크와 이미지를 합친 문법 (이미지를 링크로 사용)

`[ ![텍스트](이미지URL) ]( 링크URL )`

`[![텍스트](https://t1.daumcdn.net/cfile/tistory/2444873B57E257821F)](https://unity3d.com/kr)`

----------------
# 10. Links (Anchor) 링크

` [Google](http://www.google.com "구글")`
<br>
`[Naver](http://www.naver.com "네이버")`
<br>
`[Github](http://www.github.com "깃허브")`



























