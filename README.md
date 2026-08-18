# coupon-yaho/.github

조직 프로필과 발표 자산을 함께 두는 리포입니다.

## 구성

```
profile/README.md     조직 프로필. github.com/coupon-yaho 상단 소개글
index.html            발표 자산 랜딩
plan/index.html       기획안 발표 (4조 KAFKICK)
assets/               Pretendard 서브셋 폰트 3종 · 로고
.github/workflows/    Pages 배포
```

## 배포 주소

```
https://coupon-yaho.github.io/.github/
https://coupon-yaho.github.io/.github/plan/
```

리포 이름이 `.github` 라 하위 경로로 붙습니다. 조직 대표 주소
(`https://coupon-yaho.github.io/`)로 쓰려면 리포 이름이 `coupon-yaho.github.io`
여야 합니다. HTML 참조가 전부 상대경로라 하위 경로에서도 그대로 동작합니다.

## 배포 방법

`main` 에 `index.html` · `plan/**` · `assets/**` 가 바뀌면 자동으로 배포됩니다.
수동 실행은 Actions → Deploy site to Pages → Run workflow.

**최초 1회** Settings → Pages → Source 를 **GitHub Actions** 로 바꿔야 합니다.
Pages 사이트 생성은 `GITHUB_TOKEN` 권한 밖이라 워크플로가 대신 못 켭니다.

## 주의

배포물은 리포 전체가 아니라 워크플로가 `_site` 로 **골라 담은 것**만 올라갑니다.
`profile/` 과 `.github/` 는 배포에서 제외되고, 섞이면 워크플로가 실패합니다.
발표 자산이 아닌 문서(`.md` · `.pptx` · `.docx` · `.dbml`)도 같은 가드에 걸립니다.

> 리포가 public 이라 **여기 올리는 것은 전부 공개**됩니다. 대외비 문서는 두지 마세요.
