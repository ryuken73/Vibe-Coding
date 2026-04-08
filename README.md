# 1일차

## 여러가지 툴 설치
- python, node.js, git, git cli
- 특히 powershell에서 python과 node.js가 실행가능해야한다.
- 왜냐하면 cursor에서 자동화는 python script를 만들어서 수행하는 부분이 많다.
- 로컬 자원 access는 주로 powershell을 사용하는 듯 -> agent가 필요한 powershell 명령으로 수행 

### 구글 AI 스튜디오
- AI관련 여러가지 테스트가능
- 지구본 위에 구름이 흘러가는 웹페이지 만들어달라고 하니 three.js로 아래처럼 만들어 주더라 (public access도 가능)
- https://ai.studio/apps/18c4a2a9-ac1a-44a6-8d21-42f54ee8dc16?fullscreenApplet=true

### 모델 사용
- cursor의 모델로 gemini pro를 사용할 수 있는데, GFS 사용할 수 있겠지?
- 최근 기상앱때문에 많이 썼는데, sbs.co.kr 계정의 gemini token 사용량을 확인해보자!

## Firebase : DB만 있는게 아니다. 인증 + 백엔드까지 있다(functions)

## Vercel을 활용한 배포 ==> Github연동 시 바로 배포가능 (안경프로젝트에 사용할 수 있나? 보안은?)

## Cursor UI이해
- 기본적으로는 xcode와 비슷하지만 우측에 agent 채팅창이 있다.
- 이 agent 채팅창에서 내가 원하는 것을 요청하면 열어놓은 폴더(프로젝트)에 필요한 일들을 진행한다.
- agent에서 모델을 선택할 수 있는데, composer라는 cursor에서 제공하는 모델을 쓰면 토큰을 절약할 수 있다
- 작업에 따라 맞는 모델을 선택 : 모델을 자동차 연비에 비교

### AI 활용 아이디어
- 노트북 마이크 활성화 - 녹음 및 바로 STT화 -> 회의록 작성 => 웹앱으로 가능한가?
- weather-map을 three.js 기반 3D로 전환가능?
- 문서작업용

# 2일차

## AI에 문서작업하기
- cursor + chatgpt 사용한 시연
- codex cli (또는 gemini cli, cloud) 설치해서 대화형으로 진행하나보다
- codex cli + gemini cli가 결국 cursor의 agent를 대신하는 듯! new aget에 모델을 선택하면 되지 않나?
- *** 팁: cli에 계속 명령을 넣으면 히스토리가 남지 않으니, md파일을 만들어서 요청사항을 저장한다. ***
  내용사례 : 
  방송기술원에서 바이브코딩 교육을 요청
  - 커서로 진행
  - 초급과정
- 그 다음 codex cli에서 c.md를 참고해서 목차를 구성해줘 라고 요청할 수 있다.
- 그냥 만들어달라고 하면 예전 학습된 자료로만 만드니 아래 프롬프트를 추가하면 좋겠다.
  최신 커서 공식문서를 참고해서 4시간 분량으로 목차 md파일을 만들어줘
- 목차를 먼저 만드는 이유: 뼈대를 주면 내가 핸들링하기 쉽다..
- 목차를 보고 다듬을 수 있는데, 이것도 AI에게 부탁할 수 있다
  "이 목차를 보고 입문자와 전문가관점에서 비평해줘"로 피드백을 받을 수 도 있다.
- 다음은, 각 목차부터 md파일을 만들어 간다.
  "자 1번부터 만들어보자. md파일을 만들어줘"
  
## AI에서 문서작업하기 #2
- 요청자의 참고자료를 한 폴더에 집어넣는다.
- 파일 확장자가 doc, hwp, png, xlsx로 다양하다.
- 내가 가진 소스 문서들(참고할 수 있는)도 같이 넣는다.
- 이 폴더를 cousor에 drop하면 cursor가 열림...
  소스 : 류건우 프로필.pdf
- 프로필 pdf를 참고해서 워드로 워드문서를 만들어줘라고 해보자(같은 폴더에 요청자의 워드문서 샘플이 있다)
=> 과연 워드를 채워줄 것인가? 오!! 내용을 잘 채워줌~~~
=> 내가 가진 소스를 원하는 요청대로 문서를 만들어준다. (워드까지는 잘 된다)

## 스미더리(smithery) 사용하기
- skills : 사용하면 일관성있는 문서작업, 코딩, 디자인 가능하다.
  그냥 바이브 코딩으로 ppt를 만들면 그때그때 결과물이 다르다
- frontend-design 설치해보자 : 들어가서 보면 npx로 설치하게 되어있다.
- 설치 후 setting - rules,skills .. 들어가보면 방금 설치한 skill이 보인다.
  여기는 뭐하는 거지?
- 스킬설치 후 이걸 사용하려면? agent창에서 "/frontend-design"을 선택하고 채팅을 하면된다. -- 엄청 간단(어제 rule이랑 비슷)
- 진행할 프로젝트는... 9차시 개인브랜딩 사이트를 만들어보자.
- 쯔양의 나무위키 자료들을 복사해와서 info.md, png등으로 저장
- agent 채팅창에 아래와 같이 작성 + plan + /frontend-design enable + sonnet 빠른 모델 사용
```
info.md와 png 이미지 파일을 사용해서
- 개인 브랜딩 사이트를 만들고 싶어
```
- plan 완료 후 build로 결과물 만들기. index.html
- [todo]skills를 사용하고 안하고의 차이가 있나?
- [todo]plan없이 바로 agent로 만들어보는 것과는 차이가 있나?

    
