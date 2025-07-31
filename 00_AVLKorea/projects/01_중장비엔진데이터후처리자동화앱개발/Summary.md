
# Title
STX Engine - Automated Data Processing App

# Overview
========= Korean =======
해당 프로젝트의 프로그램 개발은, STX 엔진 측에서 연소해석기(TestBed), ECS, CAS 등의 오토메이션 측정 장비를 이용한 대상시험에서 계측된 이종간의 Raw 데이터에 대한 데이터 전처리 통합 -> 채널 매핑 -> 데이터 후처리 -> 데이터 시각화 -> MS 툴 리포팅 등의 데이터 분석후처리 자동화 과정이 필요해 시작되었다.

========= English =======
The program development of the project began on the STX engine side as it required data pre-processing integration -> channel mapping -> data post-processing -> data visualization -> MS tool reporting, etc. for harmonization of raw data measured in target tests using automation measurement equipment such as TestBed, ECS, and CAS.

# Tech Stack
AVL CONCERTO SW
Visual Basic / Python 3.9

# System Flow
========= Korean =======
1. 연소해석기(TestBed) 및 ECS 에서 계측되는 엑셀 데이터 와 CAS 다이노 계측오토메이션에서 계측/저장 되는 I-File (AVL 고유형식) 의 데이터 일원화
2. Mapping_window 의 입력값에 따른 필요 채널 파라미터 매핑
3. 채널 파라미터 설정에 따른 로드 조건별 데이터 시각화
4. 시각화데이터 MS Excel 레포트 템플릿에 자동 레포팅

========= English =======
1. Centralize Excel data measured by the Combustion Engine Analyzer (TestBed) and ECS and I-File (AVL-specific format) measured and stored in CAS Dyno measurement automation
2. Mapping necessary channel parameters according to the input value of Mapping_Window
3. Visualization of data by Engine Load condition according to channel parameter settings
4. Automatic reporting visualization data to MS Excel report templates

# UI 
1. Main_window
2. Mapping_window
3. Diagram_window

# Developer Info.
AVL Korea       Sunghyun, Kim
Contact         010-9170-3409
