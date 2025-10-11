### 🌐 Remote Repository  
**📍 Remote Repository란?**  
- Remote Repository는 GitHub(또는 GitLab, Bitbucket 등) 같은 원격 서버에 있는 저장소를 말한다.  
- 즉, 내 컴퓨터(Local Repository)에서 작업한 내용을 인터넷 상의 저장소로 업로드하는 것이다.  
- Local과 Remote는 파일 단위가 아닌, Commit 단위로 소통한다.  
  
### 📦 Remote Repository 연결 방법  
**✅ 방법 1. Local에서 먼저 만들고 → GitHub와 연결하기**  
1️⃣ GitHub에서 Repository 생성  
- GitHub 사이트에서 새 저장소(New Repository)를 만든다.  
2️⃣ 내 컴퓨터(Local)에 Repository 만들기  
cd Desktop → mkdir my-repo → cd my-repo → git init  
3️⃣ GitHub 주소 연결하기  
git remote add origin {githup주소넣으면된다}  
- 내 Local Repository에게  
“이 주소가 내 GitHub 원격 저장소야” 라고 알려주는 명령어.  
4️⃣ Commit 후 업로드  
git add . →  git commit -m "first commit" →  git push -u origin main
- 이제 Local의 Commit들이 Remote(GitHub)로 올라간다.
- 이후부터는 git push만 입력해도 자동으로 연결된다.

**✅ 방법 2. GitHub에서 먼저 만들고 → Local로 가져오기 (Clone)**
1️⃣ GitHub에서 Repository 생성
- GitHub에서 새 Repository를 만든 후, 주소(URL) 를 복사한다.  
2️⃣ Local로 Clone 하기    
cd Desktop  
git clone {githup주소넣으면된다}  
- 내 바탕화면에 GitHub 저장소가 그대로 복사됨  
- 자동으로 .git 폴더가 포함되어 있어, 이미 Git 연결 완료 상태임 ✅  
3️⃣ 폴더 이동 및 작업  
cd my-repo(만들어진폴더)에서 code . 를 하면된다.
4️⃣ Commit & Push  
작업을 하고,  
git add . → git commit -m "update" → git push
- 작업 내용을 GitHub에 반영한다.

✅ 기억하기  
💬 “GitHub와 내 컴퓨터는 파일이 아니라 Commit 단위로 연결된다.”

---
31:00 시작



