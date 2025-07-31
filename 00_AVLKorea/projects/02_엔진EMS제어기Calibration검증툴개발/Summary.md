
## Important Notice
This project was develped as part of a contract-based collaboration between HMC (Hyundai Motor Company) and AVL Korea.

⚠️ **Usage Warning**
- This project depends on **AVL CONCERTO**, a commercial software developed by AVL List GmbH.
- In order to run this project, **AVL CONCERTO must be installed** and properly licensed.
- Without a valid license for AVL CONCERTO, you will not be able to execute or analyze the project files.
- Unauthorized use or distribution of this project is strictly prohibited.

# Title
HMC - Engine Control Verification Tool 

# Overview
========= Korean ========
현대자동차와의 용역과제를 통해 개발된 것으로 표준화된 자동 분석 프로그램을 통해 업무의 효율을 증진시키고 품질 향상에 기여하고자 하는 목적으로 개발되었다.
특히, EMS (Engine Management System) 개발을 위해 실도로 주행 테스트를 진행하며 EMS 의 Calibration 품질을 검증확인할 수 있는 자동 데이터 후처리 SW 가 필요했으며, 구체적으로는 차량 주행데이터 읽기, 트리거 및 이벤트 감지, 보고서 시각화 등이 자동화가 이뤄졌다. 

========= English ========
It was developed through a service task with Hyundai Motor Company and was developed for the purpose of enhancing work efficiency and contributing to quality improvement through a standardized automatic analysis program.
In particular, for the development of EMS (Engine Management System), automatic data post-processing software was needed to verify calibration quality of EMS by conducting real-road driving tests, and specifically automatic post-processing was made to import vehicle driving data, detect triggers and events, and visualize reports.

# Task 
========= Korean ========
해당 툴의 개발이 된 이후 유지보수 단계에서 투입되어, 버그픽스, 코드디버깅, 새버젼 릴리즈 등의 업무를 맡아,
총 8번의 버젼 업데이트 및 배포를 수행하였다.

========= English ========
After the development of the tool, it was put in the maintenance stage and took charge of bug fixes, code debugging, and new version releases, and performed a total of eight version updates and distributions.

# Tech Stack
AVL CONCERTO SW 5R5
Visual Basic
Python 3.9
- numpy
- pprint
- typing

# System Flow
========= Korean ========
1. 차량 VDMS (Vehicle and Driver Management System) 및 INCA S/W 에서 수집된 .mdf or .dat 파일 데이터 수집
2. Calibration 매핑파일 .dcm 데이터 수집
3. Base Mapping, Emission, Startability&Drivability, OBD 등의 엔진 칼리브레이션 검사항목 및 range / Trigger / Diagram 조건 입력
4. 시그널 리샘프링 => range 필터 => 이벤트 감지 (Rising, Falling, Min, Max, Debouncing) => 후처리결과 어레이 재정렬
5. 이벤트 탐지 분석 시각화 및 자동레포팅

========= English ========
1. Collect .mdf or .dat file data collected from Vehicle and Driver Management System (VDMS) and INCAS/W
2. Calibration mapping file .dcm data collection
3. Enter engine calibration inspection items such as Base Mapping, Emission, Startability&Drivability, OBD, and range/trigger/diagram conditions
4. Signal resampling => range filter => event detection (Rising, Falling, Min, Max, Debouncing) => Rearranging postprocessing results array
5. Visualize and automatically report event detection analysis

# UI 
1. About                    Tool 버젼이력관리
2. Main                     프로젝트입력, 차량데이터 입력, 칼리브레이션데이터 입력, 검증 검사항목 입력, Configuration 설정 등
3. Plot                     리포트 시각화 화면 관리
4. Convert Excel to ini     Configuration 변환 : Excel 형식 -> ini 형식
5. Convert ini to Excel     Configuration 변환 : ini 파일 -> Excel 형식
6. Change Font              Font 적용

# Developer Info.
AVL Korea       Sunghyun, Kim
Contact         010-9170-3409