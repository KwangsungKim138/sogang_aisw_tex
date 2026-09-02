# 서강대학교 AI·SW대학원 학위논문 LaTeX 템플릿

서강대학교 AI·SW대학원 석사학위논문 작성을 위한 LaTeX 템플릿입니다.
`template.tex`는 **작성 가이드이자 템플릿**이므로, 먼저 읽어 보신 뒤
논문 작성용으로 편집하여 사용하시기 바랍니다.

## 파일 구성

| 파일 | 설명 |
|------|------|
| `aisw.cls` | 학위논문 문서 클래스 (표지·인준서·여백 등) |
| `aisw.bst` | 참고문헌 서식 (학위논문작성지침 반영) |
| `template.tex` | 작성 가이드 + 형식 데모 (메인 문서) |
| `template.pdf` | 위 문서의 컴파일 결과 |
| `mybib.bib` | BibTeX 샘플 (`book`, `article`, `inproceedings`, `unpublished`, `misc` 등) |
| `figures/1h_CER.pdf` | 그림 삽입 예시용 벡터 PDF |
| `.gitignore` | LaTeX 중간 파일 제외 설정 |

## 시작 방법

1. `template.tex`를 복사하여 `mythesis.tex` 등으로 이름을 바꿉니다.
2. 제목·저자·지도교수·심사위원·날짜 등 정보를 수정합니다.
3. 본문·표·그림·참고문헌을 논문 작성자의 연구 내용으로 교체합니다.
4. 아래 순서로 빌드하여 PDF를 확인합니다.

## 빌드 명령어

```bash
pdflatex template
bibtex template
pdflatex template
pdflatex template
```

각 행의 역할

`pdflatex template`
- 1단계: 인용 정보를 모아 `.aux`를 만듭니다.

`bibtex template`
- 2단계: `mybib.bib`에서 참고문헌을 가져와 `aisw.bst` 서식을 적용합니다. (확장자 `.tex`는 적지 않습니다.)

`pdflatex template`
`pdflatex template`
- 3–4단계: 참고문헌·인용 번호·목차를 반영합니다.

## 환경

- **Windows**: [TeX Live](https://tug.org/texlive/) 권장 (또는 MiKTeX)
- **macOS**: [MacTeX](https://tug.org/mactex/)
- **Linux**: `texlive-full` 등 (`kotex` 포함)
- **Overleaf**: `aisw.cls`, `aisw.bst`, `mybib.bib`, `figures/`를 업로드하고 컴파일러는 pdfLaTeX로 설정합니다.

## 학위논문작성지침

서식은 AI·SW대학원 공지사항(2025년 5월 19일)의 [학위논문작성지침](https://gsinfo.sogang.ac.kr/front/cmsboardview.do?pkid=922318&bbsConfigFK=386&siteId=gsinfo)을 기준으로 합니다.

## 그림 (figure)

PNG/JPEG 등은 확대 시 깨질 수 있으므로 PDF 등 벡터 이미지 입력을 권장합니다.
`template.tex` 제5장을 참고하시기 바랍니다.
