---
layout: default
title: CI/CD 구축기 - 참고자료
nav_order: 10
description: "CI/CD 구축기 - 참고자료"
parent: CI/CD 구축기
grand_parent: Story
permalink: /story/ci-cd/dictionary
---
# **참고자료**
**since** 2022-08-20
{:.text-right}

---
# 목차

---
 - [환경](/story/ci-cd/dictionary#환경)
   - [AWS ELB(Elastic Load Balancing)](/story/ci-cd/dictionary#aws-elbelastic-load-balancing)
   - [AWS EC2(Amazon Elastic Compute Cloud)](/story/ci-cd/dictionary#aws-ec2amazon-elastic-compute-cloud)
   - [AWS Route 53](/story/ci-cd/dictionary#aws-route-53)
   - [AWS ElasticCache(Redis)](/story/ci-cd/dictionary#aws-elasticcacheredis)
   - [AWS S3(Amazon Simple Storage Service)](/story/ci-cd/dictionary#aws-s3amazon-simple-storage-service)
   - [GIT](/story/ci-cd/dictionary#git)
   - [BITBUCKET(GIT)](/story/ci-cd/dictionary#bitbucketgit)
   - [JENKINS](/story/ci-cd/dictionary#jenkins)
   - [Amazon CloudWatch](/story/ci-cd/dictionary#amazon-cloudwatch)
   - [AWS Fargate](/story/ci-cd/dictionary#aws-fargatehttpsdocsawsamazoncomko_kramazonecslatestuserguidewhat-is-fargatehtml)
   - [Docker](/story/ci-cd/dictionary#docker)
   - [Amazon ECR(Amazon Elastic Container Registry)](/story/ci-cd/dictionary#amazon-ecramazon-elastic-container-registry)
   - [Amazon ECS(Amazon Elastic Container Service)](/story/ci-cd/dictionary#amazon-ecsamazon-elastic-container-service)
 - [언어](/story/ci-cd/dictionary#언어)
   - [Python](/story/ci-cd/dictionary#python)
   - [Javascript](/story/ci-cd/dictionary#javascript)
   - [Typescript](/story/ci-cd/dictionary#typescript)
   - [React](/story/ci-cd/dictionary#react)
   - [Html](/story/ci-cd/dictionary#html)
 - [FRAMEWORK](/story/ci-cd/dictionary#framework)
   - [Django](/story/ci-cd/dictionary#djangohttpswwwdjangoprojectcom)
   - [FastAPI](/story/ci-cd/dictionary#fastapihttpsfastapitiangolocomko)
   - [NextJs](/story/ci-cd/dictionary#nextjshttpsnextjsorg)
 - [참고자료](/story/ci-cd/dictionary#참고자료)
   - [GIT FLOW](/story/ci-cd/dictionary#git-flow)
   - [EKS (쿠버네티스) or ECS(Docker)](/story/ci-cd/dictionary#eks-쿠버네티스-or-ecsdocker)
   - [CloudWatch Log With Django](/story/ci-cd/dictionary#eks-쿠버네티스-or-ecsdocker)

---

## 환경

---

### AWS ELB(Elastic Load Balancing)

- 서비스단 트래픽 분산
- Elastic Load Balancing(ELB)은 하나 이상의 가용 영역(AZ)에 있는 여러 대상 및 가상 어플라이언스에서 들어오는 애플리케이션 트래픽을 자동으로 분산합니다.

### AWS EC2(Amazon Elastic Compute Cloud)

- 클라우드 환경 웹서버
- 500개가 넘는 인스턴스, 그리고 최신 프로세서, 스토리지, 네트워킹, 운영 체제 및 구매 모델의 옵션과 함께 워크로드의 요구 사항에 가장 잘 부합할 수 있도록 가장 포괄적이고 심층적인 컴퓨팅 플랫폼을 제공

### AWS Route 53

- Amazon Route 53는 높은 가용성과 확장성이 뛰어난 클라우드 [Domain Name System (DNS)](https://aws.amazon.com/ko/route53/what-is-dns/) 웹
  서비스
- 최종 사용자를 인터넷 애플리케이션으로 라우팅할 수 있는 매우 안정적이고 비용 효율적인 방법을 개발자와 기업에 제공하기 위해 설계

### AWS ElasticCache(Redis)

- Web Cache, Celery 및 Celery beat 을 이용한 비동기 처리 시 사용
- Amazon ElastiCache는 유연한 실시간 사용 사례를 지원하는 완전관리형 인 메모리 캐싱 서비스
- [캐싱](https://aws.amazon.com/caching/)에 ElastiCache를 사용하면 애플리케이션 및 데이터베이스 성능을 가속화할 수 있으며, 세션 스토어, 게임 리더보드, 스트리밍 및 분석과
  같이 내구성이 필요하지 않는 사용 사례에서는 기본 데이터 스토어로 사용 가능
- ElastiCache는 Redis 및 Memcached와 호환 가능

### AWS S3(Amazon Simple Storage Service)

- 확장성, 데이터 가용성, 보안 및 성능을 제공하는 객체 스토리지 서비스
- 고객은 규모와 업종에 관계없이 원히는 양의 데이터를 저장하고 보호하여 데이터 레이크, 클라우드 네이티브 애플리케이션 및 모바일 앱과 같은 거의 모든 사용 사례를 지원
- 비용 효율적인 스토리지 클래스와 사용이 쉬운 관리 기능을 통해 비용을 최적화하고, 데이터를 정리하고, 세분화된 액세스 제어를 구성하여 특정 비즈니스, 조직 및 규정 준수 요구 사항을 충족

### GIT

- 깃은 컴퓨터 파일의 변경사항을 추적하고 여러 명의 사용자들 간에 해당 파일들의 작업을 조율하기 위한 분산 버전 관리 시스템

### BITBUCKET(GIT)

- 빗버킷은 아틀라시안 소유의 웹 기반 버전 관리 저장소 호스팅 서비스
- 깃 버전 관리 시스템을 사용하는 소스 코드 및 개발 프로젝트를 대상

### JENKINS

- 소프트웨어 개발 시 지속적 통합 서비스를 제공하는 툴
- 다수의 개발자들이 하나의 프로그램을 개발할 때 버전 충돌을 방지하기 위해 각자 작업한 내용을 공유 영역에 있는 Git등의 저장소에 빈번히 업로드함으로써 지속적 통합이 가능하도록 해 준다.
- MIT 라이선스를 따른다.

### Amazon CloudWatch

- DevOps 엔지니어, 개발자, 사이트 안정성 엔지니어(SRE), IT 관리자 및 제품 소유자를 위해 구축된 모니터링 및 관찰 서비스
- 애플리케이션을 모니터링하고 시스템 전체 성능 변경에 대응하며 리소스 사용률을 최적화하는 데 필요한 데이터와 실행 가능한 인사이트를 제공
- 모니터링 및 운영 데이터를 로그, 지표 및 이벤트 형태로 수집
- 운영 상태를 통합적으로 보고 AWS 및 온프레미스에서 실행되는 AWS 리소스, 애플리케이션 및 서비스를 완벽하게 파악
- 환경에서 이상 동작을 감지하며, 경보를 설정하고, 로그와 지표를 나란히 시각화하며, 자동화된 작업을 수행하고, 문제를 해결하며, 인사이트를 확보하여 애플리케이션을 원활하게 실행

### AWS Fargate**([https://docs.aws.amazon.com/ko_kr/AmazonECS/latest/userguide/what-is-fargate.html](https://docs.aws.amazon.com/ko_kr/AmazonECS/latest/userguide/what-is-fargate.html))

- Amazon EC2 인스턴스의 서버나 클러스터를 관리할 필요 없이 [컨테이너](http://aws.amazon.com/what-are-containers)를 실행하기 위해 Amazon ECS에 사용할 수 있는
  기술
- Fargate를 사용하면 더 이상 컨테이너를 실행하기 위해 가상 머신의 클러스터를 프로비저닝, 구성 또는 조정할 필요가 없습니다.
- 서버 유형을 선택하거나, 클러스터를 조정할 시점을 결정하거나, 클러스터 패킹을 최적화할 필요가 없습니다.

### Docker

- 도커는 리눅스의 응용 프로그램들을 프로세스 격리 기술들을 사용해 컨테이너로 실행하고 관리하는 오픈 소스 프로젝트
- 도커 컨테이너는 일종의 소프트웨어를 소프트웨어의 실행에 필요한 모든 것을 포함하는 완전한 파일 시스템 안에 감싼다.

### Amazon ECR(Amazon Elastic Container Registry)

- 어디서나 애플리케이션 이미지 및 아티팩트를 안정적으로 배포할 수 있도록 뛰어난 성능 호스팅을 제공하는 완전관리형 컨테이너 레지스트리

### Amazon ECS(Amazon Elastic Container Service)

- 컨테이너화된 애플리케이션의 손쉬운 배포, 관리 및 크기 조정을 지원하는 완전관리형 컨테이너 오케스트레이션 서비스

## 언어

---

### Python

- 파이썬은 1991년 네덜란드계 프로그래머인 귀도 반 로섬이 발표한 고급 프로그래밍 언어로, 플랫폼에 독립적이며 인터프리터식, 객체지향적, 동적 타이핑 대화형 언어
- 파이썬이라는 이름은 귀도가 좋아하는 코미디인〈Monty Python's Flying Circus〉에서 따온 것

### Javascript

- 자바스크립트는 객체 기반의 스크립트 프로그래밍 언어
- 다른 응용 프로그램의 내장 객체에도 접근할 수 있는 기능
- 또한 Node.js와 같은 런타임 환경과 같이 서버 프로그래밍에도 사용

### Typescript

- 타입스크립트는 자바스크립트의 슈퍼셋인 오픈소스 프로그래밍 언어
- 마이크로소프트에서 개발, 유지하고 있으며 엄격한 문법을 지원
- C#의 리드 아키텍트이자 델파이, 터보 파스칼의 창시자인 Anders Hejlsberg가 개발에 참여

### React

- 리액트는 자바스크립트 라이브러리의 하나로서 사용자 인터페이스를 만들기 위해 사용
- 페이스북과 개별 개발자 및 기업들 공동체에 의해 유지보수
- 리액트는 싱글 페이지 애플리케이션이나 모바일 애플리케이션 개발에 사용

### Html

- 하이퍼 텍스트 마크업 언어는 웹 페이지 표시를 위해 개발된 지배적인 마크업 언어
- HTML은 제목, 단락, 목록 등과 같은 본문을 위한 구조적 의미를 나타내는 것뿐만 아니라 링크, 인용과 그 밖의 항목으로 구조적 문서를 만들 수 있는 방법을 제공

## FRAMEWORK

---

### Django([https://www.djangoproject.com/](https://www.djangoproject.com/))

- 장고는 파이썬으로 작성된 오픈 소스 웹 프레임워크로, 모델-뷰-컨트롤러 패턴을 따름
- 장고 소프트웨어 재단에 의해 관리
- 고도의 데이터베이스 기반 웹사이트를 작성하는 데 있어서 수고를 더는 것이 장고의 주된 목표

### FastAPI([https://fastapi.tiangolo.com/ko/](https://fastapi.tiangolo.com/ko/))

- 현대적이고, 빠르며(고성능), 파이썬 표준 타입 힌트에 기초한 Python3.6+의 API를 빌드하기 위한 웹 프레임워크
- (Starlette과 Pydantic 덕분에) **NodeJS** 및 **Go** 와 대등할 정도로 매우 높은
  성능. [사용](https://fastapi.tiangolo.com/ko/#performance) [가능한 가장 빠른 파이썬 프레임워크 중 하나](https://fastapi.tiangolo.com/ko/#performance)
- 약 200%에서 300%까지 기능 개발 속도 증가
- 사람(개발자)에 의한 에러 약 40% 감소
- 훌륭한 편집기 지원. 모든 곳에서 자동완성. 적은 디버깅 시간
- 쉽게 사용하고 배우도록 설계. 적은 문서 읽기 시간
- 코드 중복 최소화. 각 매개변수 선언의 여러 기능. 적은 버그
- 준비된 프로덕션 용 코드를 얻으십시오. 자동 대화형 문서와 함께
- API에 대한 (완전히 호환되는) 개방형 표준 기반: [OpenAPI](https://github.com/OAI/OpenAPI-Specification)(이전에 Swagger로 알려졌던)
  및 [JSON 스키마](http://json-schema.org/)

### NextJs([https://nextjs.org/](https://nextjs.org/))

- 서버 사이트 렌더링, 정적 웹 페이지 생성 등 리액트 기반 웹 애플리케이션 기능들을 가능케 하는 Node.js 위에서 빌드된 오픈 소스 웹 개발 프레임워크

## 참고자료

---

- ### GIT FLOW
- ### EKS (쿠버네티스) or ECS(Docker)
- ### CloudWatch Log With Django

~~~
    boto3_logs_client = boto3.client("logs", region_name=AWS_REGION_NAME,
                                     aws_access_key_id=AWS_ACCESS_KEY_ID, aws_secret_access_key=AWS_SECRET_ACCESS_KEY)
        
    LOGGING = {
        'version': 1,
        'disable_existing_loggers': False,
        'root': {
            'level': 'DEBUG',
            'handlers': ['watchtower'],
        },
        'formatters': {
            'aws': {
                # 여기에서 AWS에 대한 특정 포맷을 추가할 수 있다.
                # 포맷을 변경하려면 다음을 참고 한다.
                # https://stackoverflow.com/questions/533048/how-to-log-source-file-name-and-line-number-in-python/44401529
                'format': """{"time": "%(asctime)s", "file" : "%(pathname)s", "line":%(lineno)d , "log":"%(message)s" }""",
                'datefmt': "%Y-%m-%d %H:%M:%S"
            },
        },
        'handlers': {
            'console': {
                'class': 'watchtower.CloudWatchLogHandler',
                'boto3_client': boto3_logs_client,
                'log_group_name': 'kukka-service',
                'level': 'DEBUG'
            },
            'watchtower': {
                'class': 'watchtower.CloudWatchLogHandler',
                'boto3_client': boto3_logs_client,
                'log_group_name': 'kukka-service',
                'log_stream_name': "{logger_name}",
                'level': 'DEBUG',
                'formatter': 'aws',  # 앞에서 생성한 format
            }
        },
        'loggers': logger
    }
~~~