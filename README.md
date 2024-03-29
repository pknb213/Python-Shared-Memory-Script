# Python Shared Memory Script

## 개요
2019년도 뉴로메카에서 작성한 협동 로봇 원격 모니터링 상용 웹 서비스인 IndyCARE-React 버전에 사용된 공유 메모리 스크립트입니다. 

## Overview
It is a robot battlefield memory control script store that visualizes data in conjunction with the IndyCARE React page, written in Python3 by Neuromeka on 2019.

## 기술 스택
- Shared Memory, python, react

## 로직
협동 로봇은 RTOS가 설치된 컨트롤러 박스에서 다중 프로세스를 4000hz 무결성으로 동작하게 됩니다. \
그와 동시에 py-installer로 설치된 해당 스크립트가 같이 돌아가게 되고 \
React로 작성된 웹 페이지에서 서버 사이드 동작이 요청되면 \
공유 메모리 스크립트가 수행되고 http로 데이터를 전달합니다.

## 기능
웹 사이트에 전달하게되는 기능은 다음과 같습니다.
1. 각 축의 속도, 가속도, 위치 그리고 축 회전율을 비롯한 로봇 Status.
2. 로봇 웹 캠에 부착된 준실시간 영상.
3. 에러 로그 및 에러 발생 시점의 영상.
4. 펌웨어 업데이트
