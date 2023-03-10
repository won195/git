# 2) Visual Studio Code

## [1] Visual Studio Code 시작하기

### (1) 설치 하기

- [vscode 설치 페이지](https://www.notion.so/5cbdf0943e3640f189a4ee52336dc905)를 참고하여 설치를 진행합니다.

<aside>
💡 **Visual Studio Code 왜 쓰나요?**

- Vscode는 마이크로소프트에서 개발한 코드 에디터의 한 종류입니다.
- Windows, Mac, Linux를 모두 지원합니다.
- 기존 개발 도구들 보다 가볍고 빠르다는 장점이 있습니다.
- 전 세계에서 사랑 받는 굉장한 점유율의 에디터입니다.
- Extension을 통해 다양한 기능을 설치할 수 있어서, 무한한 확장성을 가집니다.
- 게다가 무료로 사용 가능합니다.

</aside>

### (2) vscode 열기

1. 홈 디렉토리(`~`)에서 실습 폴더를 생성 후, 실습 폴더 안에서 vscode를 엽니다.
2. vscode를 열었을 때 다음과 같이 나오는 경우 `Yes, I trust the authors`를 클릭합니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1b86771a-2fbd-4f9d-a6b7-11ecb76222ff/Untitled.png)
    
3. vscode 왼쪽 메뉴바에서 `A4 용지 두 장이 겹쳐져 있는 아이콘`을 클릭합니다.
    
    현재 작업 중인 폴더의 파일/폴더의 목록이 출력됩니다.
    
    ![현재 빈 폴더라서 아무 것도 나오지 않습니다.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7cd86cd5-81e7-42a2-9d75-3d90f24d1ee0/Untitled.png)
    
    현재 빈 폴더라서 아무 것도 나오지 않습니다.
    

## [2] Vscode extensions

### (1) Extensions란?

- `익스텐션`이란 기본 기능에서 확장하여 추가적인 기능을 가능하게 하는 일종의 `플러그인`입니다.
- vscode를 열고 왼쪽 메뉴바에서 `블럭 모양의 아이콘`을 통해 익스텐션 창을 열 수 있습니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a6e43395-d9c7-464b-9582-5c2652e95c2b/Untitled.png)
    

<aside>
💡 **처음부터 모든 기능을 갖추면 되지, 왜 익스텐션을 쓰나요?**

물론, 처음부터 모든 기능을 갖춘다면 일일히 익스텐션을 설치 하지 않아도 될 것입니다.
하지만 그만큼 불필요한 기능도 많아서 필요 이상으로 에디터가 무거워집니다.
vscode는 사용자가 필요한 기능을 익스텐션을 통해 추가 설치 할 수 있도록 지원하여
가벼우면서도 다양한 작업을 할 수 있는 환경을 제공하고 있습니다.

</aside>

### (2) Extensions 설치

1. **한국어 팩** : vscode 기본 언어를 한국어로 변경할 수 있습니다.
    
    설치 이후, vscode를 껐다 켜야 적용됩니다.
    
    ![익스텐션 검색창에 `korean`을 검색한 후, 가장 위에 있는 익스텐션을 install 합니다.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/596ebd69-a56a-4573-bb6a-8ff0cb091ced/Untitled.png)
    
    익스텐션 검색창에 `korean`을 검색한 후, 가장 위에 있는 익스텐션을 install 합니다.
    

1. **Markdown all in one** : 마크다운 문법을 실시간으로 변환해서 보여줍니다.
    
    이후 마크다운 문법 수업 과정에서 사용할 수 있습니다.
    
    ![익스텐션 검색창에 `markdown all in one`을 검색한 후, 가장 위에 있는 익스텐션을 install 합니다.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1b46052d-88a4-45a0-a4d6-d081a9e1416e/Untitled.png)
    
    익스텐션 검색창에 `markdown all in one`을 검색한 후, 가장 위에 있는 익스텐션을 install 합니다.
    

## [3] Vscode 터미널 사용

> 지금까지는 Git Bash 혹은 Terminal과 작업 폴더를 직접 옆에 띄워 놓고 수업을 진행했습니다. 
이제부터는 vscode에서 모든 수업과 실습을 진행합니다.
> 

### (1) 기본 터미널 지정

1. vscode 화면에서 터미널을 엽니다.
    - `vscode 화면 상단 → Terminal → New Terminal`
    - 혹은 단축키 `ctrl + `(backtick, 백틱)` 를 통해 터미널을 열고 닫을 수 있습니다.
        
        ![백틱은 숫자 1의 왼쪽에 있습니다. 물결 표시와 함께!](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7d4b6167-28d5-4b67-9039-37cf5e0f0881/Untitled.png)
        
        백틱은 숫자 1의 왼쪽에 있습니다. 물결 표시와 함께!
        

1. 기본 터미널을 `powershell → Git Bash` 로 바꾸기 (Windows)
    - 현재 Windows는 vscode에서 터미널을 열 때, 기본적으로 Powershell이 설정 되어 있습니다.
    - 아래 사진에 쓰인 숫자 순서대로 클릭합니다. (`아래 화살표 → 기본 프로필 선택`)
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7fa7777c-7939-4360-a2f5-eb9add7cb250/Untitled.png)
        
    - 상단에 나타난 여러 터미널 목록 중 Git Bash를 클릭합니다.
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d68c83d6-4eea-4978-bcdd-5535ba2eabaa/Untitled.png)
        
    - 이후 기존에 떠있는 Powershell을 `휴지통` 버튼을 눌러서 삭제합니다. **(X가 아니라 휴지통)**
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/799ca24c-6d9b-4c42-bf54-dd67b471b252/Untitled.png)
        
    - 그리고 다시 터미널을 열면! Git Bash로 기본 터미널이 설정된 것을 확인할 수 있습니다.
        
        ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c198dd8d-3d65-4b41-ade4-5a71a19fd251/Untitled.png)
        

<aside>
💡 **터미널을 닫을 때 X(닫기)와 휴지통의 차이**

`X(닫기)` 버튼은 터미널의 내용은 유지하고 잠시 숨겨두는 것입니다. (Close panel)
`휴지통` 버튼은 터미널을 아예 삭제하는 것입니다. (Kill terminal)

따라서 가독성을 위해 잠시 닫아 놓을 때는 `X(닫기)` 버튼을,
터미널을 삭제하고 싶을 때는 `휴지통` 버튼을 사용해야 하는 점 잊지 마세요!

</aside>

### (2) vscode에서 터미널 명령어 사용해보기

- CLI 수업에서 학습했던 터미널 명령어를 vscode에서 실습해 봅니다.
- 터미널에서 명령어를 입력했을 때, 왼쪽 파일 트리의 변화를 잘 관찰해 봅니다.
- `예시`

![vscode 터미널에서 작성한 명령어가 파일 트리에 어떤 영향을 끼치는지 살펴봅니다.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6c9c0b5f-e201-4454-a1d6-01cb56d91385/Untitled.png)

vscode 터미널에서 작성한 명령어가 파일 트리에 어떤 영향을 끼치는지 살펴봅니다.