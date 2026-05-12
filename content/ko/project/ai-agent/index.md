---
title: LLM 기반 AI Agent
summary: LangChain과 OpenAI API를 활용한 자율 작업 수행 AI Agent 구현
tags:
  - agent
  - ai
date: 2025-03-01
external_link: https://github.com/BaePro-source
image:
  caption: 'AI Agent Architecture'
  focal_point: Smart
  preview_only: false
---

## LLM 기반 AI Agent 프로젝트

LangChain 프레임워크와 OpenAI GPT API를 활용하여 자율적으로 도구를 선택하고 작업을 수행하는 AI Agent를 구현한 프로젝트입니다.

### 주요 기능
- **Tool Calling**: 웹 검색, 파일 읽기/쓰기, 코드 실행 등 외부 도구 연동
- **ReAct 패턴**: 추론(Reasoning)과 행동(Acting)을 반복하는 에이전트 루프 구현
- **메모리 관리**: 대화 히스토리와 장기 기억 저장소를 활용한 컨텍스트 유지
- **멀티 에이전트**: 역할이 다른 여러 에이전트가 협력하는 파이프라인 설계

### 기술 스택
- Python, LangChain, OpenAI API
- ChromaDB (벡터 스토어)
- FastAPI (Agent 서빙)
