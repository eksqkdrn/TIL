hyper : 컴퓨터 용어로써 텍스트 등의 정보가 동일 선상에 있는 것이 아닌 다중으로 연결돼있는 상태

사용자들은 텍스트와 문서들의 고정관념인 것에서 벗어나 사용자가 원하는 대로 읽을 수 있도록 함. 즉, 한 텍스트에서 다른 텍스트로 건너뛸 수 있게 하는 것

```html
<!DOCTYPE html>
<html>
  <body>
    <a href="http://www.google.com">Visit google.com!</a>
  </body>
</html>
```

## A태그

하이퍼링크를 걸어주는 태그

HREF

이동하려고 하는 파일의 위치(경로)를 값으로 받음

경로는 파일 시스템에서 특정 파일의 위치를 의미함

## 디렉터리 Directory (폴더)

- 루트 디렉터리 - 파일 시스템 구조 최상위

       window : C:\

- 홈 디렉터리 - 사용자에게 각각 할당됨

       window : C:\Users\{계정명}

- 작업 디렉터리 - 작업 중인 파일에 위치함

       ./

- 부모 디렉터리 - 작업 디렉터리의 부모

       ../

## 파일 경로 File Path

파일 시스템에서 파일의 위치를 나타내는 방법

### 절대경로

현재 작업 중인 디렉터리와 상관없이 특정 파일의 절대적 위치를 가리킴

루트 디렉터리를 기준으로 파일의 위치를 나타냄

- http://www.mysite.com/index.html
- /Users/leeungmo/Desktop/myImage.jpg
- C:\users\leeungmo\Desktop\myImage.jpg
- /index.html

### 상대경로

현재 디렉터리를 기분으로 특정 파일의 상대적 위치를 가리킴

- ./index.html
- ../dist/index.js
- ../../dist/index.js
- index.html
- html/index.html

herc 속성에 사용 가능한 값

| Value               | Description                                                    |
| ------------------- | -------------------------------------------------------------- |
| 절대 URL            | 웹사이트 URL (href=”http://www.example.com/default.html”)      |
| 상대 URL            | 자신의 위치를 기준으로한 대상의 URL (href=”html/default.html”) |
| fragment identifier | 페이지 내의 특정 id를 갖는 요소에의 링크 (href=”#top”)         |
| 메일                | mailto:                                                        |
| script              | href=”javascript:alert(‘Hello’);”                              |

```html
<!DOCTYPE html>
<html>
  <body>
    <a href="http://www.google.com">URL</a><br />
    <a href="html/my.html">Local file</a><br />
    <a href="file/my.pdf" download>Download file</a><br />
    <a href="#">fragment identifier</a><br />
    <a href="mailto:someone@example.com?Subject=Hello again">Send Mail</a><br />
    <a href="javascript:alert('Hello');">Javascript</a>
  </body>
</html>
```

페이지 내부 이동 방법

```html
<!DOCTYPE html>
<html>
  <body>
    <h2 id="top">Top of page!</h2>

    <p>
      In my younger and more vulnerable years my father gave me some advice that I've been turning over in my mind ever
      since.
    </p>
    <p>
      "Whenever you feel like criticizing any one," he told me, "just remember that all the people in this world haven't
      had the advantages that you've had."
    </p>
    <p>
      He didn't say any more, but we've always been unusually communicative in a reserved way, and I understood that he
      meant a great deal more than that. In consequence, I'm inclined to reserve all judgments, a habit that has opened
      up many curious natures to me and also made me the victim of not a few veteran bores. The abnormal mind is quick
      to detect and attach itself to this quality when it appears in a normal person, and so it came about that in
      college I was unjustly accused of being a politician, because I was privy to the secret griefs of wild, unknown
      men. Most of the confidences were unsought-frequently I have feigned sleep, preoccupation, or a hostile levity
      when I realized by some unmistakable sign that an intimate revelation was quivering on the horizon; for the
      intimate revelations of young men, or at least the terms in which they express them, are usually plagiaristic and
      marred by obvious suppressions. Reserving judgments is a matter of infinite hope. I am still a little afraid of
      missing something if I forget that, as my father snobbishly suggested, and I snobbishly repeat, a sense of the
      fundamental decencies is parcelled out unequally at birth.
    </p>
    <p>
      And, after boasting this way of my tolerance, I come to the admission that it has a limit. Conduct may be founded
      on the hard rock or the wet marshes, but after a certain point I don't care what it's founded on. When I came back
      from the East last autumn I felt that I wanted the world to be in uniform and at a sort of moral attention
      forever; I wanted no more riotous excursions with privileged glimpses into the human heart. Only Gatsby, the man
      who gives his name to this book, was exempt from my reaction-Gatsby, who represented everything for which I have
      an unaffected scorn. If personality is an unbroken series of successful gestures, then there was something
      gorgeous about him, some heightened sensitivity to the promises of life, as if he were related to one of those
      intricate machines that register earthquakes ten thousand miles away. This responsiveness had nothing to do with
      that flabby impressionability which is dignified under the name of the "creative temperament"-it was an
      extraordinary gift for hope, a romantic readiness such as I have never found in any other person and which it is
      not likely I shall ever find again. No-Gatsby turned out all right at the end; it is what preyed on Gatsby, what
      foul dust floated in the wake of his dreams that temporarily closed out my interest in the abortive sorrows and
      short-winded elations of men.
    </p>

    <a href="#top">Go to top</a>
  </body>
</html>
```

## A태그

하이퍼링크를 걸어주는 태그

### HREF

이동하려고 하는 파일의 위치(경로)를 값으로 받음

경로는 파일 시스템에서 특정 파일의 위치를 의미함

### TARGET

target 속성은 hyper link를 클릭했을 때 어떤 방식으로 창을 열지 지정

| Value        | Description                                                     |
| ------------ | --------------------------------------------------------------- |
| `_self`      | 링크를 클릭했을 때 연결문서를 현재 윈도우에서 오픈한다 (기본값) |
| `_blank`     | 링크를 클릭했을 때 연결문서를 새로운 윈도우나 탭에서 오픈한다   |
| `_parent`    | 부모 페이지로, iframe 등이 사용된 환경에서 쓰임                 |
| `_top`       | 최상위 페이지로, iframe 등이 사용된 환경에서 쓰임               |
| `프레임이름` | 프레임이름을 직접 명시해서 사용할 수 있음                       |

```html
<!DOCTYPE html>
<html>
  <body>
    <a href="http://www.google.com" target="_blank" rel="noopener noreferrer">Visit google.com!</a>
  </body>
</html>
```
