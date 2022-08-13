---
title: "Commands"
description: "Doks comes with commands for common tasks."
lead: "Doks comes with commands for common tasks."
date: 2020-10-13T15:21:01+02:00
lastmod: 2020-10-13T15:21:01+02:00
draft: false
images: []
menu:
  docs:
    parent: "prologue"
weight: 130
toc: true
---

# GrammarPro API Interface

## Request

- `Host`:TBA
- `Content-Type`application/json
    
    ### key별 정보
    
    | key | type |  | example |
    | --- | --- | --- | --- |
    | text | string | 사용자 입력 텍스트 전문 | Happy families is all alike. Every unhappy family unhappy in its own ways. |
    | model | string | 문법 수정 엔진 (gt 로 고정) | gt |
    
    ### 요청 예시
    
    ```bash
    curl -i -X POST \
    -H "Content-Type:application/json" \
    -d \
    '{
    "text": "Happy families is all alike. Every unhappy family unhappy in its own ways.",
    "model": "gt"
    }' 
    ```
    

## Response

### key 별 정보

| key |  |  | type | info  | example |
| --- | --- | --- | --- | --- | --- |
| details |  |  |  |  |  |
|  | sent_idx |  | int | 문장 인덱스  | 1 |
|  | sentence |  | string | 문장 | Every unhappy family unhappy in its own ways. |
|  | corrected_sentence |  | string | 수정된 문장 | Every unhappy family is unhappy in its own ways. |
|  | errant_result |  | array | 문장 내의 수정사항 내역 (array of maps) | [{’’onset’:0,’offset’:1,error_type:’주어-동사 수일치’…},{’onset’:3,’offset’:7,’error_type:’기타’…},{’onset’:8,’offset’:9,’error_type:’형용사’…}] |
|  |  | onset | int | 시작 단어 인덱스 | onset=2,offset=3이면 문장 내에서 3번째 단어 1개를 의미함; onset=2,offset=5이면 3,4,5번째 단어 총 3개를 의미함  |
|  |  | offset | int | 끝 단어 인덱스 | 3 |
|  |  | error_type | string | 오류 유형 | 주어-동사 수일치 |
|  |  | edit | string | 수정 내용 | is |
|  |  | description | string | 오류 유형에 대한 설명 | 주어가 단수면 주어에 맞는 단수 동사, 주어가 복수이면 주어에 맞는 복수 동사가 나와야 합니다. |
| summary |  |  |  | 텍스트 전체에 대한 종합 평가 결과 | {”cefr_total”:”A2”,”cefr_sentence_structure”:”A1”,”cefr_verb”:”B1”} |
|  | total_level |  | string | CEFR (영어 수준 레벨) 문법 종합 레벨 | A2 |
|  | count |  |  | CEFR 수준별 단어 카운트 |  |
|  | c | A1 | int | A1 수준 단어 개수 | 3 |
|  |  | A2 | int | A2 수준 단어 개수 | 2 |
|  |  | B1 | int | B1 수준 단어 개수 | 1 |
|  |  | B2 | int | B2 수준 단어 개수 | 0 |
|  |  | C1 | int | C1 수준 단어 개수 | 1 |
|  |  | C2 | int | C2 수준 단어 개수 | 4 |
|  |  | cefr_sentence_structure | string | CEFR 기준 문장 구조 수준 | B1 |
|  |  | cefr_verb_use | string | CEFR 기준 동사 활용 수준 | A1 |

### 응답 예시

- 
    
    ```json
    {
       "success":true,
       "data":{
          "details":[
             {
                "idx":0,
                "orig_sentence":"Happy families is all alikes.",
                "corrected_sentence":"Happy families are all alike.",
                "errant_result": [{
                   "onset":2,
                   "offset":3,
    							 "original": "is", 
    	             "correct_onset": 2, 
    	             "correct_offset": 3,
    							 "edit":"are", 
                   "error_type": "R:VERB:SVA",
                   "description":"기타 오류 유형입니다.",
    							 "cefr":"A1"
                },
    						{
                   "onset":4,
                   "offset":5,
    							 "original": "alikes", 
    	             "correct_onset": 4, 
    	             "correct_offset": 5,
    							 "edit":"alike", 
                   "error_type": "R:MORPH",
                   "description":"기타 오류 유형입니다.",
    							 "cefr":"B1"
    	
                }]
             },
             {
                "idx":1,
                "sentence":"Every unhappy family unhappy in its own ways.",
                "corrected_sentence":"Every unhappy family is unhappy in its own ways.",
                "errant_result": [{
                   "onset":3,
                   "offset":3,
    							 "original": "", 
    	             "correct_onset": 3, 
    	             "correct_offset": 4,
    							 "edit": "is", 
                   "error_type": "R:NOUN",
                   "description":"주어가 단수면 주어에 맞는 단수 동사, 주어가 복수이면 주어에 맞는 복수 동사가 나와야 합니다.",
    							 "cefr":"A2"
                }]
             }
          ],
          "summary":{
    			"total_level": "A1",
    	    "total_words": 33,
    	    "count": {
    	      "A1": 21,
    	      "A2": 5,
    	      "B1": 2,
    	      "B2": 3,
    	      "C1": 1,
    	      "C2": 0,
    	      "unk": 1,
    	      "stopwords": 17
    	    },
          "cefr_sentence_structure":"A1",
          "cefr_verb":"B1"
      }
    
       }
    }
    ```
    

## (참고) 오류 유형 (error_type) 종류

|  | error_type |  |
| --- | --- | --- |
| 1 | 형용사 |  |
| 2 | 형용사의 형태 |  |
| 3 | 부사 |  |
| 4 | 접속사 |  |
| 5 | 축약어 |  |
| 6 | 관사 |  |
| 7 | 품사 |  |
| 8 | 명사 |  |
| 9 | 가산/불가산 명사 |  |
| 10 | 명사 단복수 |  |
| 11 | 명사의 소유격 |  |
| 12 | 대/소문자 및 띄어쓰기 |  |
| 13 | 기타 |  |
| 14 | 소사 |  |
| 15 | 전치사 |  |
| 16 | 대명사 |  |
| 17 | 구두점 |  |
| 18 | 철자 |  |
| 19 | 알 수 없는 오류 |  |
| 20 | 동사 |  |
| 21 | 부정사/동명사/현재/과거분사 |  |
| 22 | 시제 |  |
| 23 | 주어-동사 수일치 |  |
| 24 | 동사의 태와 시제 |  |
| 25 | 단어 배열 순서 |  |
