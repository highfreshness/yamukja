# [야먹자(머신러닝을 이용한 지역 맛집 지도 서비스)](http://highfreshness.shop/)

<br>

## 프로젝트 소개
머신러닝을 이용한 지역 맛집 지도 서비스	

<br>

## 담당 업무
API 개발 및 배포

<br>

## 사용법

1. 최상단 프로젝트 링크 또는 http://highfreshness.shop 를 통해 메인 페이지 진입
2. 검색어를 입력 후 출발! 버튼을 누른다.
   * 검색어는 지역명을 올바르게 입력해야 합니다. (ex. 영등포구, 중구, 애월읍 등)
   * 현재 서울 모든 구에 대한 데이터는 입력이 되었으나 기타 지역은 속도 문제로 적은 데이터만 가져오고 있습니다.
3. 지도 우측 상단의 openstreetmap 기능을 통해 카테고리별로 음식점이나 주차장을 제외할 수 있습니다.
4. 음식점 아이콘을 클릭하면 음식점의 별점과 분류가 표시되고 자세히 보기를 새 탭에서 열기를 하면 망고플레이트의 해당 음식점 페이지를 확인할 수 있습니다. 

<br>

## 주요 사용 기술

<div align=center>
  <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white"> 
  <img src="https://img.shields.io/badge/Jupyter-F7931E?style=for-the-badge&logo=Jupyter&logoColor=white">
  <img src="https://img.shields.io/badge/Google Colab-F9AB00?style=for-the-badge&logo=Google Colab&logoColor=white">
    <img src="https://img.shields.io/badge/Visual Studio Code-007ACC?style=for-the-badge&logo=Visual Studio Code&logoColor=white">
  <br>
  <br>
  <img src="https://img.shields.io/badge/scikit-learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white">
  <img src="https://img.shields.io/badge/Folium-77B829?style=for-the-badge&logo=Folium&logoColor=white">
  <br>
  <br>
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> 
  <img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white"> 
  <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black">  
  <img src="https://img.shields.io/badge/mongoDB-47A248?style=for-the-badge&logo=MongoDB&logoColor=white">
  <img src="https://img.shields.io/badge/amazonaws-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=FastAPI&logoColor=white">
</div>

<br>  

## 프로젝트 세부 소개
<머신러닝 분류 시스템 개발>
* Selenium, BeautifulSoup을 활용한 데이터 수집
* 이름, 메뉴 등 14개 카테고리 구성 후 220개 raw data 라벨링
* Pandas matplotlib를 활용한 EDA
* MongoDB를 이용한 데이터 저장/추출
* LightGBM 모델을 활용한 분류시스템 개발

<Web Visualization>

* HTML, CSS, 자바스크립트 프론트앤드 개발
* Fast API를 활용한 서버 백엔드 개발
* Folium를 활용 지도를 통해 맛집 시각화서비스 구현

<배포>

* AWS Lightsail을 이용해 웹 배포

[중요하게 생각한 점]
* 맛집의 카테고리 분류를 통한 지도 추가/제외 기능
* 데이터 ETL(Extract, Transform, Load) 속도 최적화

[문제점]
* 유저의 클릭수를 확보할 수 없고 별점만으로 개인화된 추천을 하기 어렵기 때문에  POI(Point of interest) 데이터 기준 설정이 어려운 문제
 > 별점이 높은 순으로 카테고리를 일관되게 분류하여 원하는 종류의 음식만 선택할 수 있도록 지도서비스 구현
* 비지도학습 분류를 할 경우 분류 카테고리가 원하는 대로 나오지 않는 문제
 > 일부 데이터에 직접 라벨링 후 지도 학습으로 전환으로 해결
* 카카오 API 사용 시 특정 구역에 한정된 데이터만 가져오는 문제
 > 카카오API 데이터 포기 후 다른 사이트 데이터로 대체
* 망고플레이트 / 네이버지도 / 카카오맵 데이터 병합 시 Key값으로 설정할만한 컬럼이 존재하지 않는 문제
 > 망고플레이트 데이터만 사용해 프로젝트 진행
* 프론트엔드 환경이 PC마다 다르게 표현
* Selenium 크롤링의 데이터 수집 속도 한계

[후속과제]
* 검색 및 크롤링 속도 추가 최적화 필요
* 반응형 웹페이지 구현 스킬 필요
* 비지도 학습을 위해 대용량 데이터 확보 및 데이터 분할하여 학습 필요



