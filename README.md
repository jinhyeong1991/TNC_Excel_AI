# TNC Excel AI (Gemini 도우미 + 신전산 CMS 만들기)

엑셀 추가 기능(`GeminiAI.xlam`)입니다. 어떤 엑셀 파일에서든 쓸 수 있습니다.

## 설치 (PC마다 한 번)
1. 이 폴더의 파일을 모두 `%AppData%\Microsoft\AddIns` 폴더에 복사합니다.
2. `GeminiAI.xlam` 파일 우클릭 → 속성 → 맨 아래 "차단 해제" 체크 → 확인.
3. 엑셀 → 파일 → 옵션 → 추가 기능 → 관리: "Excel 추가 기능" → 이동 → 찾아보기 → `GeminiAI.xlam` 선택 → 확인.
4. **Gemini API 키 넣기** (키는 이 저장소에 들어 있지 않습니다): https://aistudio.google.com 에서 키 발급 → 엑셀 Alt+F11 → `Gemini` 모듈 맨 위 `PASTE_YOUR_KEY_HERE` 를 본인 키로 교체 → 저장.
5. 신전산 양식 파일 `신전산_CMS양식.xlsx` 를 같은 AddIns 폴더에 넣습니다 (이 저장소에는 포함하지 않았습니다).

## 사용
- `Ctrl+Shift+G` : Gemini 창 (시트 내용을 읽고 필터/정렬/서식/그래프 등을 제안·적용)
- `Ctrl+Shift+M` : 신전산 CMS 만들기 (정책표 → 신전산 양식 엑셀 자동 생성)
- 셀 우클릭 → `Gemini AI` / `CMS 만들기`
- 수식 `=AskGemini("질문")`

## 파일
- `GeminiAI.xlam` : 추가 기능 본체 (API 키 제거본)
- `GeminiGuide.txt` : AI에게 알려 주는 업무 용어/규칙 (자유롭게 수정)
- `제품구분코드.txt` : 제품구분 코드표 (사용불가 제외)
- `제품구분_별칭.txt` : 이름 → 제품구분 코드 학습 결과

## 주의
- 시트 내용이 Google Gemini로 전송됩니다. 개인정보가 있는 파일에는 쓰지 마세요.
- 저장 위치 기본값은 `D:\<월>월\cms\<날짜>` 입니다. D 드라이브가 없으면 CMS 화면의 "저장 폴더"에 경로를 직접 입력하세요.