
---
layout: post
comments: true
title: Oracle TNS 
categories: [TIL]
---


프로젝트에서 Orange에 냅다 로그인만 해주고 DB 접속 정보를 안알려주었다..!
TNS로 로그인했길래 정보를 어디서 찾는지 헤맴.

TNS(Transparent Network Substrate)란?
Oracle Database에서 클라이언트와 서버 간의 통신을 관리하는 네트워크 프로토콜. TNS는 Oracle 데이터베이스에 연결하기 위한 기본 구성 요소이며, 이를 통해 클라이언트 애플리케이션이 데이터베이스 서버와 통신할 수 있도록 설정됨.

로컬경로 oracle/버전정보/network/admin/tnsnames.ora 에 해당 TNS의 이름만 검색해보면 간단히 찾기 완료.
