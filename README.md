# 🎙️ Sori AI (소리 AI)

> AI가 매일 전화로 어르신의 안부를 확인하고, 보호자에게 요약 리포트를 제공하는 케어 서비스

## ✨ 주요 기능

- **AI 음성 통화**: AI가 정해진 시간에 어르신과 자연스러운 대화
- **5단계 온보딩**: 보호자/어르신 정보, 통화 일정, 내용 커스터마이징
- **대시보드**: 오늘의 하이라이트, 주간 통계, 통화 기록 확인
- **통화 관리**: 전체 대화 내용, 감정 분석, 타임라인 제공
- **테스트 전화**: VoIP 푸시 알림으로 즉시 테스트 가능

## 🛠️ 기술 스택

- **Framework**: Next.js 16 (App Router), React 19
- **Language**: TypeScript 5
- **State**: Zustand (localStorage persist)
- **UI**: Tailwind CSS 4, Radix UI
- **Form**: React Hook Form, Zod
- **Date**: date-fns, react-day-picker

## 🚀 시작하기

### 설치

```bash
npm install
# or
yarn install
# or
pnpm install
```

### 개발 서버 실행

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

브라우저에서 [http://localhost:3000](http://localhost:3000)을 열어 확인하세요.

### 빌드

```bash
npm run build
npm start
```

## 📂 프로젝트 구조

```
app/
├── (dashboard)/          # 대시보드 라우트 그룹
├── dashboard/[elderId]/  # 어르신별 대시보드
├── call-list/            # 통화 목록 및 상세
├── register/             # 5단계 등록 폼
└── onboarding/           # 서비스 소개

components/
├── ui/                   # Radix UI 기반 컴포넌트 (23개)
├── custom/               # 커스텀 컴포넌트 (20개)
└── onboarding/           # 온보딩 폼 컴포넌트 (9개)

lib/api/                  # API 클라이언트
├── auth.ts               # 이메일 인증
├── elder.ts              # 어르신 관리
├── dashboard.ts          # 대시보드 데이터
└── push.ts               # 테스트 전화

store/                    # Zustand 상태 관리
types/                    # TypeScript 타입 정의
```

## 🔧 환경 변수

`.env.local` 파일 생성:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
```

## 📱 주요 페이지

- `/` - 랜딩 페이지
- `/onboarding` - 서비스 소개 (3단계 가이드)
- `/register` - 어르신 등록 (5단계 온보딩)
- `/dashboard` - 어르신 목록
- `/dashboard/[elderId]` - 어르신 대시보드
- `/call-list/[elderId]` - 통화 목록
- `/call-list/[elderId]/[callId]` - 통화 상세

## 🎯 핵심 데이터 흐름

```
사용자 입력 → React Hook Form → Zod 검증 → API 호출 → Zustand 업데이트 → UI 렌더링
```

## 📄 라이선스

이 프로젝트는 비공개 프로젝트입니다.
