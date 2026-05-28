# 🏫 가정통신문 AI 초안 자동생성 시스템

> **Google Forms + Google Sheets + n8n + Gemini AI + Gmail** 을 연결한 교육 자동화 워크플로  
> 교사가 폼을 제출하면 AI가 즉시 가정통신문 초안을 작성하고 이메일로 발송합니다.

---

## 🔗 구글 폼 바로가기

👉 **[가정통신문 작성 요청 폼 바로가기](https://docs.google.com/forms/d/e/1FAIpQLSdHfyibSE-74Oy-3g9o4I5Jnm4YBrFIU-QkoOMK1iUBlZ9jRg/viewform)**

---

## 📌 전체 흐름도

```
[교사] 구글 폼 작성
    ↓ (제목 · 학년반 · 이메일 입력)
[Google Sheets] 응답 자동 저장
    ↓ (1분마다 감지)
[n8n] 폼 응답 감지 트리거
    ↓
[Gemini 2.5 Flash] AI 초안 생성
    ↓
[n8n Set 노드] 데이터 정리
    ↓
[Google Sheets] 초안검토 시트에 저장
    ↓
[Gmail] 교사에게 검토 이메일 발송
```

---

## 🛠 사전 준비물

| 항목 | 내용 |
|------|------|
| Google 계정 | Gmail, Google Forms, Google Sheets 사용 |
| n8n Cloud 계정 | [https://n8n.io](https://n8n.io) 무료 플랜 가능 |
| Gemini API 키 | [Google AI Studio](https://aistudio.google.com/app/apikey) 에서 무료 발급 |
