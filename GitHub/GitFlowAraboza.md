# Git Flow에 대해 Araboza..

협업 시 유용한 전략인 Git Flow에 대해 알아봅시다! 여러분이 앱잼에 참여한다면.. 분명 도움이 많이 되는 지식일 거에요..!:smiley:

<br>

### 1. Git-Flow란? :jack_o_lantern:

`git`을 통해 효율적으로 **프로젝트를 관리하고 배포하기 위한 전략**이 바로 Git-Flow 전략입니다. 간단히 말하자면 **브랜치 관리 전략**입니다. 프로젝트의 규모가 커지고 협업하는 동료가 많아진다면 저장소의 `master branch`만을 이용해서 프로젝트를 진행하는 데는 무리가 있겠죠?(~~화려한 merge conflict가 나를 감싸네..~~ ) 다양한 branch를 통해 다양한 인원이 독립적으로 개발이 가능한 전략이 바로 Git Flow 전략입니다.

<img src="https://about.gitlab.com/images/git_flow/gitdashflow.png" alt="git_flow" style="zoom: 67%;" />

<br>

### 2. 브랜치 전략 :cherry_blossom:

Git-Flow에는 대표적으로 버전의 갱신이 이루어지는`master branch`와 대부분의 변경사항이 출발하는 `develop branch`가 있습니다. 그 외에, `develop branch`에서 생성되어 세부적인 기능이 개발 되는 `feature branch`, 버그를 수정하는 `hotfix branch` 등의 브랜치들도 존재합니다.



<table class="tg">
<tbody>
    <tr>
        <td>master branch</td>
        <td>develop branch</td>
    </tr>
    <tr>
        <td><img src="https://camo.githubusercontent.com/70f7e458a965f38831d1c50757b3a284c4280328/687474703a2f2f646f67666565742e6769746875622e696f2f61727469636c65732f323031312f612d7375636365737366756c2d6769742d6272616e6368696e672d6d6f64656c2f6d61696e2d6272616e636865732e706e67" width="200px"/></td>
        <td><img src="https://camo.githubusercontent.com/c9cbf25c64dc0519860230cb98d098c3d069eda3/687474703a2f2f646f67666565742e6769746875622e696f2f61727469636c65732f323031312f612d7375636365737366756c2d6769742d6272616e6368696e672d6d6f64656c2f6d657267652d776974686f75742d66662e706e67"  width="300px"/></td>
    </tr>
</tbody>
</table>



<br>

#### :bulb:그런데 솔직히...!

위에 말들이 개념적인 말들만 가득해서 솔직히 이해가 어렵잖아요..:eyes: 그런 여러분들을 위해​ 밑에서부터는 아주아주아주..! 간단하게 설명해 드리겠습니다..!

- **Git Flow 어렵지 않아요! 밑 과정을 통해 Git Flow는 이뤄져요! :smile:**

  **:one: 첫 Repo생성과 동시에 생성 되는 branch! : master branch**

  **:two: master branch에서 branch를 하나 파고 거기서 다른 개발 branch들을 생성한다! : develop branch**

  **:three: develop branch에서 새로운 기능 개발을 위해 만들어진 branch! : feature branch**

  **:four: feature branch에서 기능 개발이 완료되었으면 develop branch에 merge합니다!**

  **:five: 갑자기 버그가 생겼다! develop branch(또는 master branch)에서 버그를 해결하기 위해 만드는 branch! : hotfix branch**

  **:six: 어느 정도 기능 개발이 완료되어 develop branch에 완성된 제품이 생겼으면 master branch에 merge합니다!**

  <br>

- **아직도 어렵다구요?**

  그런 당신을 위해 제가 이번 겨울 진행했던 프로젝트 포모스트에서 사용한 Git Flow전략을 보여드릴게요! :smile:

<br>

### 3. Git Flow 이용 사례 :seedling:

##### :star: develop branch

<img src="/Image/img_develop_branch.png" alt="img_develop_branch" style="zoom:33%;" />

- 현재 보이는 사진의 branch가 develop 브랜치입니다. 이 branch에 팀원들이 각자 feature branch에서 작업한 내용물들이 나중에 합쳐지게 됩니다!

  <br>

##### :star: feature branch(+hotfix branch)

<img src="/Image/img_feature_branch.png" alt="img_feature_branch" style="zoom:33%;" />

- 새로운 기능을 개발할 때는 feature branch를, 버그를 수정할 때는 hotfix branch를 각각 develop branch에서 생성해줍니다.
- 저희가 협업 시 local에서 코드를 짜게 되는 branch는 이러한 feature, 또는 hotfix branch입니다!(나중에 여기서 작업한 결과물을 pull request를 통해 develop branch에 합쳐줄거에요)
- **절.대.로 develop이나 master branch에서 작업한 후 외부 저장소에 push하시면 안됩니다!!(다른 팀원들이 작업해놓은 결과물들이 다 날라갈 수 있어요 ☹️)**

<br>

##### :star: Issues

<img src="/Image/img_issue.png" alt="img_issue" style="zoom:33%;" />

- branch를 생성하고 바로 작업에 들어가도 되겠지만.. 기왕이면 팀원들이 현재 제가 뭘하고 있는 지 파악할 수 있으면 더 좋겠죠? 그럴 때 필요한 게 바로 `Issues` 기능이에요!
- 저희 포모스트 팀에서는 작업에 들어가기 전에 Issue를 하나 생성한 후, Issue에 무엇을 작업할 것인지 간략히 작성한 후 branch를 파고 작업을 시작했습니다 :) (눈치 채신분들도 있겠지만 포모스트팀의 feature branch 이름에 붙은 숫자는 이슈 넘버(#붙은 번호)입니다.)
- Issue는 Issue와 관련된 pull request와 연동시켜, pull request가 완료되었을 때 자동적으로 close되게 할 수 있습니다.
- 아래 사진은 제가 팀에서 Issue를 직접 써 본 사진이에요!

<img src="/Image/img_issue_detail.png" alt="img_issue_detail" style="zoom: 33%;" />

<br>

##### :star: Pull request

:one:

<img src="/Image/img_pull_request.png" alt="img_pull_request" style="zoom:33%;" />

:two:

<img src="/Image/img_pull_request2.png" alt="img_pull_request2" style="zoom:33%;" />

- 이제 feature branch(hotfix branch)에서 어느정도 작업이 완료되었다싶으면 pull request를 할 수 있습니다.
- pull request란 현재 제가 작업한 feature branch(위 사진에서는 hotfix/93-remind-and-report)를 다른 branch(위 사진에서는 develop)에 merge할 것을 요청하는 작업입니다.
- Git-Flow 전략에서는 바로 이 pull request기능을 통해, develop이나 master branch에 합병하는 작업을 하게됩니다.
- merge가 가능하다면 위 사진과 같이 **Create pull request** 버튼이 활성화 되는데, 저 버튼을 눌러서 pull request를 생성할 수 있습니다.
- issue때와 마찬가지로 pull request에도 간략한 설명을 적을 수 있고, branch를 함부로 merge할 수 없게 assignees를 정할 수도 있고 코드리뷰 등도 할 수 있습니다.
- assignees를 지정할 경우, assignees들이 해당 pull request를 approve해줘야만 merge 버튼이 활성화 되게 됩니다.
- 활성화 된 merge버튼을 누르면 merge 작업이 완료 됩니다.
- 아래 사진은 pull request에서 할 수 있는 코드리뷰 예시 사진입니다.

<img src="/Image/img_pull_request_review.png" alt="img_pull_request_review" style="zoom:33%;" />

<br>

##### :star: master branch

- pull request기능을 이용해, 완성 된 상품(버전)을 develop branch에서 master branch로 merge 시킵니다.

<br>

### 4. 마치며...​ :rabbit:

저도 아직 초보자라.. 완전 간략한 내용을 정리한거라 이상한 내용이 있을 수도 있어요..! 하지만 여러분에게 도움이 되었길 바랍니다:slightly_smiling_face: 여러분 모두가 협업의 고수가 되기를 바라며 글 마칩니다 :)

<br>

### 5. 참고 자료​ :book:

https://www.holaxprogramming.com/2018/11/01/git-commands/

https://github.com/TeamMyDaily/4most-Android



