Important Notice
This project was develped as part of a contract-based collaboration between HMC and AVL Korea.

⚠️ Usage Warning

This project depends on AVL CONCERTO, a commercial software developed by AVL List GmbH. In order to run this project, AVL CONCERTO must be installed and properly licensed. Without a valid license for AVL CONCERTO, you will not be able to execute or analyze the project files. Unauthorized use or distribution of this project is strictly prohibited.

# Title
Auto-Reporting Template for Analysis of Measurements Data from Battery Cell

# Overview
========= Korean ======== 
배터리의 성능을 평가/분석 하기 위해 다량의 배터리 셀에서 계측되는 전류, 전압, 용량 등의 데이터를 이용하여 
사용자가 직접 원하는 셀 계측 사이클 구간에 대한 용량분석, 전력성능, 충방전 효율, DC 내부저항(DC-IR), dQ/dV 및 SOC에 따른 OCV 관계 등의 성능 지표 뿐만 아니라, 베터리 셀 계측 테스트와 관련된 헤더 정보까지 자동으로 레포팅을 해주는 분석자동화 툴 

========= English ======== 
An automated analysis tool that provides automatic reporting of performance indicators such as capacity analysis, power performance, charge/discharge efficiency, DC resistance (DC-IR), dQ/dV, and SOC-OCV relationships for user-selected cell measurement cycle intervals, as well as header information related to battery cell measurement tests, using current, voltage, capacity, and other data measured from a large number of battery cells for battery performance evaluation and analysis.

# Tech Stack
AVL CONCERTO SW 5R7 ver. 
Visual Basic 
Python 3.9

# Main Libraries
Data Analysis: pandas, numpy
Web Requests: requests, chardet
Configuration: configparser
Standard Library: os, sys, csv, shutil, urllib.parse
Custom: concerto (AVL CONCERTO specific module)
자세한 패키지 목록과 버전은 PythonSrc/requirements.txt 파일을 참조하세요.

# Installation
Prerequisites
Python 3.9 이상
AVL CONCERTO SW 5R7 (유효한 라이선스 필요)
Dependencies
이 프로젝트는 다음과 같은 주요 의존성을 가지고 있습니다:

데이터 처리: pandas, numpy를 사용한 데이터 분석 및 처리
웹 요청: requests를 통한 HTTP 요청 처리 (웹기반 데이터매니지먼트 시스템)
인코딩 감지: chardet를 사용한 파일 인코딩 자동 감지
설정 관리: configparser를 통한 구성 파일 처리
전체 의존성 목록과 정확한 버전은 PythonSrc/requirements.txt 파일을 참조하세요.

# Workflow
1. Web 기반 데이터매니지먼트 플랫폼 에서 배터리셀 계측 데이터 다운로드
2. 사용자가 Tag Input UI 상에서 검사항목 선택 (Capacity 용량, Power, dQdV 선도, DC-IR 표, SOC-OCV 표)
3. 사용자가 각 검사항목에 대한 사이클 구간을 커서를 이용하여 직접 인터랙티브하게 선정
4. 검사항목에 해당하는 보고서 템플릿 선택적 시각화
