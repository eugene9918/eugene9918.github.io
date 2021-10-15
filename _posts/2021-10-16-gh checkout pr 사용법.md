

# `gh checkout pr`의 올바른 사용
`gh checkout pr` 을 쓸 때를 한 번 더 정리해보자면 다음과 같습니다.

내가 만든 PR 인 경우 항상 git push 와 git pull 만 한다.
내가 maintainer 이고 다른 사람이 생성한 PR 을 받고 싶으면 gh checkout pr 을 실행한다. 
나중에 다른 사람이 추가 commit 을 올렸으면 다시 gh checkout pr 을 수행하면 git pull 받는 것과 같은 효과가 난다. 
PR 생성자가 edit by maintainer 를 허용했으면 나도 해당 branch 에서 commit 하고 git push 를 할 수 있다.

출처: 짱가
