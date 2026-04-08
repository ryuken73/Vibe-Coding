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

