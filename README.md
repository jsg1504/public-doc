# JSG Docs — 문서 공유 저장소

> 여행, 생활, 기술 등 다양한 주제의 문서를 공유하는 GitHub Pages 사이트입니다.

🌐 **사이트 주소**: https://jsg1504.github.io/public-doc/

---

## 폴더 구조

```
public-doc/
├── index.html          ← 대문 페이지 (자동 카드 생성)
├── docs.json           ← 문서 목록 (이 파일을 수정해서 카드 추가)
├── travel/
│   ├── index.html      ← 여행 카테고리 목록 페이지
│   └── 260501/
│       └── index.html  ← 개별 문서
└── ...
```

---

## 새 문서 추가하기

### 1단계 — 폴더와 index.html 생성

```
주제명/index.html
```

예시: 호주 여행 문서를 추가하려면

```
travel/australia/index.html
```

접근 URL: `https://jsg1504.github.io/public-doc/travel/australia`

### 2단계 — docs.json 업데이트

`docs.json`에 아래 형식으로 항목을 추가합니다.

```json
{
  "title": "문서 제목",
  "description": "문서에 대한 간단한 설명",
  "path": "/카테고리/문서폴더",
  "category": "travel",
  "icon": "✈️",
  "date": "2026-05-12"
}
```

#### 지원 카테고리

| 카테고리 키 | 표시 이름 | 아이콘 |
|------------|----------|--------|
| `travel`   | 여행      | ✈️     |
| `life`     | 생활      | 🏠     |
| `tech`     | 기술      | 💻     |
| `food`     | 음식      | 🍽️     |
| `etc`      | 기타      | 📌     |

> 새 카테고리를 추가하려면 `docs.json`에 새 `category` 값을 사용하면 됩니다.  
> 대문 페이지의 필터 버튼이 자동으로 생성됩니다.

### 3단계 — 커밋 & 푸시

```bash
git add .
git commit -m "docs: 새 문서 추가"
git push
```

---

## GitHub Pages 설정

저장소 Settings → Pages → Source를 **`main` 브랜치 / `/ (root)`** 로 설정하세요.
