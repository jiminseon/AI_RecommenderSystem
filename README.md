#  EmoDiary
<img src="https://github.com/user-attachments/assets/3a4d931f-e36a-4356-aa4f-9a3a12879736"  width="700" height="400"/>
<br>

- 개발 기간 : 2024.09 ~ 2024.12
  
- 배포 URL : https://huggingface.co/spaces/dazzleun-7/Bigdatacapstone_24-2
</p>

# EmoDiary 🎵📔

감정 기반 개인화 맞춤형 플레이리스트 및 일기 회고 추천 서비스

---

## 📌 프로젝트 소개

**EmoDiary**는 사용자의 감정을 분석하여 맞춤형 플레이리스트와 일기 회고 콘텐츠를 추천하는 **스마트 감정 일기 도우미 서비스**입니다.

* 🎶 **플레이리스트 추천** : 실시간 감정 분석 결과를 기반으로 음악 추천
* ✍️ **일기 회고 콘텐츠 추천** : 생성형 AI를 활용해 주제/캐릭터/회고 문장 제시
* 😊 **정서적 웰빙** : 자기 성찰을 촉구하고 스트레스 완화 및 심리적 안정에 기여

---

## 📖 기획 배경

* 음악 감상이 정서 조절에 긍정적 효과를 주지만, 기존 플랫폼은 개인의 **구체적인 감정 상태 반영 부족**
* 일기 작성 시 소재 부족, 감정 파악 어려움, 올바른 작성법 부재 등의 문제 존재
* 이를 해결하기 위해 **감정 분석 + 추천 시스템 + 생성형 AI**를 결합한 서비스를 기획

---

## ⚙️ 기술 스택

* **Language / Data**: Python, Pandas, Numpy
* **ML Framework**: PyTorch, Hugging Face Transformers
* **NLP**: KoBERT (텍스트 감정 분석)
* **CV**: CLIP, OpenCV (얼굴 표정 감정 분석)
* **Recommender System**: Cosine Similarity 기반 User-Song / Song-Song 유사도
* **Generative AI**: Hugging Face Diffusers (일기 주제 및 캐릭터 이미지 생성)
* **Frontend / Deployment**: Gradio, Hugging Face Spaces
* **Collaboration**: GitHub

---

## 🗂 데이터 수집 및 전처리

* **감정 데이터**: 감정대화 말뭉치 데이터셋 → 6개 감정 라벨 (기쁨, 즐거움, 사랑, 분노, 우울, 외로움)
* **음악 데이터**: Melon Top 100 (2010\~2024) 가사 데이터 수집 및 정제

  * 영어/특수문자 제거, 중복 제거, NaN 데이터 제거

---

## 🤖 모델 및 추천 시스템

* **KoBERT**: 사용자 입력 텍스트 감정 분석
* **CLIP + OpenCV**: 사용자 얼굴 이미지 기반 감정 분석
* **최종 사용자 감정 벡터**: 텍스트(0.7) + 이미지(0.3) 가중치 반영
* **추천 알고리즘**:

  * 1차: 사용자 감정 벡터와 노래 가사 감정 벡터 유사도(Cosine Similarity)
  * 2차: Song-Song Similarity + User-Song Similarity 가중치 기반 최종 플레이리스트 도출

---

## ✨ 주요 기능

* [x] 텍스트 입력 기반 감정 분석
* [x] 얼굴 표정 이미지 기반 감정 분석
* [x] 감정 벡터와 음악 가사 벡터 매칭 → 플레이리스트 추천
* [x] 일기 회고 주제 및 캐릭터 이미지 생성
* [x] Gradio UI 제공 및 Hugging Face 배포

---



## 📊 성과 및 기대효과

* 사용자 맞춤형 감정 기반 음악 추천 경험 제공
* 자기 성찰과 정서적 웰빙 촉진
* 생성형 AI 기반 콘텐츠 추천을 통한 재미와 몰입감 향상
* 데이터 기반 감정 분석/추천 모델의 산업적 활용 가능성 제시



