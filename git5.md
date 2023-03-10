# 5) Github

---

## [1] 원격 저장소 (Remote Repository)

> 여태 까지는 내 컴퓨터라는 한정된 공간에 있는 로컬 저장소에서만 버전 관리를 진행했습니다.
이제는 Github의 원격 저장소를 이용해 내 컴퓨터의 로컬 저장소를 다른 사람과 `공유`해봅시다.
Git의 주요 목적 중 하나인 `협업`을 위해 로컬 저장소와 원격 저장소의 연동 방법을 학습합니다.
> 

### (1) Github에서 원격 저장소 생성

![화면 오른쪽 상단 더하기(+) 버튼을 누르고 New repository를 클릭합니다.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/55e28914-796f-487f-9ce1-972cf15cc1d1/그림3.png)

화면 오른쪽 상단 더하기(+) 버튼을 누르고 New repository를 클릭합니다.

![저장소의 이름, 설명, 공개 여부를 선택하고 Create repository를 클릭합니다. (체크 박스는 건드리지 않습니다!)](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/40d4c341-35df-4cf7-8586-83afe060d56c/그림4.png)

저장소의 이름, 설명, 공개 여부를 선택하고 Create repository를 클릭합니다. (체크 박스는 건드리지 않습니다!)

### (2) 로컬 저장소와 원격 저장소 연결

1. 원격 저장소가 잘 생성되었는지 확인 후, 저장소의 주소를 복사합니다.
    
    ![그림5.png](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/798d21e0-9c40-4995-b5ed-fc77b9e75bb1/그림5.png)
    
2. 기존에 실습 때 만들었던 홈 디렉토리의 TIL 폴더로 가서 vscode를 엽니다.

1. git init을 통해 TIL 폴더를 로컬 저장소로 만들어줍니다.
    
    ```bash
    kyle@KYLE MINGW64 ~/TIL
    $ git init
    Initialized empty Git repository in C:/Users/kyle/TIL/.git/
    ```
    

1. **git remote**
    
    로컬 저장소에 원격 저장소를 `등록, 조회, 삭제`할 수 있는 명령어
    
    1. **등록**
        
        `git remote add <이름> <주소>` 형식으로 작성합니다.
        
        ```bash
        $ git remote add origin https://github.com/edukyle/TIL.git
        
        [풀이]
        git 명령어를 작성할건데, remote(원격 저장소)에 add(추가) 한다.
        origin이라는 이름으로 https://github.com/edukyle/TIL.git라는 주소의 원격 저장소를
        ```
        
    2. **조회**
        
        `git remote -v` 로 작성합니다.
        
        ```bash
        $ git remote -v
        origin  https://github.com/edukyle/TIL.git (fetch)
        origin  https://github.com/edukyle/TIL.git (push)
        
        add를 이용해 추가했던 원격 저장소의 이름과 주소가 출력됩니다.
        ```
        
    3. **삭제**
        
        `git remote rm <이름>` 혹은 `git remote remove <이름>` 으로 작성합니다.
        
        > 로컬과 원격 저장소의 연결을 끊는 것이지, 원격 저장소 자체를 삭제하는 게 아닙니다.
        > 
        
        ```bash
        $ git remote rm origin
        $ git remote remove origin
        
        [풀이]
        git 명령어를 작성할건데, remote(원격 저장소)와의 연결을 rm(remove, 삭제) 한다.
        그 원격 저장소의 이름은 origin이다.
        ```
        

### (3) 원격 저장소에 업로드

- 실습 때 작성했던 TIL 파일을 Github 원격 저장소에 업로드 해보겠습니다.
- **정확히 말하면, 파일을 업로드하는 게 아니라 커밋을 업로드 하는 것입니다!**
- 따라서 먼저 로컬 저장소에서 커밋을 생성해야 원격 저장소에 업로드 할 수 있습니다.

1. **로컬 저장소에서 커밋 생성**
    
    ```bash
    # 현재 상태 확인
    
    $ git status
    On branch master
    
    No commits yet
    
    Untracked files:
      (use "git add <file>..." to include in what will be committed)
            day1.md
    
    nothing added to commit but untracked files present (use "git add" to track)
    ```
    
    ```bash
    $ git add day1.md
    ```
    
    ```bash
    $ git commit -m "Upload TIL Day1"
    [master (root-commit) f3d6d42] Upload TIL Day1
     1 file changed, 0 insertions(+), 0 deletions(-)
     create mode 100644 day1.md
    ```
    
    ```bash
    # 커밋 확인
    
    $ git log --oneline
    f3d6d42 (HEAD -> master) Upload TIL Day1
    ```
    

1. **git push**
    - 로컬 저장소의 커밋을 원격 저장소에 업로드하는 명령어
    - `git push <저장소 이름> <브랜치 이름>` 형식으로 작성합니다.
    - `-u` 옵션을 사용하면, 두 번째 커밋부터는 `저장소 이름, 브랜치 이름`을 생략 가능합니다.
    
    ```bash
    $ git push origin master
    
    [풀이]
    git 명령어를 사용할건데, origin이라는 이름의 원격 저장소의 master 브랜치에 push 한다.
    
    ------------------------------------------------
    
    $ git push -u origin master
    이후에는 $ git push 라고만 작성해도 push가 됩니다.
    ```
    

1. **vscode 자격 증명**
    
    ![Sign in with your browser를 클릭합니다.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b28d0353-708a-43eb-9e97-8cc67d03fd4f/Untitled.png)
    
    Sign in with your browser를 클릭합니다.
    
    ![Authorize GitCredentialManager를 클릭합니다.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6dfe2042-1157-45fb-a444-3ce992a9b7fd/Untitled.png)
    
    Authorize GitCredentialManager를 클릭합니다.
    
    ![정상적으로 자격 증명이 완료 되었습니다.](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fd24bd5f-4b46-4618-bb90-4ab5e90cdd3e/Untitled.png)
    
    정상적으로 자격 증명이 완료 되었습니다.
    
    이후 git push 완료
    
    ```bash
    $ git push -u origin master
    info: please complete authentication in your browser...
    Enumerating objects: 3, done.
    Counting objects: 100% (3/3), done.
    Writing objects: 100% (3/3), 218 bytes | 218.00 KiB/s, done.
    Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
    To https://github.com/edukyle/TIL.git
     * [new branch]      master -> master
    Branch 'master' set up to track remote branch 'master' from 'origin'.
    ```
    
2. **원격 저장소에서 정상 업로드 확인**
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6d5698c4-ea50-4e47-a766-feebbd5b7a3a/Untitled.png)
    

<aside>
❗ **(주의) Github 원격 저장소에 절대로 파일을 드래그해서 업로드 하지 않습니다!!!!**

가끔 Github를 구글 드라이브처럼 여겨서, 파일을 직접 드래그해서 올리는 경우가 있습니다.
Git 명령어를 학습했기 때문에, 반드시 git add → git commit → git push 의 단계로만
업로드 해야합니다.

그 이유는 로컬 저장소와 원격 저장소의 동기화 때문입니다.
로컬 저장소에서 변경이 먼저 일어나고, 그 변경 사항을 원격 저장소에 반영하는 형태여야 합니다. 하지만, Github에 드래그를 해서 파일을 업로드하면 원격 저장소에 변경이 먼저 일어나는 형태가 되기 때문에 이러한 행동을 지양해야 합니다.

</aside>


## [2] 실습

### (1) README.md 파일 push 해보기

- `README.md`는 원격 저장소의 소개와 설명이 담겨있는 일종의 대문 역할을 합니다.
- 반드시 파일 이름을 `README.md`로 지정해야 Github가 인식할 수 있습니다.
- 홈 디렉토리에 있는 TIL 폴더에 `README.md` 파일을 생성하고, 자유롭게 `설명, 각오, 분류 등`을 마크다운 문법으로 작성하고 자신의 Github TIL 원격 저장소에 push를 해봅니다.
- 예시