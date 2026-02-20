# 🧠 CISP : AI 경찰 수사 지원 시스템

<img src="img/thumbnail.png" width="100%">


## 📌 프로젝트 개요

본 프로젝트는 수사 과정에서 생성되는 비정형 데이터(음성 진술, 자필 진술서, 문서, 영상 등)를 통합 분석하여 수사관의 판단을 지원하는 
**AI 기반 지능형 수사 지원 시스템**입니다.

기존 수사 시스템은 기록 관리 및 단순 검색 중심의 기능에 머물러 있어,
대량의 진술서, 녹취, 영상 자료를 수작업으로 검토해야 하는 한계가
존재합니다.

본 시스템은 STT, OCR, LLM, RAG, 멀티모달 분석 기술을 결합하여 사건의
맥락을 자동으로 구조화하고, 사실관계 분석 및 추가 조사 포인트를 도출하는
것을 목표로 합니다.

---

## 🎯 개발 목적

수사 업무는 조사관 개인의 경험과 역량에 의존하는 비중이 높아 동일·유사 사건 간 판단 편차가 발생할 수 있으며, 비정형 수사 자료의 수작업 검토로 인해 시간 지연 및 업무 부담이 증가하는 문제가 있습니다.

본 프로젝트는 다음과 같은 목적을 달성하기 위해 개발되었습니다.

-   비정형 수사 데이터의 자동 구조화 및 통합 분석
-   사건 요지 및 핵심 쟁점 자동 도출
-   진술 간 모순 및 누락 정보 탐지
-   추가 심문 및 조사 질문 추천
-   설명 가능한 AI 기반 수사 판단 지원

---

## 🛠️ 기술 스택

### Front End

![TypeScript](https://img.shields.io/badge/typescript-%23323330.svg?style=for-the-badge&logo=typescript&logoColor=%233178C6)
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![vite](https://img.shields.io/badge/vite-%239135FF?style=for-the-badge&logo=vite&logoColor=white)

### Back End

![Java](https://img.shields.io/badge/java-ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)
![SpringBoot](https://img.shields.io/badge/springboot-%2320232a.svg?style=for-the-badge&logo=springboot&logoColor=%236DB33F)
![SpringSecurity](https://img.shields.io/badge/springsecurity-%2320232a.svg?style=for-the-badge&logo=springsecurity&logoColor=%236DB33F)
![PostgreSQL](https://img.shields.io/badge/postgresql-4169E1.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![JWT](https://img.shields.io/badge/jsonwebtokens-000000.svg?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

### AI

![Python](https://img.shields.io/badge/python-%2320232a.svg?style=for-the-badge&logo=python&logoColor=3776AB)
![FastAPI](https://img.shields.io/badge/fastapi-%23009688.svg?style=for-the-badge&logo=fastapi&logoColor=white)
![LangChain](https://img.shields.io/badge/langchain-%231C3C3C.svg?style=for-the-badge&logo=langchain&logoColor=white)
![HuggingFace](https://img.shields.io/badge/huggingface-%2320232a.svg?style=for-the-badge&logo=huggingface&logoColor=FFD21E)
![Pytorch](https://img.shields.io/badge/pytorch-%2320232a.svg?style=for-the-badge&logo=pytorch&logoColor=EE4C2C)
![OpenCV](https://img.shields.io/badge/opencv-5C3EE8.svg?style=for-the-badge&logo=opencv&logoColor=white)

---

## 🧩 주요 기능

### 1. 멀티모달 데이터 수집 및 처리

-   음성 진술(STT)
-   자필 진술서 및 문서(OCR)
-   영상(CCTV, 블랙박스)
-   텍스트 수사 기록

### 2. 진술 데이터 구조화 분석 (LLM)

-   사건 요약 자동 생성
-   시간 흐름 정리
-   핵심 사실 및 주장-근거 구조화
-   주요 쟁점 도출

### 3. 법령·판례 기반 RAG 분석

-   법령 및 판례 데이터 연동
-   사건 유형별 법리적 쟁점 분석
-   근거 기반 수사 판단 지원

### 4. 심문 및 조사 지원 기능

-   진술 내용 간 모순 탐지
-   누락 정보 자동 식별
-   추가 질문 및 심문 전략 추천

### 5. 자동 수사 리포트 생성

-   사건 요약
-   증거 목록
-   진술 분석 결과
-   쟁점 및 판단 근거 포함 리포트 자동 생성

### 6. 영상 기반 대화형 분석

-   CCTV 및 영상 데이터를 기반으로 자연어 질의응답 제공
-   특정 시간 구간 및 이벤트 설명
-   영상 분석 결과 기반 추가 질문 응답
---

## ⚙️ 시스템 핵심 구성

-   STT 모델: 음성 진술 교차 분석 및 모순 도출
-   LMM (Large Multimodal Model): CCTV 등 영상자료 + 진술서 등 수사자료 분석
-   LLM: 분석 결과 기반 보고서 작성
-   RAG(Vector DB): 법령 및 유사사건 판례 기반 검색 분석
-   Web-Backend 서버: API 및 서비스 관리
-   AI 서버: 모델 추론 및 분석 처리

---

## 📊 기대 효과

-   수사 판단의 객관성 및 일관성 향상
-   조사관 반복 업무 감소 및 업무 효율 증대
-   대량 수사 자료의 신속한 분석 지원
-   설명 가능한 AI 기반 수사 행정 체계 구축

---

## 🏛️ 적용 대상

-   검찰 등 수사기관 (B2G)
-   대한민국 경찰청 (B2G)

---

## 서비스 배포 아키텍처

<img src="img/aws-architecture.png" width="100%">

---

### 🧾 한 줄 설명

> 비정형 수사 데이터를 AI로 구조화·분석하여 사건의 맥락 이해와 수사
> 판단을 지원하는 지능형 수사 분석 플랫폼
