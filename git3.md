# 3) Markdown

## [1] **Markdown all in one** 설정하기

1. 익스텐션 검색창에 `markdown all in one`을 검색한 후, 가장 위에 있는 익스텐션을 install 합니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1b46052d-88a4-45a0-a4d6-d081a9e1416e/Untitled.png)

1. `.md` 확장자 파일을 생성 후, `사이드 뷰`를 활성화합니다.

![스크린샷 2022-07-21 오후 3.41.04.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/4d138018-a7c7-4a44-829e-2a44215bc110/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-07-21_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_3.41.04.png)

1. 최종 모습입니다.

![스크린샷 2022-07-21 오후 3.41.40.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/211cdde5-365b-40b1-8bc4-3ed2036ae7fd/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA_2022-07-21_%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE_3.41.40.png)

## [2] Markdown

### (1) 마크다운이란?

- 일반 텍스트 기반의 경량 마크업(Markup) 언어
- 마크업과 반대 개념이 아니라, 마크업을 더 쉽고 간단하게 사용하고자 만들어졌습니다.
- `.md` 확장자를 가지며, 개발과 관련된 많은 문서는 마크다운 형식으로 작성되어 있습니다.
- 개발 분야에 있어서 `문서화`는 굉장히 중요한 능력입니다. 마크다운은 그 토대가 될 것입니다.

<aside>
💡 **마크업(Markup)이란 무엇인가요?**

마크업 언어는 말 그대로 마크(Mark)로 둘러싸인 언어입니다.
여기서 마크(Mark)란 글의 역할을 지정하는 일종의 표시와 같습니다.

예를 들면 HTML에서 M이 의미하는 것은 Markup 입니다. 즉 HTML도 마크업 언어입니다.
HTML에서 제목을 표시할 때는 `<h1>제목1</h1>` 과 같이 작성합니다.
`제목1`을 둘러싸고 있는 `<h1>`을 태그(tag)라고 말하며, 마크 역할을 합니다.
각각의 글이 `제목, 내용, 목록, 인용 등등` 어떤 역할을 가지고 있는지 표시하는 것입니다.

</aside>

### (2) 마크다운의 장점, 단점, 주의사항

1. **장점**
    - 문법이 직관적이고 쉽습니다.
    - 관리가 쉽습니다.
    - 지원 가능한 플랫폼과 프로그램이 다양합니다.
2. **단점**
    - 표준이 없어 사용자마다 문법이 상이할 수 있습니다.
    - 모든 HTML 마크업 기능을 대신하지는 못합니다.
3. **주의사항**
    - 마크다운의 본질은 글에게 `역할`을 부여하는 것입니다.
    - 따라서 반드시 `역할`에 맞는 마크다운 문법으로만 작성해야 합니다.
    - 예를 들면 `글씨의 크기를 키우고 싶다`는 이유로 `내용`에게 `제목`의 역할을 부여하면 안됩니다. (이 부분은 마크다운 문법을 학습하면서 자연스럽게 이해할 수 있습니다.)

### (3) 마크다운 문법

1. **제목 (Headings)**
    - `h1 ~ h6` 에 해당하는 제목을 표현합니다.
    - `#`을 사용합니다.
    - 작성
        
        ```markdown
        # 제목 1
        ## 제목 2
        ### 제목 3
        #### 제목 4
        ##### 제목 5
        ###### 제목 6
        ```
        
    - 결과
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b1534e2b-b67f-47d0-b966-76b3f50d09ad/Untitled.png)
        

1. **목록 (List)**
    - 순서가 없는 목록과 순서가 있는 목록을 표현합니다.
    - 순서가 없는 목록은 `- * +` 를 사용합니다.
    - 순서가 있는 목록은 `1. 2. 3.` 과 같은 숫자를 사용합니다.
    - `tab 키`를 이용해서 들여쓰기를 할 수 있습니다.
    - 작성
        
        ```markdown
        - 순서가 없는 목록
        	- 서브 목록
        	- 서브 목록
        
        + 순서가 없는 목록
        	+ 서브 목록
        	+ 서브 목록
        
        * 순서가 없는 목록
        	* 서브 목록
        	* 서브 목록
        
        1. 순서가 있는 목록
        	1. 서브 목록
        	2. 서브 목록
        
        1. 혼합 해보기 1
        	- 순서 없음
        	+ 순서 없음
        	* 순서 없음
        2. 혼합 해보기 2
        	1. 순서 있음
        	- 순서 없음
        	2. 순서 있음
        ```
        
    - 결과
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/00bafa7d-6880-4280-a763-e65d1c6356ca/Untitled.png)
        

1. **강조 (Emphasis)**
    - 글자의 스타일링을 표현합니다.
    1. **기울임** : `*글자*` 혹은 `_글자_`
    2. **굵게** : `**글자**` 혹은 `__글자__`
    3. **취소** : `~~글자~~`
    - 작성
        
        ```markdown
        *이탤릭체1* 
        _이탤릭체2_
        
        **볼드체1**
        __볼드체2__
        
        ~~취소선~~
        ```
        
    - 결과
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/77e83882-4710-4bcd-a010-8b2e88cfb543/Untitled.png)
        

1. **코드 (Code)**
    - 한 줄 코드인 **인라인 코드**와 여러 줄 코드인 **블록 코드**로 나눌 수 있습니다.
    1. 인라인(Inline) 코드 : ``inline code``처럼 백틱을 통해 코드를 감싸줍니다.
    2. 블록(Block) 코드 : ````python` 처럼 백틱을 3번 입력하고 코드의 종류를 작성합니다.
    - 작성
        
        ```markdown
        파이썬의 print는 `print("Hello World!")` 과 같이 사용합니다.
        
        ```python
        for i in range(10):
        	print(i)
        ```
        
        ```bash
        $ touch test.txt
        ```
        
        ```
        Just plain text
        ```
        ```
        
    - 결과
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9ced236f-5816-41e3-8cd4-677b171bea30/Untitled.png)
        

1. **링크 (Links)**
    - 클릭하면 해당 주소로 이동할 수 있는 링크를 표현합니다.
    - `[표시할 글자](이동할 주소)` 형태로 작성합니다.
    - 작성
        
        ```markdown
        [GOOGLE](https://google.com)을 눌러서 구글로 이동하세요.
        ```
        
    - 결과
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a9050d59-f33b-4e58-a72e-b0c7ac035c79/Untitled.png)
        

1. **이미지 (Images)**
    - 마크다운 문서에 이미지를 삽입할 수 있습니다.
    - `![대체 텍스트](이미지 주소)` 형태로 작성합니다.
    - `대체 텍스트`란 이미지를 정상적으로 불러오지 못했을 때 표시되는 문구입니다.
    - Typora에서는 이미지 파일을 끌어와서 놓아도 자동 업로드 됩니다.
    - 작성
        
        ```markdown
        Git 로고입니다.
        
        ![Git로고](https://git-scm.com/images/logo@2x.png)
        ```
        
    - 결과
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/db013257-c43f-49e6-a8f4-4ae8b915a198/Untitled.png)
        

1. **인용 (Blockquote)**
    - 주석이나 인용 문구를 표현합니다.
    - `>` 를 사용합니다. 갯수에 따라 중첩이 가능합니다.
    - 작성
        
        ```markdown
        > 인용문을 작성합니다.
        >> 중첩된 인용문 1
        >>> 중첩된 인용문 2
        >>>> 중첩된 인용문 3
        >>>>> 중첩된 인용문 4
        ```
        
    - 결과
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/ae65cfd3-5a2d-49f9-bb6f-45ee987dda66/Untitled.png)
        

1. **표 (Table)**
    - 테이블(표)를 생성합니다.
    - `파이프( | )`와 `하이픈( - )`을 이용해서 행과 열을 구분합니다.
    - 테이블 양쪽 끝의 `파이프( | )`는 생략 가능합니다.
    - 헤더 셀을 구분할 때는 `3개 이상의 하이픈( - )`이 필요합니다.
    - Typora에서는 `ctrl + T` 를 통해서 쉽게 표 생성이 가능합니다.
        
        (Mac은 `option + command + t`)
        
    - 행을 늘릴 때는 `ctrl + enter` 를 누릅니다.
    - 작성
        
        ```markdown
        | 동물   | 종류   | 다리 개수 |
        | ------ | ------ | --------- |
        | 사자   | 포유류 | 4개       |
        | 닭     | 조류   | 2개       |
        | 도마뱀 | 파충류 | 4개       |
        ```
        
    - 결과
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1b8821a7-034a-4d07-a33c-6712c801d0a8/Untitled.png)
        

1. **수평선 (Horizontal Rule)**
    - 구분 선을 생성합니다.
    - `- * _` 을 3번 이상 연속으로 작성합니다.
    - 작성
        
        ```markdown
        ---
        ***
        ___
        ```
        
    - 결과
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5eaf7db0-394b-406a-ae1c-c4ebdf52b905/Untitled.png)
        

## [3] 실습

### TIL(Today I Learned) 작성하기

<aside>
💡 TIL은 무엇인가요?
**Today I Learn 의 약어**로 오늘 내가 배운 내용을 마크다운 문서로 기록하는 것입니다.

일일 일커밋, 오늘 배운 것들을 기록하고 정리하며 장기 기억력으로 전환하기 위한 용도로 사용되며, 꾸준함을 습관화할 수 있습니다.

현재까지 배운 것을 마크다운 문법을 활용하여 정리해 봅니다. 

</aside>

1. `TIL_Day_01.md`를 `TIL_Day_01_정답.md`와 동일하게 만들어보며 마크다운을 연습합니다.
    - TIL이라는 폴더를 새로 만들고 그 안에 아래 파일을 저장합니다.
    
    [TIL_Day_01.md](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/613c3b91-3d98-4419-8892-267c7a8f151f/TIL실습_문제.md)
    
    [TIL_Day_01_정답.md](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/dea54047-0eff-41a9-bb32-98994c7b70f5/TIL실습_정답.md)
    

1. 정답화면 미리보기
    - 아래 링크에 나와 있는 것과 똑같이 만들어봅니다.
    
    [GitHub - educhelsea/Markdown-example: TIL 1일차 실습 정답](https://github.com/educhelsea/Markdown-example)
    

1. 오늘부터 매일매일 꾸준하게 배운 내용을 기록합니다.
    - **TIL 모범 예시**
        
        ![출처 : [https://github.com/cheese10yun/TIL](https://github.com/cheese10yun/TIL)](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b586771c-1e5b-4962-a3d4-6e01361aa6b1/Untitled.png)
        
        출처 : [https://github.com/cheese10yun/TIL](https://github.com/cheese10yun/TIL)
        
    - **TIL 모범 예시**
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c932fe1a-3f47-4466-b01f-efa0271fb187/Untitled.png)
        
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e0e6f304-b93e-4786-aa96-a869f2a0f690/Untitled.png)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7e18063e-bbfa-4ca9-a08f-5163c2822146/Untitled.png)
    
    1. 아래 TIL 모범 사례를 보면서, 자기만의 TIL을 완성할 수 있도록 내용을 추가합니다.
    - [https://github.com/Gyubin/TIL](https://github.com/Gyubin/TIL)
    - [https://github.com/cheese10yun/TIL](https://github.com/cheese10yun/TIL)
    - [https://github.com/Integerous/TIL](https://github.com/Integerous/TIL)

배우지 않은 요소가 있더라도, 강의 자료나 인터넷 검색을 통해 해결하는 능력을 기릅니다.
아래 내용도 참고해 봅니다.

[Basic Syntax | Markdown Guide](https://www.markdownguide.org/basic-syntax/)

[마크다운(Markdown) 사용법](https://gist.github.com/ihoneymon/652be052a0727ad59601)