# 오름(Oreum) ⛰️

대학생의 취업 준비 과정을 산 등반에 비유한 커리어 관리 서비스입니다. 학년과 희망 직무에 따른 비교 통계, 성취도 시각화를 통해 준비 현황을 확인할 수 있습니다.

멋쟁이사자처럼 인천대학교 14기 미니 해커톤 프로젝트 · 2026.06.29 ~ 2026.07.13

## 주요 기능

- **커리어 대시보드:** 학년·희망 직무 기준 비교 통계와 현재 성취도 확인
- **성취도 시각화:** 고도와 깃발 등 등반 요소로 준비 과정 표현
- **사용자 정보 관리:** 학적, 희망 직무, 비밀번호 변경

## 기술 스택

- **Frontend:** React, JavaScript, Vite
- **Styling:** styled-components
- **Routing:** React Router
- **API:** Axios
- **Animation:** Framer Motion

## 문제 해결 경험

### 공통 모달 컴포넌트

- **문제:** 학적·직무·비밀번호 변경 과정에서 기본 브라우저 알림창을 사용하면 화면 경험이 일관되지 않고, 기능별 모달을 각각 만들면 중복 코드가 늘어날 수 있었습니다.
- **해결:** 열림 상태와 모달 유형을 함께 관리하는 공통 컴포넌트로 구성하고, 유형에 따라 내용을 바꾸도록 구현했습니다.
- **결과:** 여러 화면에서 동일한 모달 UI를 재사용할 수 있게 했습니다.

### API 응답 및 오류 처리

- **문제:** API 요청 성공 이후에도 응답 데이터 접근 방식 때문에 후속 처리가 정상적으로 실행되지 않는 문제가 있었습니다.
- **해결:** Axios 응답의 `data` 구조를 확인하고, 오류 메시지는 `error?.response?.data?.message`로 안전하게 접근하도록 수정했습니다.
- **결과:** 서버 응답과 오류 메시지를 화면에 정상적으로 반영할 수 있도록 개선했습니다.

### 화면 간 희망 직무 정보 유지

- **문제:** 코스 리뷰 화면에서 필요한 희망 직무 정보가 API 응답에 포함되지 않았습니다.
- **해결:** 앞선 입력 단계에서 선택한 직무 정보를 `localStorage`에 저장하고 후속 화면에서 재사용했습니다.
- **결과:** 화면 이동 후에도 필요한 직무 정보를 사용할 수 있도록 했습니다.

## 실행 방법

```bash
npm install
npm run dev
```

프로덕션 빌드:

```bash
npm run build
```

API 연동 기능을 실행하려면 백엔드 서버 및 프로젝트 환경 설정이 필요할 수 있습니다.

## 프로젝트 구조

```text
src/
  api/          API 요청
  assets/       이미지 및 정적 리소스
  components/   공통 UI 컴포넌트
  pages/        화면 컴포넌트
  styles/       스타일
```

## 팀 구성

| 역할     | 팀원                                                                          |
| -------- | ----------------------------------------------------------------------------- |
| PM       | 김지유                                                                        |
| Design   | [정지인](https://github.com/jiin-jung)                                        |
| Frontend | [김남윤](https://github.com/namyoon0418), [임상현](https://github.com/sh2624) |
| Backend  | [임재영](https://github.com/yim0327), [조수진](https://github.com/sujincyan)  |

## 관련 링크

- [웹 서비스](https://www.oreumm.site)
- [프로젝트 소개 자료](https://drive.google.com/file/d/1PSVO96uw7UohAeXVdN6iKzYTZn_i9GnI/view?usp=sharing)
- [백엔드 저장소](https://github.com/LikeLionUniv-INU-oreum/oreum-backend)
