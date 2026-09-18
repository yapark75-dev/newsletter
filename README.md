# 🧠 나만의 AI 학습 허브 — 템플릿

AI를 따라잡는 두 가지 길을 한 곳에. **코딩을 몰라도** Claude Cowork에게 시키면 됩니다.
이 저장소는 **Use this template 버튼으로 복사해 바로 시작하는 깨끗한 템플릿**입니다. (가득 찬 예시는 👉 [ai-newsletter 샘플](https://github.com/imakerjun/ai-newsletter) / [라이브](https://imakerjun.github.io/ai-newsletter/))

- 📰 **받아보기 (자동)** — 내 관심사 맞춤 AI 뉴스레터가 매일 아침 자동 발행됩니다.
  - 아카이브: `index.html` · 한 호: `editions/{날짜}.html`
- 📚 **깊이 읽기 (수동)** — 공부하고 싶은 어려운 문서를 **5가지 렌즈**(🔤어원·⚡한입요약·🧒비유·🧪퀴즈·📄전문번역)로 재구성.
  - 라이브러리: `learn/index.html` · 한 문서: `learn/{슬러그}.html`
- 🤖 **사양**: [`AGENT.md`](./AGENT.md) — 자동 발행 + 수동 렌즈 생성 지시서
- 🎨 Folio(Notion 스타일) 단일 HTML · 라이트/다크 자동 · **GitHub Pages**(또는 Vercel)로 배포·누적

> 지금 들어 있는 항목은 **예시(`예시` 배지)**입니다. 첫 발행 때 에이전트가 자동으로 비우고 내 콘텐츠로 채웁니다.

---

## 따라하기 — Cowork + GitHub Pages로 3단계

> 코딩 지식이 없어도 됩니다. 아래 순서대로 **클로드 코워크(Cowork)에게 말로** 시키면 돼요.
> 낯선 단어는 각 단계의 💡 설명과 맨 아래 ‘용어 한눈에’를 참고하세요.

### 1단계. 먼저 페이지로 만들어 보기 (미리보기)

Cowork에 이 템플릿 링크를 주며 이렇게 요청합니다.
```
https://github.com/imakerjun/ai-newsletter-template 이 템플릿 활용해서,
지난 1주일간 있었던 AI 소식을 페이지로 만들어 주세요.
```
> 💡 **무엇을 위한 작업인가요?** 인터넷에 올리기 전에, 내 관심사로 뉴스레터가 잘 만들어지는지 먼저 눈으로 확인하는 단계예요. 깃허브 링크는 일종의 ‘설계도’이고, Cowork가 그 설계도로 내 페이지를 만들어 줍니다. 아직은 내 작업 공간 안에서만 보이는 ‘미리보기’입니다.

### 2단계. 내 GitHub 저장소로 복사하고 인터넷에 올리기 (배포)

> 💡 **‘배포’가 뭔가요?** 만든 페이지를 나만 보는 게 아니라, **링크 하나로 누구나(휴대폰에서도) 열어볼 수 있게 인터넷에 올리는 것**을 ‘배포’라고 해요. 여기서는 GitHub이 무료로 해주는 **GitHub Pages**를 씁니다.

1. **이 템플릿을 내 저장소로 복사** — 이 페이지 오른쪽 위 **Use this template** → **Create a new repository**. 이름은 `ai-newsletter`, **Public**을 고르고 Create.
   > 💡 저장소는 GitHub에 만드는 내 폴더예요. 무료 계정은 Public 저장소만 Pages가 됩니다.
2. **Pages 켜기** — 내 저장소에서 **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: main / (root) → Save**. 1~2분 뒤 `https://내아이디.github.io/ai-newsletter/` 주소가 생깁니다.
   > 💡 이 주소를 열면 지금은 템플릿 예시가 보여요. 내 내용은 다음 단계에서 채워집니다.
3. **클로드 커넥터에 GitHub 추가** — 클로드 설정의 커넥터(연결)에서 GitHub을 추가하고 이 저장소 접근을 허용합니다.
   > 💡 클로드가 내 저장소에 파일을 올릴 수 있도록 ‘연결’해 주는 단계예요. 인증 화면의 코드는 다른 사람에게 보이지 않게.
4. **내 설정으로 바꾸기** — 이렇게 말합니다.
   ```
   {내아이디}/ai-newsletter 저장소의 AGENT.md에서 owner를 "{내 이름}"으로, pages_url을 https://{내아이디}.github.io/ai-newsletter 로,
   interests를 내 관심사로 바꿔줘. index.html의 "(내 이름)"도 바꿔줘. 커밋해줘.
   ```
5. **발행 요청** — 이렇게 말합니다.
   ```
   AGENT.md 1번 순서대로 오늘 호를 만들어 editions/에 저장하고, index.html 목록 맨 앞에 추가한 뒤 커밋·푸시해줘. 끝나면 pages_url을 알려줘.
   ```
   > 💡 1~2분 뒤 내 주소를 새로고침하면 예시가 사라지고 내 첫 호가 보입니다.

> 다른 방법: Vercel 커넥터가 있으면 클로드가 Vercel로 직접 올릴 수도 있습니다(AGENT.md §1.6 대안).

### 3단계. 매일 아침 자동으로 받기 (스케줄)

> 💡 **무엇을 위한 작업인가요?** 매번 직접 시키지 않아도, **정해진 시간에 알아서** 새 뉴스레터를 만들고 배포하고 나에게 보내게 하는 것입니다. 한 번 걸어두면 매일 자동이에요.

Cowork의 **스케줄 기능**으로 이렇게 등록합니다.
```
매일 아침 8시에, AGENT.md 사양대로 지난 24시간 AI 소식으로 새 뉴스레터를 만들고,
저장소에 커밋·푸시한 다음, pages_url 주소를 Gmail로 나에게 보내줘.
```
> 💡 이제부터는 **아침마다 도착한 링크만 열어보면** 됩니다.

### (선택) 어려운 문서를 ‘깊이 읽기’로
공부하고 싶은데 어려운 공식문서가 있으면 이렇게 시켜보세요.
```
이 링크를 '깊이 읽기' 렌즈 문서로 만들어줘 — {문서 URL}
```

---

### 용어 한눈에 (비개발자용)
| 단어 | 쉬운 설명 |
|---|---|
| **배포** | 내 페이지를 인터넷에 올려, 링크로 아무나 볼 수 있게 만드는 것 |
| **GitHub Pages** | 저장소 안 파일을 인터넷 주소로 보여주는 GitHub 기능. 무료, Public 저장소만 |
| **커넥터** | 클로드를 외부 서비스(GitHub·Gmail·슬랙 등)에 연결해 주는 설정 |
| **토큰** | 내 계정 대신 작업하게 해주는 비밀 출입증 — **노출 금지** |
| **스케줄** | 정해진 시간에 작업을 자동으로 반복시키는 기능 |
| **커밋·푸시** | 변경한 내용을 깃허브에 저장·반영하는 것. 클로드가 대신 해줍니다 |

---

## 구조
```
.
├── index.html               # 📰 뉴스레터 아카이브 (ARCHIVE.editions)
├── editions/2026-06-18.html  # 예시 한 호 (NEWSLETTER 데이터 객체)
├── _TEMPLATE_edition.html    # 뉴스레터 한 호의 고정 구조 템플릿 (웹페이지용)
├── _TEMPLATE_email.html      # 같은 호를 이메일로 보낼 때 쓰는 템플릿 (인라인 style·table 레이아웃)
├── learn/
│   ├── index.html            # 📚 렌즈 라이브러리 (LIBRARY.docs)
│   ├── prompting-fable-5.html#   예시 렌즈 문서 (LENS_DOC 데이터 객체)
│   └── _TEMPLATE_lens.html   #   렌즈 문서의 고정 구조 템플릿
├── AGENT.md                  # 자동 발행 + 수동 렌즈 생성 사양
└── README.md
```

디자인: [Folio](https://claude.ai/design) · 깊이 읽기는 [doc-lenses](https://github.com/imakerjun/learning-templates/tree/main/doc-lenses) 각색.
