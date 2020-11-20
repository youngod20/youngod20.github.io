---
title: "if(kakao)_Click House"
excerpt: "Click House 내용 정리"

categories:
  - DB
tags:
  - DB
---

# Click House APL 2.0
#### 1 -> 2로 변경하며, 분석용 DB에서 중요하지 않은 기능을 축소함
#### 1. Apache Druid - aggregated
#### 2. ClickHoust - Non aggregated

### (1) Vectorized processing: 한 번에 여러가지 연산 가능
#### - SIMD(single instruction Multiple Data)
#### - x86 SSE*(한번에 4개의 정수를 더할 수 있음, 4배 빠름), AVX 명령어 집합
#### - tet parsing, data filtering, 
### (2)  MergeTree: DB 테이블 생성에서 사용됨
#### - 여러개 테이블 엔진 지원 : 데이터 조회 저장 방식 결정
#### - 파티션, 정렬
#### - 하나의 파티션은 여러개의 파트로 저장됨
#### - 파트로 나눠진 데이터를 한번에 불러올때 저장공간을 고려해서 자동으로 merge해서 가져옴
### (3) Primary Index
#### - 파티션 안에 primary index의 위치만 스캔함
### (4) Data Skipping Index
#### - 블룸 필터: 집합의 원소의 포함여부를 결정하는 사용구조(hash값을 찾고 각 블룸필터의 bit값이 참인지 판단) => set, minmax 등 다양한 것 있음

## [분산 시스템 관점]
### (1) Replication(복제)
#### - 데이터 유실이 우려된다면 인설트 쿼럼? 참조
#### - Asynchronous: REP1로 데이터를 보내면 백그라운드에서 REP2로 보냄, 바로 REP2에서 데이터를 #### 요청하는 경우 없을 수도 있음
#### - Multi-master: 복제에 참여하는 모든 멤버가 데이터를 추가 할 수 있음. 데이터 압축, 압축된 데이터를 #### 카피함(복제)
#### - Fault  tolrerent
### (2) Distributed Processing
#### - Cluster는 여러개의 shard에 나눠서 저장 
#### - 분산 쿼리는 여러개의 shard에서 데이터를 모아서 제공함
#### - 쿼리 받은 샤드: Initiator Node > 모든 샤드에게 전달
#### - 로컬리하게 집계해서 중간단계 만들고 initiator Node에게 전달 > 사용자에게 전달

## [데이터 분석 관점]
### (1) Funnel Analysis
#### - 일련의 이벤트 단계별로 분석이 가능함
#### - 이벤트 화면(50%) > 추천상품(30%) > 구매완료
#### - 뒤로 갈수록 사용자가 줄어들어서 깔때기 모양이 됨

```
####  SELECT windowFunnel(3600):  이벤트 시간 윈도우
####  (date, 시간기준
####   action = '이벤트 화면', 행동 정의
####   action = '추천 상품',
####   action = '구매완료'
####  )
#### FROM ActionLog
#### GROUP BY id
```