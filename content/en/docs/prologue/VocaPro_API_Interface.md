---
title: "vocapro api"
description: "vocapro."
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

# VocaPro API Interface

## Request

- `Host`:***http://112.220.79.218:56045/***
- `Content-Type`application/json
    
    ### key별 정보
    
    | key | type |  | example |
    | --- | --- | --- | --- |
    | sentences | string | 사용자 입력 텍스트 전문 | I once misquoted the fees for a particular type of membership to the club where I worked. I explained my mistake to my supervisor, who appreciated my coming to him, and my honesty. |
    | model | string | 모델 (’model1’로 고정) | model1 |
    
    ### 요청 예시
    
    - 
        
        ```bash
        curl -i -X POST \
        -H "Content-Type:application/json" \
        -d \
        '{
        "text": "I once misquoted the fees for a particular type of membership to the club where I worked. I explained my mistake to my supervisor, who appreciated my coming to him, and my honesty.",
        "model": "model1"
        }' 
        ```
        
    - 요청예시
        
        ```bash
        curl --location --request POST '112.220.79.218:56045/api/gec' \
        --header 'Content-Type: application/json' \
        --data-raw '{
            "data": [
                "hello my friend",
                "model1"
            ]
        }'
        ```
        

## Response

- key별 정보

| key |  |  | type | info |
| --- | --- | --- | --- | --- |
| details |  |  |  | 문장별 상세 정보 |
|  | sent_idx |  | int | 문장 인덱스 |
|  | sentence |  | string | 사용자 입력 |
|  | words_info |  | int | 단어별 분석 |
|  |  | word_idx | int | 문장 내 단어 인덱스 |
|  |  | word | string | 단어 |
|  |  | lemma | string | 어간 |
|  |  | pos | string | 형태소 |
|  |  | cefr | string | 단어 수준 |
|  |  | stopword | bool | stopword 여부 |
| summary |  |  |  | 전체 평가및 통계 |
|  | word_list |  | array | 수준별 단어 리스트 |
|  |  | A1 | array | A1 단어 리스트 |
|  |  | A2 | array | A2 단어 리스트 |
|  |  | A3 | array | A3 단어 리스트 |
|  |  | B1 | array | B1 단어 리스트 |
|  |  | B2 | array | B2 단어 리스트 |
|  |  | C1 | array | C1 단어 리스트 |
|  |  | C2 | array | C2 단어 리스트 |
|  | total_level |  | string | 종합 단어 수준 |
|  | total_words |  | int | 전체 단어 개수 |
|  | count |  |  | 수준별 단어 개수 |
|  |  | A1 | int | A1 수준 단어 개수 |
|  |  | A2 | int | A2 수준 단어 개수 |
|  |  | B1 | int | B1 수준 단어 개수 |
|  |  | B2 | int | B2 수준 단어 개수 |
|  |  | C1 | int | C1 수준 단어 개수 |
|  |  | C2 | int | C2 수준 단어 개수 |

### 응답 예시

```json
//QUOTE 는 double로 통일
{
	"success":true,
  "data":{
  "details": [
    {
      "sent_idx": 0,
      "sentence": "I once misquoted the fees for a particular type of membership to the club where I worked",
      "words_info": [
        {
          "word_idx": 0,
          "word": "I",
          "lemma": "I",
          "pos": "pron.",
          "cefr": "A1",
          "stopword": False
        },
        {
          "word_idx": 1,
          "word": "once",
          "lemma": "once",
          "pos": "adv.",
          "cefr": "A2",
          "stopword": True
        },
        {
          "word_idx": 2,
          "word": "misquoted",
          "lemma": "misquote",
          "pos": "unk",
          "cefr": "unk",
          "stopword": False
        },
        {
          "word_idx": 3,
          "word": "the",
          "lemma": "the",
          "pos": "det.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 4,
          "word": "fees",
          "lemma": "fee",
          "pos": "n.",
          "cefr": "B1",
          "stopword": False
        },
        {
          "word_idx": 5,
          "word": "for",
          "lemma": "for",
          "pos": "prep.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 6,
          "word": "a",
          "lemma": "a",
          "pos": "det.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 7,
          "word": "particular",
          "lemma": "particular",
          "pos": "adj.",
          "cefr": "B2",
          "stopword": False
        },
        {
          "word_idx": 8,
          "word": "type",
          "lemma": "type",
          "pos": "n.",
          "cefr": "A2",
          "stopword": False
        },
        {
          "word_idx": 9,
          "word": "of",
          "lemma": "of",
          "pos": "prep.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 10,
          "word": "membership",
          "lemma": "membership",
          "pos": "n.",
          "cefr": "B1",
          "stopword": False
        },
        {
          "word_idx": 11,
          "word": "to",
          "lemma": "to",
          "pos": "infinitive marker",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 12,
          "word": "the",
          "lemma": "the",
          "pos": "det.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 13,
          "word": "club",
          "lemma": "club",
          "pos": "n.",
          "cefr": "A2",
          "stopword": False
        },
        {
          "word_idx": 14,
          "word": "where",
          "lemma": "where",
          "pos": "adv.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 15,
          "word": "I",
          "lemma": "I",
          "pos": "pron.",
          "cefr": "A1",
          "stopword": False
        },
        {
          "word_idx": 16,
          "word": "worked",
          "lemma": "work",
          "pos": "v.",
          "cefr": "A1",
          "stopword": False
        }
      ]
    },
    {
      "sent_idx": 1,
      "sentence": "I explained my mistake to my supervisor, who appreciated my coming to him, and my honesty",
      "words_info": [
        {
          "word_idx": 0,
          "word": "I",
          "lemma": "I",
          "pos": "pron.",
          "cefr": "A1",
          "stopword": False
        },
        {
          "word_idx": 1,
          "word": "explained",
          "lemma": "explain",
          "pos": "v.",
          "cefr": "A2",
          "stopword": False
        },
        {
          "word_idx": 2,
          "word": "my",
          "lemma": "my",
          "pos": "det.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 3,
          "word": "mistake",
          "lemma": "mistake",
          "pos": "n.",
          "cefr": "A2",
          "stopword": False
        },
        {
          "word_idx": 4,
          "word": "to",
          "lemma": "to",
          "pos": "infinitive marker",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 5,
          "word": "my",
          "lemma": "my",
          "pos": "det.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 6,
          "word": "supervisor",
          "lemma": "supervisor",
          "pos": "n.",
          "cefr": "C1",
          "stopword": False
        },
        {
          "word_idx": 7,
          "word": "who",
          "lemma": "who",
          "pos": "pron.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 8,
          "word": "appreciated",
          "lemma": "appreciate",
          "pos": "v.",
          "cefr": "B2",
          "stopword": False
        },
        {
          "word_idx": 9,
          "word": "my",
          "lemma": "my",
          "pos": "det.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 10,
          "word": "coming",
          "lemma": "come",
          "pos": "v.",
          "cefr": "A1",
          "stopword": False
        },
        {
          "word_idx": 11,
          "word": "to",
          "lemma": "to",
          "pos": "infinitive marker",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 12,
          "word": "him",
          "lemma": "him",
          "pos": "pron.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 13,
          "word": "and",
          "lemma": "and",
          "pos": "conj.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 14,
          "word": "my",
          "lemma": "my",
          "pos": "det.",
          "cefr": "A1",
          "stopword": True
        },
        {
          "word_idx": 15,
          "word": "honesty",
          "lemma": "honesty",
          "pos": "n.",
          "cefr": "B2",
          "stopword": False
        }
      ]
    }
  ],
  "summary": {
    "word_list": {
      "A1": [
        "worked",
        "I",
        "the",
        "who",
        "coming",
        "for",
        "and",
        "my",
        "him",
        "of",
        "to",
        "a",
        "where"
      ],
      "A2": [
        "once",
        "club",
        "explained",
        "mistake",
        "type"
      ],
      "B1": [
        "fees",
        "membership"
      ],
      "B2": [
        "particular",
        "appreciated",
        "honesty"
      ],
      "C1": [
        "supervisor"
      ],
      "C2": [
        
      ],
      "unk": [
        "misquoted"
      ],
      "stopwords": [
        "the",
        "who",
        "and",
        "for",
        "my",
        "him",
        "of",
        "once",
        "to",
        "a",
        "where"
      ]
    },
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
    }
  }
}
}
```

![Untitled](VocaPro%20API%20Interface%2090be0ac963a64f25bf6a2b53fee30f47/Untitled.png)
