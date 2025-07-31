

# Important Notice
This project was develped as part of a contract-based collaboration between HD Hyundai Infracore and AVL Korea.

⚠️ Usage Warning

This project depends on AVL CONCERTO, a commercial software developed by AVL List GmbH.
In order to run this project, AVL CONCERTO must be installed and properly licensed.
Without a valid license for AVL CONCERTO, you will not be able to execute or analyze the project files.
Unauthorized use or distribution of this project is strictly prohibited.

# Title
Data Analytics Template Development for Heavy Industry Engine

# Overview
========= Korean ======== 
중형선박 엔진 개발에서 취득되는 엔진 제어기 데이터와 내연기관 연소해석 데이터를 Load 조건별 효율적인 데이터분석을 위해 오토리포팅 템플릿을 개발하였습니다.
특히, 서로 다른 파일포맷의 데이터 (.tdms and .xlsx) 를 일원화하고 간단한 채널 매핑, 통계정보 시각화, 관심데이터 필터링, 연소해석 Raw 데이터의 로그포이트 기반 -> 크랭크축 기반 변환 알고리즘, 바 차트, 박스 플롯, 인터랙티브 차트 등을 구현하여 손쉽게 중장비 엔진 테스트베드의 데이터를 분석,시각화,레포팅 할 수 있는 툴을 개발하였습니다.

========= English ======== 
For efficient data analysis of engine controller data and internal combustion analysis data obtained from heavy ship engine development, an auto reporting template was developed for each load condition.
In particular, I developed a tool that can easily analyze, visualize, and report data on heavy equipment engine testbeds by unifying data from different file formats (.tdms and .xlsx) and implementing simple channel mapping, statistical visualization, data filtering of interest, and logpoint-based to crank-angle based conversion algorithm, bar charts, box plots, and interactive charts of Raw data.

# Tech Stack
AVL CONCERTO SW 5R7 ver.
Visual Basic 
Python 3.9

## Main Libraries
- **Data Analysis**: pandas, numpy, scipy, scikit-learn, polars
- **Visualization**: matplotlib, seaborn, plotly, streamlit
- **File Processing**: asammdf, npTDMS, openpyxl, XlsxWriter
- **Database**: cx-Oracle, oracledb, mysql-connector-python
- **GUI**: customtkinter, PyAutoGUI
- **Web Framework**: fastapi, uvicorn, starlette

*자세한 패키지 목록과 버전은 `PythonProgram/Scripts/requirements.txt` 파일을 참조하세요.*

# Installation

## Prerequisites
- Python 3.9 이상
- AVL CONCERTO SW 5R7 (유효한 라이선스 필요)

# Dependencies
이 프로젝트는 다음과 같은 주요 의존성을 가지고 있습니다:

- **데이터 처리**: pandas, numpy, scipy를 사용한 데이터 분석 및 처리
- **시각화**: matplotlib, seaborn, plotly를 통한 차트 및 그래프 생성
- **파일 처리**: asammdf(.mdf), npTDMS(.tdms), openpyxl(.xlsx) 등 다양한 파일 형식 지원
- **데이터베이스**: Oracle, MySQL 연결 지원
- **웹 인터페이스**: FastAPI와 Streamlit을 통한 웹 기반 UI
- **GUI**: customtkinter를 사용한 데스크톱 애플리케이션

전체 의존성 목록과 정확한 버전은 [`PythonProgram/Scripts/requirements.txt`](PythonProgram/Scripts/requirements.txt) 파일을 참조하세요.

# UI
1. Data Input
    a. Each measurements data should be imported by button or writing manual path
        (Engine Controller data – excel format & Combustion Pressure data – tdms format)
    b. Users have to put in the engine’s specifications by UI.
    
2. Channel Mapping
    a. Filtering table should be developed including source (raw files) & target (selected channels) data
    b. Drop down filtering (combo box) for source category
    c. Drop down filtering (combo box) for source specific measurement file 
    d. Display average values for each channels
    
3. Data Monitoring
    a. Box plot should be visualized for Engine Load, Engine RPM, Boost Air Pressure, Boost Air Temp, Gas Temp, Pmax based on each Test Condition
    b. Line plot should be visualized for Combustion Pressure based on Crank Angle based
    c. Users have to check the specific value when selecting the cursor

4. Server Transfer
    a. Display if each channels in the target data are uploaded(or saved) well
