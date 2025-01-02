# 장고 요청처리 흐름
**HttpRequest란?**
HttpRequest는 브라우저가 서버에 "어떤 요청"을 보낼 때 사용하는 메시지입니다.
예를 들어, 브라우저 주소창에 http://127.0.0.1:8000/index를 입력했다고 가정해보세요
그러면 브라우저가 "이 주소에 있는 서버에게 /index라는 정보를 보내주세요!"라는 요청을 HttpRequest 형식으로 전달합니다.

**쉽게 이해하기 위한 비유**
브라우저를 "편지 보내는 사람"으로 생각해 보세요. (여기서는 크롬)
브라우저는 주소(http://127.0.0.1:8000/index)가 적힌 편지(HttpRequest)를 작성합니다.
이 편지를 Django 서버에게 전달합니다.
Django 서버는 편지를 읽고, 적절한 응답(HttpResponse)을 작성하여 다시 브라우저로 돌려줍니다.


**왜 HttpRequest가 중요한가요?**
Django 서버는 HttpRequest라는 편지가 있어야만 "사용자가 무엇을 원하는지" 알 수 있습니다. 요청이 없으면 서버는 어떤 데이터를 반환해야 할지 알지 못합니다.


**요청흐름 순서**
Chrome에서 HttpRequest 발생
사용자가 브라우저(여기서는 Chrome)를 통해 특정 URL(예: /index)에 접근합니다.
이는 Django 서버로 HTTP 요청(HttpRequest) 을 보내는 과정입니다.

2. urls.py로 요청 전달
Django 서버가 해당 요청을 받으면, 가장 먼저 urls.py 파일을 확인합니다.
urls.py 파일은 URL 패턴(예: /index)과 그 URL을 처리할 view 함수를 매핑합니다.
요청된 URL과 매칭되는 패턴을 찾아, 매칭된 view 함수로 요청을 전달합니다.

3. views.py에서 요청 처리
요청이 매칭된 view 함수로 전달되면, view 함수는 요청을 처리합니다
예를 들어, /index URL에 대응하는 view 함수가 views.py에 정의되어 있다면, 해당 함수가 호출됩니다
view 함수는 요청에 맞는 로직을 처리하고, HttpResponse 객체를 생성해 반환합니다.

4. HttpResponse를 브라우저로 전달
views.py에서 생성된 HttpResponse 객체는 다시 Django 서버를 통해 사용자(브라우저)로 전달됩니다.
브라우저는 전달받은 HttpResponse의 내용을 화면에 출력합니다. (예: "Hello, Django!”)


**흐름 요약**
브라우저가 HttpRequest를 보냄.
Django가 urls.py를 확인하여 요청된 URL과 매칭되는 view 함수 탐색.
views.py의 view 함수가 요청을 처리하고 HttpResponse 객체 생성.
생성된 HttpResponse가 브라우저로 전달되어 화면에 출력.

---
