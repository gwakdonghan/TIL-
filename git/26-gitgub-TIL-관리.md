# github TIL 작성법과 문제점
## 파일정리

### 작성법
1. github 에서 Repository 를 먼저 만든다. github에 들어가서 프로필누르고 Your repositories 여기들어가서 NEW 로 들어가서 만들어준다. 
TIL만 작성할꺼니까 Repository name은 TIL로 만든다. 그리고 밑으로 내려가서 
Add a README file 이거를 선택해 준다. **Add a README file 를 체크하고 Repository를 만들면 commit이 생긴다**
그리고 제일밑에 초록색으로 되있는 create Repository 를 누르면 된다. 그럼 commit이 되어있는걸 볼수있다.

2. 이제 만들어진 TIL Repository 를 내 로컬로 가지고 와야 한다. 이걸 git Clone 이라고 한다
내 로컬 원하는 위치에다가 clone 하면되는데 데스트탑에다가 하면된다. 터미널에서 데스크탑으로 위치해서 **git clone 주소** 이렇게적고 
엔터하면 clone이 되고 데스크탑에 폴더가 만들어진다. 그럼 해당 폴더에 위치해서 code . 이라고 하면 vscode가 열린다. 여기서 TIL 을 작성하면 된다. 
사진이나 링크다 다 할수있다.

3. 작성이끝났다면 저장을 하고 commit을 만들어줘야 한다. vscode터미널에서 git add . 적고 엔터하고, git commit -m "TIL" 적고 엔터하고 git push 까지하면 내 github에 내가 작성한 글이 올라가 있는걸 볼수있다. 
---

### 문제점
1. github 으로 TIL 작성을 할려고한다. TIL은 매일 작성을 해야되는데 작성할때마다 github에서 새로운 Repository 를 만들고 새로운 폴더를 만들어야 되는줄 알았다, 
새로 만들때 마다 폴더들이 데스크탑에 쌓였다. 그런데 그게 아니라 github에서 TIL 이라는 Repository 하나만 만들어서 vscode랑 연결해주면 vscode에서 계속 TIL 을 작성하면된다.
그리고
2. vscode에서 TIL을 매일 작성할때마다 파일을 만들어야 되는데 만들면, 내 github TIL Repository에 파일이 계속 남겨서져 어떻게 정리를 해야하는지 몰랐다.

1-1 
말했던것 처럼 github에서 TIL 이라는 Repository 하나만 만들어서 vscode랑 연결해주면 vscode에서 계속 작성해주면된다.
TIL 작성을 할꺼면, TIL 폴더에서 vscode 를열어주고 파일을하나 만들어서 작성하고 git add . 하고, git commit -m ""
해주고, git push 해주면 github에 올라간다.

2-1 하루마다 TIL을 작성하면 vscode 든 github이든 파일이 계속 쌓일것이다. 파일이많아지면 너무 지져분해 져서,
연도 단위인 폴더를 만들고, 한달단위인 폴더를 만들어서 연도 단위폴더에 넣어주고, 한달 단위폴더안에 날짜별로 파일을 넣어주면 정리가 된다.

![vscodeTIL](/imgs/vscode_TIL.png)
![githubTIL](/imgs/github_TIL.png)
