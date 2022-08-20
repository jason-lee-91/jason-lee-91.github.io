---
layout: default
title: CI/CD 구축기
nav_order: 2
description: CI/CD 구축기 
parent: Story
permalink: /story/ci-cd
has_children: true
---
# **CI/CD 구축기**
**since** 2022-08-20
{:.text-right}

---
## 시작하며

---
LoadBalancer 한 서버와 거기에 웹서버를 붙이는 방식으로 작업을 해오며 shell sript를 사용해서

주로 배포 작업을 해오며 사실 그렇게 불편한 부분이 없었지만...

뭔가 시대에 뒤처지는 느낌을 받아 관련된 공부도 할 겸 해서 CI/CD 구축을 진행하기로 했습니다.

첫 회차에는 평소 진행하던 방식의 서버 구성과 중간 목표, 최종 목표에 대한 계획을 작성하고,

순차적으로 블로그를 작성하며 진행하려 했지만..

일을 진행하다 보니 이미 중간 목표까지는 달성한 상태고, 아마 순차적으로 작성했을 때보다는 좀 더,

정리된 느낌으로 공유가 가능할 것 같습니다.

이번 블로그로 사용되는 기술로는 주로 AWS 서비스로 구축되었고, 

운영환경 기반이다 보니 웹서버가 계속 늘어나는 부분을 고려해

중간에 VPC 및 SUBNET 관련해서도 간략하게 진행할 것 같습니다.

사실 CI/CD 구축을 진행하다 보니 테스트가 너무 중요하다 보니 

기존에는 중요한 로직 부분만 검증하던 테스트 방식에서

좀 더 구조라던가 규칙을 잡는 게 좋을 것 같아 테스트 관련 책도 보며 공부를 하고 있어 

테스트 관련 내용을 먼저 블로깅 할 것 같지만,

최종 이후 그리는 그림이 있어 CI/CD 구축기 부분도 열심히 작성하겠습니다.



# 목차

---

 - [CI/CD 구축기 - 도입 설계 및 계획](/story/ci-cd/1)
   - [기반환경](/story/ci-cd/1#기반-환경)
     - [서비스 설명](/story/ci-cd/1#서비스-설명)
   - [중간목표](/story/ci-cd/1#중간-목표)
     - [컨테이너 오케스트레이션(최종)을 바로 사용할 수 없는 이유](/story/ci-cd/1#컨테이너-오케스트레이션최종을-바로-사용할-수-없는-이유)
   - [최종목표](/story/ci-cd/1#최종-목표)
 - [CI/CD 구축기 - 참고자료](/story/ci-cd/dictionary)
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