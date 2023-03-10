# 11) Git workflow 실습

## [1] Pull Request (PR) 자세히 알아보기

> Github 화면을 통해 Pull Request 과정을 자세히 알아봅니다.
> 

1. 브랜치를 Push 하면 `Compare & pull request` 라는 알림 버튼이 나타나는데, 이를 누르면 됩니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8e93888e-c19b-4c07-ac2e-d58e03ee7e1d/Untitled.png)
    
2. 혹은 원격 저장소 상단 바에서 `Pull requests → New pull request`을 통해서도 가능합니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cd42e34a-aae5-42ff-95cb-efa5226e2eb9/Untitled.png)
    

1. `base`는 병합될 대상입니다. `master를 base로` 두면 됩니다.
`compare`는 병합할 대상입니다. 우리가 만든 `feature/login 브랜치를 compare로` 두면 됩니다.
그리고 아래쪽에서 비교 내용을 확인하고 `Create pull request`를 클릭합니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/16d746e2-6f1d-4272-912f-ccfe7f4580f3/Untitled.png)
    

1. Pull Request에 대한 제목과 내용, 각종 담당자를 지정하는 페이지가 나옵니다.
모두 작성했다면 `Create pull request`를 눌러서 PR을 생성합니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/fed29aad-7ec5-4f93-8afd-684afc195e65/Untitled.png)
    
    `Reviewers` : 현재 PR에 대해 코드 리뷰를 진행해 줄 담당자
    
    `Assignees` : 현재 PR에 대한 작업을 맡고 있는 담당자
    
2. PR이 생성되면 다음과 같은 화면이 나타납니다. 빨간 표시가 된 세 부분을 살펴보겠습니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/e2ba1dd2-57ff-40f4-9f58-1053f1c00ccc/Untitled.png)
    
3. `Conversation` : 아래 Write 부분에서 comment를 별도로 작성할 수도 있습니다. 그리고 `Merge pull request` 버튼을 누르면 병합이 시작됩니다. (충돌(conflict) 상황에서는 충돌을 해결하라고 나옵니다.)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0e1a6f87-17b2-4c79-8ab6-879b1891aa8e/Untitled.png)
    
4. `Commits` : PR을 통해 반영될 커밋들을 볼 수 있습니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/3c37c888-187a-47c2-b945-94fb440f6a88/Untitled.png)
    
5. `Files changed` : 파일의 변화 내역들을 볼 수 있습니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/9ac9ad6e-63e9-431c-8757-a92778b169a2/Untitled.png)
    
6. 코드리뷰를 원하는 라인에서 `+` 를 눌러서 해당 라인에 리뷰를 남길 수 있습니다.
    
    빨간 사각형으로 표시된 작은 아이콘을 클릭하면, 
    **`suggestion 기능`(코드를 이렇게 바꾸라고 추천하는 기능)**을 넣을 수도 있습니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1cd52944-6941-4302-b520-c54eac4f2447/Untitled.png)
    
7. 코드 리뷰를 끝내려면 `Finish your review` 버튼을 누르면 됩니다. 
그리고 옵션을 선택하고 `Submit review`를 클릭합니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c69d4afa-c6df-4b42-8226-cb51c2f45ef0/Untitled.png)
    
    - `Comment`: 추가적인 comment를 작성할 경우 선택
    - `Approve`: merge를 승인하는 경우 선택
    - `Request change` : 수정해야 하는 사항이 있을 경우 선택

1. 다시 conversation으로 가보면 진행했던 리뷰가 이렇게 나타난 것을 확인할 수 있습니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/efb77ecb-305a-472d-9414-ece0ec9192b8/Untitled.png)
    

1. 병합을 하게 되면 아래와 같이 보라색으로 병합이 완료되었다고 나오면 성공입니다.
    
    `Delete branch` 버튼을 통해 병합된 `feature/login` 브랜치를 지울 수 있습니다. 
    (원격 저장소에서만 지워집니다.)
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/311953ae-acc1-4393-9f28-c724efc92aee/Untitled.png)
    
2. `master`를 확인해보면 `feature/login`의 내용이 master에 병합된 것을 확인할 수 있습니다.
    
    ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0c856336-d306-4e59-bc39-6d60d5a390de/Untitled.png)
    
3. 이후 로컬 저장소의 master 브랜치에서 `git pull`을 이용해 로컬과 원격을 동기화 합니다.

## [2] Pull Request 실습 - N행시 짓기

> 소유권이 없는 상태에서의 협업하는 방법(fork 와 pull request)에 대해 익혀 봅시다.
> 
1. 강사의 깃허브에 있는 `acrostic-poem` repository를 fork합니다.
2. 교육생은 fork 한 자신의 repository를 `clone`하여 자신의 local에 복제합니다.
3. `교육생 이름`으로 된 브랜치를 생성하고, 주어진 명제에 따라 N행시를 작성합니다.
4. 작성을 완료한 결과물에 대해 커밋 후 `push` 합니다.
    - master 브랜치가 아닌, 자신 이름으로 된 브랜치로 push 해야 합니다.
    - 강사의 repository가 아닌, fork 한 자신의 repository로 push 해야 합니다.
5. 깃허브에서 강사의 repository에 `Pull Request` 를 보내 봅시다.
    
    <aside>
    ⚠️ **교육생 repository의 자신 이름 브랜치 → 강사 repository의 master 브랜치**
    이대로 설정해서 Pull Request 보내야 합니다!
    
    </aside>
    
6. 이후 아래처럼 강사의 repository의 Pull Request 목록에서 자신의 요청을 찾아봅니다.
    
    ![Pull Request 목록 예시](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/edd7b74d-1c37-4808-9a81-391d9ccd3443/Untitled.png)
    
    Pull Request 목록 예시
    
    ![Files changed 란에서 요청한 PR의 내용 살펴보기](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c5fe9177-e4db-4015-9eaf-99e45b3cef73/Untitled.png)
    
    Files changed 란에서 요청한 PR의 내용 살펴보기
    

<aside>
📌 **요약**

`fork`→`clone`→브랜치 생성→ `add` → `commit` → 브랜치 `push` → `pull request` 보내기

</aside>