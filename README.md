# 🌊 FlowPlan (플로우플랜)

> **"계획이 삶을 방해하지 않도록, 삶의 흐름에 따라 움직이는 유동적 스케줄러"**

FlowPlan은 고정된 시간표에 나를 맞추는 스트레스에서 벗어나, 실제 나의 행동 시점에 맞춰 일정을 실시간으로 재구성하는 **피드백 기반 라이프 매니저**입니다.

---

## ✨ 핵심 컨셉 (Core Concept)

기존 스케줄러가 "지키지 못한 계획"에 대한 부채감을 주었다면, **FlowPlan**은 그 차이를 데이터로 전환합니다.
- **실행(Do):** 실제 시작/종료 버튼을 기반으로 타임라인 업데이트
- **조정(Adjust):** 지연 시 뒤쪽 유동 일정을 자동으로 밀기 (Shift)
- **우선순위(Priority):** 고정 일정(Fixed)을 침범하지 않는 선에서 유동 일정 최적화
- **분석(Analyze):** 스킵 사유와 공백(Gap) 데이터를 통한 생활 패턴 개선

---

## 🚀 주요 기능 (Main Features)

### 1. 일정 유형 이원화
- **Fixed (고정):** 수업, 회의, 약속 등 변경 불가능한 시간. (유동 일정이 밀려와도 우선순위를 가짐)
- **Flexible (유동):** 독서, 운동, 공부 등 상황에 따라 조정 가능한 시간.

### 2. 다이내믹 실행 컨트롤러 (Popup UI)
- **4단계 시작 버튼:** [즉시 시작], [5분 뒤], [15분 뒤], [30분 뒤] 선택지를 제공하여 지연을 시스템에 반영.
- **일정 종료 & 즉시 시작:** 일정이 일찍 끝났을 때, 다음 일정을 당겨서 수행하거나 공백으로 남기기 선택.
- **스킵 메모:** 일정을 건너뛸 때 사유를 간단히 메모하여 나중에 확인 가능.

### 3. 지능적 일정 재계산 (Smart Re-scheduling)
- **Auto-Shift:** 앞 일정이 늦어지면 이후 유동 일정들을 연쇄적으로 지연.
- **Auto-Trim:** 유동 일정이 밀리다가 고정 일정과 겹치면, 고정 일정 시작 시간에 맞춰 앞 일정을 자동 종료.
- **Gap Tracking:** 스킵이나 조기 종료로 발생한 '공백 시간'을 추적하고 시각화.

### 4. 히스토리 & 리포트
- **Timeline Comparison:** 계획했던 시간(Gray)과 실제 수행 시간(Color)을 겹쳐서 비교.
- **Pattern Feedback:** "주로 어떤 사유로 스킵하는지", "어떤 시간대에 지연이 많은지" 분석 데이터 제공.

---

## 🛠 기술 스택 (Tech Stack)

- **Frontend:** Flutter / React Native (Cross-platform)
- **Database:** SQLite / Room (Local persistence)
- **Logic:** Dynamic Time-shifting Algorithm
- **Notifications:** OS Native Alarm & Foreground Service

---

## 📖 실행 시나리오 (User Scenario)

1. **07:00 기상 (유동):** 팝업 발생. [15분 뒤] 클릭.
2. **07:15 시작:** 기상 일정이 15분 지연 시작됨에 따라 이후 모든 유동 일정 15분 지연.
3. **08:50 독서 중:** 09:00에 고정 일정(회사 회의) 감지. 독서 일정이 5분 뒤 자동 종료됨을 알림.
4. **13:00 공부 (유동):** 급한 용무로 [스킵] 클릭. "은행 업무" 메모 입력.
5. **17:00 보고서 작성:** 집중력이 좋아 일찍 종료. [다음 일정 즉시 시작] 클릭하여 저녁 시간을 조기 확보.
6. **22:00 마감:** 오늘 발생한 1시간의 공백과 지연 패턴을 확인하며 내일 계획 조정.

---

## ⚙️ 설치 및 빌드 방법 (Getting Started)

```bash
# Repository Clone
git clone [https://github.com/your-username/FlowPlan.git](https://github.com/your-username/FlowPlan.git)

# Install Dependencies
flutter pub get

# Run Project
flutter run
