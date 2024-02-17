딥러닝응용 팀프로젝트  “나만의 다큐 (Document)”

프로젝트 주제 : 개인데이터(논문,개인 공부 pdf자료 등 포함)을 활용한 RAG 시스템

개발 환경 : Google Colab

구현 방법 : 
- PDF의 이미지, 테이블의 정보를 분석할 수 있는 RAG 시스템을 구축한다. 
- cohere api, openai api를 활용 한다.
- Cohere의 rerank를 통해서 질문과 유사한 문서의 목록 생성 및 요소의 순위를 매겨 결과를 재구성하여 모델을 개선한다. 
- 중복되는 문서의 내용을 필터링하기 위해 EmbeddingsRedundantFilter 와 연산을 더욱 빠르게 할 수 있도록 EmbeddingsFilte를 사용하여 파이프라인을 구축해 사용한다.
- multiqueryRetreiver을 이용하여 사용자의 질문과 유사한 질문 3가지를 추출하여 선택해서 질문하도록 구축 한다.
- 외부 데이터를 접근 하기 위하여, Search tool(Duckduckgo api)를 추가하여 agent가 접근할 수 있도록 시스템 구축 한다.
- 이미지를 전송 시, gpt4-vision을 통하여 이미지의 분석 결과를 출력한다. 
- 한국어에 질문할 시 파파고 api로 번역하여 쿼리로 사용하고, 마지막으로 나온 영어 결과에 대해서 파파고api로 한국어로 번역 한다. 
- summery checker를 이용하여 memory에 있는 내용을 요약하여 정리하여 출력한다.
- streamlit을 사용하여 UI를 구성한다.  
