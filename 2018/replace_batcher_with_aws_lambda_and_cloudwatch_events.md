---
layout: post
title: 'AWS Lambda + CloudWatch Events로 Batch Job 만들기'
author: robert
date: 2018-06-24 16:42
category : review
tags: [aws lambda,cloudwatch events,batch job, django, data, data architecture]
published: false
---
AWS Lambda + CloudWatch Events로 Batch Job 만들기
===

## 배경

기존에 운영되고 있는 Django RestFrameWork 기반으로 작성된 데이터 처리를 위한 API에서, 시간마다 Cron Job 역할을 수행하던 부분을 AWS Lambda + CloudWatch Events로 대체하였다.

## 적용 순서

1. VirtualEnv생성 Package install
2. AWS Lambda Code 작성
3. Package 및 코드 압축
4. AWS s3 upload
5. AWS Lambda 배포
6. CloudWatch Events Trigger 설정
7. 결과 확인

### VirtualEnv 생성 및 Package install
