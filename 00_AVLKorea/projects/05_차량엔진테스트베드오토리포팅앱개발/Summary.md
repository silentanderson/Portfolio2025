<<<<<<< HEAD
# AVL_2025_HMC_EngineTestbedAutoReporting
This is the project I have done with HMC E-Motor Team in the part of Data Management Project
=======
Important Notice
This project was develped as part of a contract-based collaboration between HMC and AVL Korea.

⚠️ Usage Warning

This project depends on AVL CONCERTO, a commercial software developed by AVL List GmbH. In order to run this project, AVL CONCERTO must be installed and properly licensed. Without a valid license for AVL CONCERTO, you will not be able to execute or analyze the project files. Unauthorized use or distribution of this project is strictly prohibited.

# Title
Auto-Reporting Tool for Measurements of Engine Dyno Testbed 

# Overview
========= Korean ======== 
엔진 다이노 테스트베드에서 계측되는 엔진 동작시 주요 파라미터의 로그 데이터를 사용자가
핸들링하고, 구간별 분석 하여 계측 시각화를 수행하고, 자동 레포팅까지 하는 후처리 분석기툴을 개발하였습니다.
구체적으로는, 주요 운전 조건별 (Idle, Ramp-Up, Full Load) 파라미터 구간을 분할하여 통계 및 이벤트 기반 지표를 산출하여 결과를 CSV 또는 그래프 형태로 자동 저장합니다.

========= English ======== 
System Overview : This post-processing analysis tool is designed for comprehensive engine dynamometer testbed data management, featuring automated data handling, sectional analysis, measurement visualization, and intelligent reporting capabilities.

Key Features:
- Data Processing: Automated handling of engine operation parameter logs
- Segmental Analysis: Intelligent data segmentation by operating conditions
- Visualization: Advanced measurement data visualization
- Automated Reporting: Streamlined report generation workflow

# Tech Stack
구분                  기술 스택
메인 소프트웨어         AVL CONCERTO SW 5R7 ver. (유효 라이선스 필요)
프로그래밍 언어         Visual Basic 
추가 언어              Python 3.10+

# Main Libraries
데이터 분석
- pandas: 데이터 분석 및 처리
- numpy: 수치 계산
웹 및 네트워크
- requests: HTTP 요청 처리 (웹 기반 데이터 매니지먼트 시스템)
- chardet: 파일 인코딩 자동 감지
설정 관리
- configparser: 구성 파일 처리
표준 라이브러리
- os: 운영체제 인터페이스
- sys: 시스템 관련 기능
- csv: CSV 파일 처리
- shutil: 파일 및 디렉토리 조작
- urllib.parse: URL 파싱
전용 모듈
- concerto: AVL CONCERTO 전용 모듈

# Workflow
1. 데이터베이스 서버 접속
2. UI 기반 데이터 임포트 및 핸들링 (불필요 행 제거)
3. 구간별 자동 통계처리(Averaging, Linear Fitting) or 이벤트 분석
4. 결과 매트릭스 추출 후 csv 저장
5. 계측 메타데이터 표 시각화, 토크-RPM 라인선도, 토크-RPM 막대선도, 토크-RPM 에 따른 BSFC(효율) 컨투어맵 선도 등 시각화
6. 자동 이미지 저장 및 레포팅 

# 프로젝트 구조
HMC_E_Motor/
├── README.md
├── PythonSrc/
│   ├── requirements.txt
│   └── [Python 소스 파일들]
├── Python/
│   └── ComputerScienceStudy/
│       └── engine_analysis_system.py
└── [기타 프로젝트 파일들]
>>>>>>> 4385b7b (First Update all the things)
