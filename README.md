# 놀이공원 데이트 신청

09월 19일(토) 놀이공원 데이트 신청 페이지입니다. 순수 HTML/CSS/JS로만 되어 있어 별도 빌드 없이 바로 배포할 수 있습니다.

## GitHub Pages로 배포하기

1. 이 `daterequest` 폴더 내용을 GitHub 저장소에 푸시합니다. (레포 이름 예: `daterequest`)
2. GitHub 저장소 → **Settings** → **Pages**로 이동합니다.
3. **Source**를 `Deploy from a branch`로 설정하고, 브랜치는 `main`(또는 사용 중인 브랜치), 폴더는 `/ (root)`를 선택 후 저장합니다.
   - 만약 저장소 루트가 아니라 `daterequest` 폴더만 올렸다면 그 폴더가 곧 루트가 되므로 그대로 `/ (root)`를 선택하면 됩니다.
4. 잠시 후 `https://<사용자명>.github.io/<저장소명>/` 주소에서 접속할 수 있습니다.

## 로컬에서 미리보기

`index.html` 파일을 브라우저로 그냥 열면 됩니다. 별도 서버가 필요 없습니다.

## 동작

- **좋아요!** 버튼: 두 장소 중 하나를 고르는 선택지("사람이 많지만 아름다운 불꽃축제와 함께하는 이월드!" / "놀이기구를 더 많이 탈 수 있는 경주월드!")가 나타납니다.
  - 둘 중 하나를 선택하면 폭죽(캔버스 파티클) 애니메이션과 함께 "사랑해요!" 문구가 나타나고, 고른 장소에 맞는 문구가 함께 표시됩니다.
- **싫어요!** 버튼: 마우스/터치가 가까이 오면 화면 안에서 계속 도망다녀서 클릭할 수 없습니다.

## 링크 공유 시 미리보기(오픈그래프)

카카오톡·슬랙·디스코드 등에 이 페이지 링크를 붙여넣으면 "데이트 신청서가 도착했습니다." 문구와 함께 [og-image.png](og-image.png) 미리보기 카드가 뜨도록 `index.html`에 Open Graph / Twitter Card 메타태그를 넣어두었습니다.

- GitHub Pages로 배포한 뒤, 아래 도구로 실제 미리보기가 잘 뜨는지 확인해보세요.
  - 카카오 공유 디버거: https://developers.kakao.com/tool/debugger/sharing
  - Facebook 공유 디버거: https://developers.facebook.com/tools/debug/
  - https://www.opengraph.xyz/ (범용 미리보기 확인 도구)
- 일부 서비스(특히 카카오톡)는 `og:image`에 **절대경로(https://...)**를 요구하는 경우가 있습니다. 배포 후 `og-image.png`가 상대경로로 잘 안 뜨면, `index.html`의 `og:image`/`twitter:image` 값을 `https://<사용자명>.github.io/<저장소명>/og-image.png` 형태의 전체 URL로 바꿔주세요.
- 미리보기 캐시 때문에 이미지를 바꿔도 이전 이미지가 계속 보일 수 있습니다. 위 디버거 도구에서 "다시 크롤링"으로 캐시를 갱신하세요.
