상품 소스를 기존 SBUI쪽에 머지 하면서 발생한 문제 관련 공유드립니다.
임시로 개발 환경에서 호출 가능하도록 수정했으나, 추가적으로 문제가 있으면  알려주세요

하위 경로를 볼 수 있게 변경  (nginx.conf 수정)
API  경로 수정
=>  기본  경로 http://dev.service-billing.com/ 로 세팅
           (http-common.ts , env.production 수정)


+) 추가로 지금 UI 소스를 보니 
상품에서는 prod/ + api경로
공통에서는 /api/comm/ + api경로로 개발되어있어서 
공통만 kong을 통해 호출되고 상품은 직접 alb 로직으로 분기 호출되는 것으로 보이는데 이 부분도 통일화가 필요해보입니다.

감사합니다
