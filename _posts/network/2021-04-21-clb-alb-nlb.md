---
published: true
layout: single
title: "AWS CLB, ALB, NLB 비교"
category: Network
tags:
  - AWS
  - ALB
  - Network
comments: true


---

# AWS CLB, ALB, NLB 비교

ELB (Elastic Load Balancer)
=============

> **로드밸런싱**은 하나의 서버에 집중된 요청을 분산시켜 이를 처리하기 위한 부하를 줄이고 인프라 전반적인 자원을 효율적으로 사용할 수 있도록 지원하는 기술이다.
>
> 하나의 서버에 있어 한정된 물리 자원을 활용해야 하는 가상화 기술의 특성을 고려할 때, 로드밸런싱은 가상화 기술의 효과를 극대화 할 수 있는 주요 요소 중 하나다.



#### AWS 에서 로드밸런서를 언제 쓸까?

- 보통 EC2 인스턴스에 붙여서 사용한다.
- 서비스 초기에는 1대의 서버로 감당가능하지만 트래픽의 증가로 CPU나 메모리의 급격한 증가로 서버가 down되는 경우가 발생할때

#### 로드밸런서를 왜 쓸까?

1. 인스턴스를 여러개 사용하고 있는데 한 인스턴스에만 트래픽이 집중되고 다른 인스턴스는 놀고 있을때, 이러한 다량의 트래픽을 여러군데로 분산시키고 싶을 때
2. Single Point of Access (DNS) 를 앱에 제공하기 위해 - 여러 인스턴스가 존재할때 모두 다른 엔드포인트를 갖고있는다면 관리 측면에서 매우 비효율 적이다. 이를 위해 한 곳(로드밸런서)에서 모두 취합하여 인스턴스로 골고루 배분해주는 역할을 한다.
3. 특정 인스턴스가 죽었을때, 서비스의 고가용성을 위해 다른 인스턴스로 트래픽을 넘겨주는 역할
4. Health Check를 위해. 인스턴스의 상태 검사
5. SSL (HTTPS) 를 지원하기 위해



#### 로드밸런서를 어떻게 쓸까?

1. 스케일 **업** 방식
   - 성능을 업그레이드
2. 스케일 **아웃** 방식
   - 서버를 추가하는 것



#### 로드밸런서의 종류

ELB 는 3가지 유형의 로드밸런서를 지원한다.





#### 로드밸런싱 알고리즘의 종류

1. 라운드로빈
2. 가중 라운드 로빈
3. IP해쉬
4. 최소연결방식
5. 최소 리스폰 타임 방식





참고하고 있는 자료

- [대용량 세션을 위한 로드밸런서](https://d2.naver.com/helloworld/605418)

https://m.post.naver.com/viewer/postView.nhn?volumeNo=27046347&memberNo=2521903