# 알약지니 (Pill Genie) - Datacampus 2023

![Java](https://img.shields.io/badge/Java-11-007396?style=flat-square&logo=java)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.7.14-6DB33F?style=flat-square&logo=spring-boot)
![MySQL](https://img.shields.io/badge/MySQL-8.0+-4479A1?style=flat-square&logo=mysql)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

> 2023 을지대학교 데이터캠퍼스 프로젝트 - 건강 설문 기반 맞춤형 영양소 추천 시스템

---

## 📋 프로젝트 소개 (Project Overview)

**알약지니**는 사용자의 건강 습관과 생활 패턴을 분석하여 맞춤형 영양소를 추천하는 웹 애플리케이션입니다. 17단계의 상세한 설문조사를 통해 수집된 데이터를 머신러닝 모델로 분석하고, 개인별로 부족한 영양소를 진단하여 적절한 건강기능식품을 추천합니다.

**Pill Genie** is a web application that analyzes users' health habits and lifestyle patterns to recommend personalized nutritional supplements. Through a detailed 17-step survey, collected data is analyzed by a machine learning model to diagnose individual nutritional deficiencies and recommend appropriate health supplements.

---

## 👥 팀 구성 (Team)

### DATA PREPROCESSING
- **DATA TEAM**: Kyungtae Choi ([@Goddohi](https://github.com/Goddohi)), Jong Hyun Park ([@JayParc](https://github.com/JayParc))
- **PAPER ANALYSIS**: Kyungtae Choi ([@Goddohi](https://github.com/Goddohi)), SuHyun Park ([@hyumme](https://github.com/hyumme)), Yeojin Chung ([@Jini-lab](https://github.com/Jini-lab))

### DEVELOPMENT TEAMS
- **Design / Frontend**: SuHyun Park ([@hyumme](https://github.com/hyumme)), Ki Tae Mun ([@vambroag](https://github.com/vambroag)), Jong Hyun Park ([@JayParc](https://github.com/JayParc))
- **AI / Backend**: JeongYeop Lee ([@ILikeCloudy](https://github.com/ILikeCloudy)), Yeojin Chung ([@Jini-lab](https://github.com/Jini-lab)), Kyungtae Choi ([@Goddohi](https://github.com/Goddohi))
- **Project Management**: Kyungtae Choi ([@Goddohi](https://github.com/Goddohi)), Ki Tae Mun ([@vambroag](https://github.com/vambroag)), SuHyun Park ([@hyumme](https://github.com/hyumme)), JeongYeop Lee ([@ILikeCloudy](https://github.com/ILikeCloudy))

---

## ✨ 주요 기능 (Key Features)

### 1. 인터랙티브 다단계 설문조사
- **17단계** 건강 및 생활습관 설문
- 진행률 표시 바와 시각적 피드백
- 단계별 입력 검증 및 조건부 질문

### 2. 설문 구성
**기본 정보 (3단계)**
- 이름, 생년월일, 키, 몸무게, 성별

**생활 습관 (8단계)**
- 하루 앉아있는 시간
- 주간 운동 빈도
- 하루 물 섭취량
- 식사 빈도 (아침, 점심, 저녁)
- 흡연 및 음주 습관
- 피로도, 수면 시간, 스트레스 수준

**건강 이력 (6+단계)**
- 우울증 진단 이력
- 전반적 건강 상태
- 복용 중인 약물 (17가지 이상)
- 현재 질병 (고혈압, 당뇨, 빈혈, 암 등)
- 현재 증상 (발진, 안구건조, 저림 등)
- 여성 전용 질문 (임신, 폐경, 피임약 복용)

### 3. 머신러닝 기반 영양소 분석
- Python 머신러닝 모델 연동
- 설문 데이터 기반 영양소 결핍 진단
- 바이너리 인코딩 시스템으로 결과 분류

### 4. 맞춤형 영양소 추천 리포트
**14가지 결과 페이지 제공:**
- **비타민**: A, B1 (티아민), B2 (리보플라빈), B9 (엽산), C, D, E
- **미네랄**: 칼슘, 칼륨, 마그네슘, 철분, 아연
- **건강 상태**: 건강함, 특이사항 없음

각 결과 페이지에는 다음이 포함됩니다:
- 개인화된 인사말
- 권장 섭취량
- 결핍 증상
- 보충제 복용 시 주의사항
- 추천 건강기능식품 (이미지 포함)

### 5. 데이터 영속성
- MySQL 데이터베이스에 모든 설문 응답 저장
- 40개 이상의 필드로 종합적인 건강 데이터 관리

---

## 🛠 기술 스택 (Tech Stack)

### Frontend
- **HTML5** with Thymeleaf Template Engine
- **JavaScript** (Vanilla + jQuery 3.6.0)
- **CSS3** with Custom Styling
- **Responsive Web Design**
- **Font**: Pretendard 1.3.8

### Backend
- **Java 11**
- **Spring Boot 2.7.14**
  - Spring Web
  - Spring Data JPA
  - Spring Web Services
- **Gradle 7.6+** (Build System)

### Database
- **MySQL 8.0+**
- **Hibernate ORM** (Auto-update DDL)
- **JDBC** (MySQL Connector)

### Machine Learning
- **Python** (External ML Model Integration)
- Binary Classification System

---

## 📁 프로젝트 구조 (Project Structure)

```
Datacampus/
├── src/
│   └── main/
│       ├── java/com/Datacampus/Team5/
│       │   ├── Team5Application.java           # Spring Boot Entry Point
│       │   ├── controller/
│       │   │   └── MainController.java         # Request Routing & Handling
│       │   ├── service/
│       │   │   └── ResponseService.java        # Business Logic
│       │   ├── repository/
│       │   │   └── ResponseRepository.java     # Database Access (JPA)
│       │   ├── entity/
│       │   │   └── ResponseEntity.java         # Survey Data Model
│       │   ├── constants/
│       │   │   └── PageSet.java                # Result Type Mappings
│       │   └── config/
│       │       └── Webconfig.java              # Web MVC Configuration
│       └── resources/
│           ├── templates/
│           │   ├── index.html                  # Home Page
│           │   └── survey.html                 # Survey Questionnaire
│           ├── application.yml                 # Spring Boot Configuration
│           └── static/datacampusproject/
│               ├── style.css                   # Home Page Styles
│               ├── survey/
│               │   ├── style.css               # Survey Styling
│               │   └── script.js               # Form Navigation & Validation
│               ├── result/                     # Result Pages (14 types)
│               │   ├── vitaminA/
│               │   ├── vitaminC/
│               │   ├── vitaminD/
│               │   ├── vitaminE/
│               │   ├── thiamine/
│               │   ├── Riboflavin/
│               │   ├── folate/
│               │   ├── calcium/
│               │   ├── kalium/
│               │   ├── magnesium/
│               │   ├── iron/
│               │   ├── zinc/
│               │   ├── healthy/
│               │   └── nothing/
│               └── img/                        # Graphics & Icons
├── build.gradle                                # Gradle Configuration
├── settings.gradle                             # Gradle Settings
├── gradlew / gradlew.bat                       # Gradle Wrapper
└── README.md
```

---

## 🚀 설치 및 실행 (Installation & Setup)

### 사전 요구사항 (Prerequisites)
- **Java 11** 이상
- **MySQL 8.0** 이상
- **Python 3.x** (머신러닝 모델 실행용)
- **Gradle 7.6+** (또는 포함된 Gradle Wrapper 사용)

### 1. 레포지토리 클론 (Clone Repository)
```bash
git clone https://github.com/ILikeCloudy/Datacampus.git
cd Datacampus
```

### 2. 데이터베이스 설정 (Database Setup)
MySQL에 데이터베이스 생성:
```sql
CREATE DATABASE mainfo;
USE mainfo;
```

### 3. 애플리케이션 설정 (Application Configuration)
`src/main/resources/application.yml` 파일 수정:
```yaml
spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    url: jdbc:mysql://localhost:3306/mainfo
    username: your_mysql_username
    password: your_mysql_password
```

### 4. 빌드 및 실행 (Build & Run)
```bash
# Gradle Wrapper를 사용한 빌드
./gradlew build

# 애플리케이션 실행
./gradlew bootRun
```

또는 직접 실행:
```bash
java -jar build/libs/Team5-0.0.1-SNAPSHOT.war
```

### 5. 브라우저에서 접속
```
http://localhost:8080
```

---

## 🗄 데이터베이스 스키마 (Database Schema)

### Table: `answer`

| Field | Type | Description |
|-------|------|-------------|
| id | BIGINT (PK) | Auto-increment ID |
| nickname | VARCHAR | 사용자 이름 |
| gender | INT | 성별 (0=남성, 1=여성) |
| age | INT | 나이 (생년월일로부터 계산) |
| pheight | INT | 키 (cm) |
| pweight | INT | 몸무게 (kg) |
| q_sit | INT | 하루 앉아있는 시간 |
| q_exercise | INT | 주간 운동 빈도 |
| q_drink | INT | 하루 물 섭취량 (컵) |
| q_breakfast | INT | 주간 아침 식사 횟수 |
| q_lunch | INT | 주간 점심 식사 횟수 |
| q_dinner | INT | 주간 저녁 식사 횟수 |
| q_smoke | INT | 흡연 여부 |
| q_alcohol | INT | 음주 여부 |
| q_alcohol_time | INT | 음주 빈도 |
| q_alcohol_quant | INT | 음주량 |
| q_tired | INT | 피로도 |
| q_sleep | INT | 수면 시간 |
| q_stress | INT | 스트레스 수준 |
| q_depress | INT | 우울증 이력 |
| q_healthy | INT | 건강 상태 자가 평가 |
| q_cancer | INT | 항생제 복용 여부 |
| q_state | INT | 현재 증상 |
| q_disease_* | INT | 질병 체크박스 (7종류) |
| q_medicine | INT | 복용 약물 개수 |
| qf_pregnant | INT | 임신/수유 여부 |
| qf_menopause | INT | 폐경 진단 |
| qf_birthpill | INT | 피임약 복용 여부 |
| result | INT | ML 결과 코드 |
| yes_or_no | INT | 사용자 피드백 |

---

## 📊 API 엔드포인트 (API Endpoints)

| Endpoint | Method | Description | Returns |
|----------|--------|-------------|---------|
| `/` | GET | 홈 페이지 | index.html |
| `/survey/survey` | GET | 설문조사 페이지 | survey.html |
| `/answer` | POST | 설문 제출 및 ML 분석 | JSON (결과 타입, 닉네임, 수치) |

---

## 🔄 데이터 흐름 (Data Flow)

```
사용자가 설문 작성 (survey.html)
    ↓
JavaScript가 데이터 검증 및 수집
    ↓
AJAX POST 요청 → /answer 엔드포인트
    ↓
MainController가 ResponseEntity 수신
    ↓
ResponseService.insertdata() → MySQL에 저장
    ↓
ProcessBuilder가 Python ML 모델 호출
    ↓
Python 모델이 설문 데이터 분석
    ↓
데이터베이스에 결과 코드 업데이트
    ↓
ResponseService.response() → 최신 레코드 조회
    ↓
PageSet이 결과 코드를 영양소 타입으로 매핑
    ↓
JavaScript가 결과 페이지로 리다이렉트
    ↓
사용자가 맞춤형 영양소 리포트 확인
```

---

## 🎯 사용 방법 (How to Use)

1. **홈 페이지 접속**: `http://localhost:8080`
2. **설문 시작**: "설문 시작하기" 버튼 클릭
3. **설문 작성**: 17단계 질문에 답변
   - 기본 정보 입력
   - 생활 습관 선택
   - 건강 이력 체크
4. **결과 확인**: 자동으로 분석된 맞춤형 영양소 추천 확인
5. **추천 제품**: 각 영양소별 추천 건강기능식품 확인

---

## ⚠️ 주의사항 (Important Notes)

> **이 레포지토리는 2023 을지대학교 데이터캠퍼스 프로젝트의 일부 파일입니다.**

### 포함되지 않은 파일 (Not Included)
- **머신러닝 데이터셋**: 개인정보 보호를 위해 제공되지 않습니다
- **완성된 ML 모델**: `total_mai3.py` 파일은 포함되지 않았습니다
- **데이터베이스 접속 정보**: `application.yml`의 DB 비밀번호는 제거되었습니다
- **정적 리소스 경로**: `C:/springboot_img/` 경로는 Windows 환경에 특화되어 있습니다

### 학습 목적 사용 (Educational Use)
이 코드는 **학습 목적**으로 제공됩니다. 실제 운영 환경에서 사용하려면:
1. 머신러닝 모델을 별도로 준비해야 합니다
2. 데이터베이스 설정을 완료해야 합니다
3. 정적 리소스 경로를 환경에 맞게 수정해야 합니다
4. 보안 설정을 강화해야 합니다

### 머신러닝 모델 관련
머신러닝 모델 및 관련 소스는 별도 제작물입니다.
- 관련 문의: 레포지토리 이슈 또는 팀원에게 직접 연락
- 다른 ML 모델을 사용하려면 `MainController.java`의 `ProcessBuilder` 부분 수정 필요

---

## 🔧 설정 예제 (Configuration Example)

### application.yml (전체 설정)
```yaml
server:
  port: 8080

spring:
  datasource:
    driver-class-name: com.mysql.cj.jdbc.Driver
    url: jdbc:mysql://localhost:3306/mainfo
    username: root
    password: your_password_here

  thymeleaf:
    cache: false

  jpa:
    open-in-view: false
    show-sql: true
    hibernate:
      ddl-auto: update
```

### Gradle 빌드 설정
```gradle
plugins {
    id 'java'
    id 'war'
    id 'org.springframework.boot' version '2.7.14'
    id 'io.spring.dependency-management' version '1.0.13'
}

java {
    sourceCompatibility = '11'
}

dependencies {
    implementation 'org.springframework.boot:spring-boot-starter-web'
    implementation 'org.springframework.boot:spring-boot-starter-data-jpa'
    implementation 'org.springframework.boot:spring-boot-starter-thymeleaf'
    implementation 'com.mysql:mysql-connector-j'
}
```

---

## 📸 스크린샷 (Screenshots)

### 홈 페이지
- 반응형 디자인
- 설문 시작 버튼

### 설문조사 페이지
- 17단계 진행률 표시
- 애니메이션 캐릭터
- 단계별 검증

### 결과 페이지
- 개인화된 인사말
- 영양소 정보
- 추천 제품 (3개)

---

## 🏆 특별 감사 (Special Thanks)

- **CodingJoa** - 프로젝트 개발 지원
- **을지대학교 데이터캠퍼스 프로그램** - 프로젝트 기회 제공
- **모든 팀원들** - 데이터 수집, 분석, 개발, 디자인 협력

---

## 📄 라이선스 (License)

이 프로젝트는 교육 및 학습 목적으로 공개되었습니다.
상업적 사용 시 팀원들의 사전 허가가 필요합니다.

---

## 📞 문의 (Contact)

프로젝트 관련 문의사항은 GitHub Issues를 통해 남겨주세요.

---

## 🔗 관련 링크 (Links)

- [Spring Boot Documentation](https://spring.io/projects/spring-boot)
- [Spring Data JPA](https://spring.io/projects/spring-data-jpa)
- [MySQL Documentation](https://dev.mysql.com/doc/)
- [Thymeleaf Documentation](https://www.thymeleaf.org/documentation.html)

---

**Made with ❤️ by HotSix Team @ 2023 Eulji University Datacampus**
