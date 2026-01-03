# 🗓️ 고령층 일정 관리 앱 (Elderly Schedule App)

고령층 사용자를 위한 직관적이고 사용하기 쉬운 일정 관리 애플리케이션입니다.

## 📱 주요 기능

### 1. 메인 화면
- 큰 버튼 2개로 구성된 간단한 인터페이스
  - ✅ **일정 입력**: 새로운 일정을 추가
  - 📅 **일정 보기**: 등록된 일정을 주간 단위로 확인

### 2. 일정 입력 플로우 (3단계)

#### 섹션 1: 일정 유형 선택
- 병원 방문
- 약 복용
- 모임/약속
- 직접 입력 (음성/텍스트 입력)

#### 섹션 2: 날짜 선택
- 스크롤 방식의 직관적인 날짜 선택
- 월, 일, 요일을 개별 선택
- 자동 날짜 계산 및 검증
- 이번주/다음주/다다음주 표시

#### 섹션 3: 시간 선택
- 오전/오후 토글
- 시간과 분을 스크롤로 선택
- 10분 단위 선택 가능

### 3. 일정 보기
- 주간 단위로 일정 표시
- 좌우 스와이프로 주차 이동
- 월~일 요일별 일정 카드
- 오늘 날짜 강조 표시
- 일정 길게 눌러서 삭제

## 🎨 디자인 특징

### 고령층 친화적 UI/UX
- ✅ **큰 글씨**: 최소 24pt 이상
- ✅ **큰 버튼**: 최소 80dp 높이
- ✅ **높은 대비**: 4.5:1 이상의 색상 대비
- ✅ **명확한 아이콘**: 아이콘 + 텍스트 조합
- ✅ **충분한 여백**: 터치하기 쉬운 간격
- ✅ **햅틱 피드백**: 버튼 클릭 시 진동 피드백
- ✅ **단계별 진행**: 한 번에 하나씩 진행

### 색상 팔레트
- Primary: `#4A90E2` (차분한 파란색)
- Secondary: `#7ED321` (연두색 - 성공)
- Warning: `#F5A623` (주황색)
- Background: `#FFFFFF` (흰색)

## 📂 프로젝트 구조

```
lib/
├── core/
│   ├── theme/
│   │   ├── app_colors.dart           # 색상 정의
│   │   ├── app_text_styles.dart      # 텍스트 스타일
│   │   ├── app_spacing.dart          # 간격 정의
│   │   └── app_theme.dart            # 테마 설정
│   └── widgets/
│       ├── large_button.dart         # 큰 버튼 위젯
│       ├── progress_indicator_bar.dart  # 진행 표시 바
│       ├── scroll_picker.dart        # 스크롤 선택기
│       └── navigation_buttons.dart   # 네비게이션 버튼
├── features/
│   ├── home/
│   │   └── screens/
│   │       └── main_screen.dart      # 메인 화면
│   ├── input/
│   │   ├── screens/
│   │   │   ├── section1_type_screen.dart    # 유형 선택
│   │   │   ├── section2_date_screen.dart    # 날짜 선택
│   │   │   └── section3_time_screen.dart    # 시간 선택
│   │   ├── widgets/
│   │   │   └── voice_input_modal.dart       # 음성 입력 모달
│   │   └── models/
│   │       └── schedule_model.dart          # 일정 데이터 모델
│   └── schedule/
│       ├── screens/
│       │   └── schedule_view_screen.dart    # 일정 보기 화면
│       └── widgets/
│           ├── week_navigator.dart          # 주차 네비게이터
│           └── day_schedule_card.dart       # 일일 일정 카드
└── services/
    └── schedule_service.dart         # 일정 저장/불러오기 서비스
```

## 🚀 시작하기

### 필요 조건
- Flutter SDK 3.10.4 이상
- Dart 3.10.4 이상

### 설치 및 실행

1. 저장소 클론
```bash
git clone <repository-url>
cd elderly_schedule_app
```

2. 의존성 설치
```bash
flutter pub get
```

3. 앱 실행
```bash
flutter run
```

### 지원 플랫폼
- ✅ Android
- ✅ iOS
- ✅ Windows
- ✅ macOS
- ✅ Linux
- ✅ Web

## 📦 사용된 패키지

- `shared_preferences`: 일정 데이터 로컬 저장

## 🔧 향후 개선 사항

### 우선순위 높음
- [ ] 실제 음성 인식 통합 (speech_to_text 패키지)
- [ ] 알림 기능 (flutter_local_notifications)
- [ ] 보호자 앱 연동 (Firebase Cloud Messaging)

### 우선순위 중간
- [ ] 일정 수정 기능
- [ ] 반복 일정 설정
- [ ] 일정 색상 커스터마이징
- [ ] 다크 모드 지원

### 우선순위 낮음
- [ ] 통계 및 리포트
- [ ] 일정 내보내기/가져오기
- [ ] 다국어 지원

## 🎯 접근성 고려사항

- ✅ 큰 터치 영역 (최소 60x60dp)
- ✅ 명확한 시각적 피드백
- ✅ 단순한 네비게이션 구조
- ✅ 오류 방지 및 되돌리기 기능
- ✅ 세로 방향 고정 (Portrait only)

## 📝 라이선스

이 프로젝트는 교육 및 개인 사용 목적으로 제작되었습니다.

## 👥 기여

이슈 리포트와 Pull Request를 환영합니다!

---

**만든 날짜**: 2026년 1월 4일
**Flutter 버전**: 3.38.5
**Dart 버전**: 3.10.4
