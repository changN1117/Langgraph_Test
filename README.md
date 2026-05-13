# Langgraph_Test
랭그래프 간단한 실습 코드입니다.

## 1. 설치 및 실행방법
- 패키지 설치
```bash
pip install langchain
pip install langgraph
pip install langchain-community
pip install ollama
```
- ollma 모델 실행
```bash
ollama run exaone3.5:2.4b
```

## 2. 멀티 에이전트 소개
Extractor Agent, Matcher Agent, Answer Agent를 사용했습니다
- Extractor Agent : 질문에서 증상 또는 상태를 단어 또는 구로 추출하는 증상추출 에이전트입니다.
- Matcher Agent : 증상을 바탕으로 해결에 도움이 되는 운동을 3개 추천하는 운동추천 후보 에이전트입니다.
- Answer Agent : 사용자의 증상을 바탕으로 사용자에게 알기 쉽게 개조식으로 설명하는 최종답변 에이전트입니다.

## 3. 사용기술스택
 사용기술스택 : Python, LangChain, LangGraph, Ollama, EXAONE 3.5 2.4B

## 4. 그래프 구조(전체 실행 흐름 이해)
 사용자 질문 입력 -> 증상 추출 에이전트 -> 운동 추천 에이전트 -> 최종 답변 생성 에이전트 -> 결과 출력

 <img width="108" height="432" alt="그래프 구조" src="https://github.com/user-attachments/assets/195802a6-c60b-4974-aa37-8d2e4d20bbb3" />

## 5. 결과 캡처 이미지
랭그래프 실습 코드를 기반으로 나온 결과 출력 이미지 입니다.
<img width="1132" height="613" alt="결과출력 1" src="https://github.com/user-attachments/assets/fcbb6069-5327-4a40-abbe-a94dd41e848a" />
<img width="1490" height="163" alt="결과출력 2" src="https://github.com/user-attachments/assets/49aed927-9dc5-48b2-b2c3-61ad99d56724" />

## 6. 핵심 학습 내용
- LangGraph의 상태(State) 기반 흐름 이해하고 학습
- 멀티에이전트 구조 구현
- PromptTemplate 활용
- Ollama 기반 로컬 LLM 연결
- Node 및 Edge 기반 그래프 구성
