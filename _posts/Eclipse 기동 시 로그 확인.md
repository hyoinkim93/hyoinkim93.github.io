---
layout: post
comments: true
title: test
categories: [TIL]
---


## Eclipse 기동 시 로그 확인 방법

RSA을 사용하는 중 플러그인 프로젝트만 import하면 자꾸 종료되는 문제 발생

- exit code -1 또는 13을 보이며 종료 
 -> 이전에 rsa 기동하는 jdk를 변경하면서 테스트 한 경험이 있어 이거 때문에 파일이 손상되었나? 생각함 (-1과 13은 주로 jdk관련 문제임)
 -> 하지만 import하지 않았을 때 또는 다른 workspace를 사용했을 때, 해당 문제는 발생하지 않았다..!

- 로그 보기
 -> workspace/.metadat/.log 파일을 확인했지만 관련 로그 전무
 -> 이클립스에서 오류로그 창을 확인하려니 기동자체가 불가능하므로 확인 불가
 -> cmd창을 켜서 이클립스 기동 시작하였으나 이클립스와 동시에 명령프롬프트창도 꺼짐.
 -> 기동 옵션 -consoleLog -debug추가했지만 여전히 꺼져서 파일에 로그 남김
```yaml
eclipse.exe -consoleLog -debug > log.txt
```

: 결국은 RSA설치 시 PDE항목을 빼먹고 설치한 거여서 5시간에 걸친 재설치 엔딩..^^..(이클립스 내 플러그인 프로젝트 자체가 생성이 안되고 플러그인 개발관련 창에 에러 뜸)...
