# tomsworkers.io

주식회사 톰즈워커즈 회사 소개 한 장입니다. GitHub Pages 로 게시됩니다.

- https://tomsworkers.io

## 왜 저장소가 따로인가

**GitHub Pages 는 저장소 하나에 커스텀 도메인 하나다.** 마이베이스볼스타
사이트(`tomsworkers-io/mabas-site`)의 `CNAME` 은 `mybaseballstar.app` 이라,
거기에 `tomsworkers.io` 를 얹으면 앱 주소가 떨어져 나간다. 그 주소는 App
Store 에 제출돼 있고 앱에 상수로 박혀 있어서 끊기면 안 된다.

## 짜임

Jekyll 을 쓰지 않는다(`.nojekyll`). 페이지가 `index.html` 하나뿐인데 레이아웃과
설정 파일을 두면 고칠 곳만 늘어난다. CSS 도 그 파일 안에 있다.

| 파일 | |
|---|---|
| `index.html` | 페이지 전부 |
| `CNAME` | 커스텀 도메인 |
| `logo.png` | 마이베이스볼스타 아이콘 |
| `.nojekyll` | 빌드 없이 그대로 게시 |

⚠️ **`logo.png` 는 앱의 아이콘이지 회사 마크가 아니다.** 제품 카드 안에서만
쓴다. 맨 위 줄은 [톰즈워커즈] 글자로 두었고, 파비콘과 `og:image` 는 비워 뒀다
— 회사 마크가 없는데 앱 아이콘을 얹으면 회사와 앱이 같은 것이 된다. 마크가
생기면 `index.html` 의 `<head>` 주석에 적어 둔 자리에 함께 넣는다.

원본은 `mabas-site` 의 랜딩 페이지에도 있다(`logo.png`). 갈아 끼울 때 양쪽을
같이 고쳐야 한다.

## 주소

`CNAME` 이 `tomsworkers.io` 를 정한다. DNS 는 GoDaddy 에 있다. 루트 도메인이라
CNAME 레코드를 쓸 수 없고 A 레코드로 GitHub Pages 를 가리킨다.

| 형식 | 이름 | 값 |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `tomsworkers-io.github.io` |

저장소 Settings > Pages 에서 Source 를 `main` 브랜치로 두고, Custom domain 에
`tomsworkers.io` 를 넣은 뒤 Enforce HTTPS 를 켠다. 인증서가 발급될 때까지
길면 한 시간쯤 걸린다.

⚠️ `mybaseballstar` CNAME 은 건드리지 않는다. 같은 GoDaddy 계정에 있지만 다른
사이트를 가리킨다.

## 내용

적힌 것은 확인된 사실뿐이다. 사업자등록번호·주소·대표자·설립일은 근거가 없어
비워 뒀다. 채울 자리는 `index.html` 의 `<dl class="info">` 위 주석에 적어 뒀다.

**마이베이스볼스타의 이용약관·개인정보 처리방침과 [시행자] 이름이 어긋나면
안 된다.** 그 문서들의 원본은 `tomsworkers-io/mabas-site` 에 있다.
