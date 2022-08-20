---
layout: default
title: CI/CD 구축기 (1) - 도입 설계 및 계획
nav_order: 1
description: "CI/CD 구축기 - 도입 설계 및 계획"
parent: CI/CD 구축기
grand_parent: Story
permalink: /story/ci-cd/1
---
# **도입 설계 및 계획**
**since** 2022-08-20
{:.text-right}

---
# 목차

---
 - [기반환경](/story/ci-cd/1#기반-환경)
   - [서비스 설명](/story/ci-cd/1#서비스-설명)
 - [중간목표](/story/ci-cd/1#중간-목표)
   - [컨테이너 오케스트레이션(최종)을 바로 사용할 수 없는 이유](/story/ci-cd/1#컨테이너-오케스트레이션최종을-바로-사용할-수-없는-이유)
 - [최종목표](/story/ci-cd/1#최종-목표)

---

## 기반 환경
![start](/assets/images/story/ci-cd/start.jpg)
### 서비스 설명
 - 배치 작업 및 디비 스키마 관리 : celery, celery beat 을 이용한 Admin Service 및 Service 단  배치 작업 및  Django ORM 을 통한 디비 스키마 관리
 - Admin Service
   - Api : FastApi 통한 문서 관리 및 어드민 Api 환경
   - Frontend : Nextjs 통한 프론트엔드 환경
 - Service
   - Django 및 React 기반 환경

## 중간 목표
![mid](/assets/images/story/ci-cd/mid.jpg)
### 컨테이너 오케스트레이션(최종)을 바로 사용할 수 없는 이유
 - 현재 로그를 각 서버에 남기고 있어 완전한 WAS 가 아님 → CLOUD WATCH 반영 예정
 - 테스트 배포(FRONTEND APP 기준) 진행시 시간이 생각보다 오래 걸려 좀더 스터디 필요
 - 현재 도커 환경을 개발 환경으로만 구성해서 사용중인데 환경 변수 처리부분 고민 필요
 - 기존에는 GIT COMMIT 관리를 따로 하지 않아 운영 환경 및 개발 환경 배포 관리 고려된 GIT 전략 도입 필요  → GIT FLOW 반영 예정
 - 기존 재구축시 시간 부족으로 각 사용 기술 버전 업그레이드 필요 → 현재 버전 반영
 - 현재 해당 작업으로 당장은 시간을 더 내기 힘들것 같아 [중간 반영] 으로 버전 업그레이드 및 배포 자동화 동기화
 - 위와 같은 이유로 [최종] 은 계속 변경 될 수 있습니다.

## 최종
![dep](/assets/images/story/ci-cd/dep.jpg)



<br>


<br>
<br>
<br>