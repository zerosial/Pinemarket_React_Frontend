### **프로젝트 명**: 파인 마켓 (당근마켓 클론)

![chrome_61HkvTxx4T](https://github.com/zerosial/Pinemarket_React_Frontend/assets/97251710/140f5219-d450-4026-800a-59db3acde328)


[WEB](https://pinemarket.cielui.com/web) : https://pinemarket.cielui.com/web

[API_END_POINT](https://pinemarket.cielui.com) : https://pinemarket.cielui.com

[SWAGGER](https://pinemarket.cielui.com/docs) : https://pinemarket.cielui.com/docs


### 1. 서론

**팀 소개 및 프로젝트 개요**

- 팀원: 유진(프론트엔드), 낙준(프론트엔드), 승훈(풀스택)
- 프로젝트 목적:  기술 습득 및 향상을 위한 미니 프로젝트
- 동기: 당근마켓의 유저 인터페이스와 기능을 모델로 삼아, 현대적인 기술 스택을 활용하여 유사한 서비스를 제작

**프로젝트 선정 배경**

- UI의 단순함과 더불어 구현 목표였던 기능이 다수 존재
- 최신 프론트엔드 기술을 활용한 실제 프로젝트 경험 축적

### 2. 프로젝트 관리 및 협업 방법

**코드 리뷰 및 회의 스케줄**

- 코드 리뷰: 매주 월, 수, 금 오후 3시 PR 리뷰 및 머지
- 주간 회의: 매주 한 번, 시간 미정 (주로 수요일에 진행)

**Branch 및 Commit 규칙**

- Branch 명명 규칙: **`feature/[기능명]`**
- Commit 메시지 규칙: **`feat: [기능 설명]`** (한글 사용 가능)

### 3. 기술 스택 및 도구

**기술 스택 소개**

- 프론트엔드
    
    # 코어
    
    ### Vite
    
    - **장점**: 빠른 핫 모듈 교체(HMR)와 빌드 속도, ES 모듈을 기반으로 한 현대적인 프로젝트 구조 제공.
    - **적용법**: 개발 의존성으로 Vite를 추가하고, **`vite.config.js`**를 통해 프로젝트 설정을 커스터마이징함.
    
    ### pnpm
    
    - **장점**: 디스크 공간 절약 및 빠른 설치 속도, 중복되는 패키지를 하드 링크로 관리하여 효율적.
    - **적용법**: 프로젝트 디렉토리에서 pnpm을 사용하여 의존성을 관리하고, **`pnpm-lock.yaml`** 파일로 일관된 패키지 버전 유지.
    
    # 비동기 통신
    
    ### Tanstack Query (React Query)
    
    - **장점**: 서버 상태 관리를 위한 강력한 도구, 데이터 캐싱, 백그라운드 업데이트, 데이터 동기화 등을 쉽게 구현.
    - **적용법**: API 호출을 위한 hook (**`useQuery`**, **`useMutation`**)을 사용하여 비동기 데이터를 처리하고, 컴포넌트에서 직접 데이터 상태와 캐싱을 관리.
    
    ### Axios
    
    - **장점**: 브라우저와 노드에서 모두 사용 가능한 HTTP 클라이언트, 요청 취소, 응답 시간 초과, HTTPs 지원.
    - **적용법**: 인스턴스를 생성하여 API 요청을 관리하고, 인터셉터를 사용하여 요청 및 응답을 전역적으로 처리.
    
    # 라우터
    
    ### React-Router
    
    - **장점**: SPA(Single Page Application)에서의 라우팅을 쉽게 구현, 동적 라우팅 지원.
    - **적용법**: **`BrowserRouter`**, **`Routes`**, **`Route`** 컴포넌트를 사용하여 애플리케이션 내의 라우팅 구조를 설정.
    
    # 상태관리
    
    ### Zustand
    
    - **장점**: 간결하고 가볍며, 설정이 적은 상태 관리 라이브러리. 리덕스보다 간단하게 상태 관리 가능.
    - **적용법**: 글로벌 상태 저장소를 생성하고, 컴포넌트에서 직접 사용하여 상태를 읽거나 업데이트함.
    
    # CSS (UI&UX)
    
    ### Emotion
    
    - **장점**: CSS-in-JS 라이브러리, 동적 스타일링 및 테마 지원, 높은 성능.
    - **적용법**: **`styled`** 컴포넌트를 사용하여 스타일을 직접 컴포넌트에 적용하거나, **`css`** prop을 사용하여 인라인 스타일링.
    
    ### DaisyUI
    
    - **장점**: Tailwind CSS 위에 구축된 UI 컴포넌트 라이브러리, 테마 지원 및 맞춤형 디자인 요소 제공.
    - **적용법**: Tailwind CSS 설정에 DaisyUI 플러그인을 추가하고, 제공되는 컴포넌트와 유틸리티 클래스를 활용하여 UI 구성.
    
    ### TailwindCSS
    
    - **장점**: 유틸리티 우선 CSS 프레임워크로 빠른 커스텀 디자인 가능, 반응형 디자인 쉽게 구현.
    - **적용법**: **`tailwind.config.js`**를 통해 프로젝트의 디자인 시스템을 정의하고, HTML 또는 JSX에 직접 유틸리티 클래스를 적용.

### 4. 프로젝트 주요 기능 및 개발 과정 (각 개발자)

**유진**

- 담당 기능: 메인 페이지와 검색 기능
- 개발 과정: 사용자 경험 중심의 디자인 및 캐싱 전략 구현, 재사용있는 컴포넌트 구현

**승훈**

- 담당 기능: 로그인/로그아웃, 헤더 및 푸터, 프로필 페이지, 백엔드 전반
- 개발 과정: 보안 강화 및 사용자 인터페이스 일관성 유지

**낙준**

- 담당 기능: 모달, 라우트 설정, 상세 페이지
- 개발 과정: 높은 퍼포먼스 유지를 위한 최적화 전략 구현
