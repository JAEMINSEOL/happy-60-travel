# 실사풍 이미지 적용 결과

- 제작 도구: 내장 `image_gen`
- 사진형 AI 참고 이미지 14장 + 메인 동선 지도 1장
- 최초 이미지 적용 당시 HTML 구조·문구·스타일 변경 없음. 이후 사용자 일정 수정은 아래 이력 참고.
- index.html SHA256: `F8DF30904B5E2BC71A3095AC46FA832F58DD027C1231631CA4E0D681BA361499`

| 파일 | 크기 | 용량 (KB, 1000B) | JPG 품질 |
|---|---:|---:|---:|
| images/american-village.jpg | 1200 × 800 | 225.7 | 80 |
| images/anggang-market.jpg | 1200 × 800 | 223.2 | 80 |
| images/cable-car.jpg | 1200 × 800 | 172.6 | 80 |
| images/cover.jpg | 1024 × 1024 | 90.5 | 80 |
| images/day-d0.jpg | 1024 × 1024 | 223.0 | 80 |
| images/day-d1.jpg | 1024 × 1024 | 298.5 | 80 |
| images/day-d2.jpg | 1024 × 1024 | 218.8 | 80 |
| images/day-d3.jpg | 1024 × 1024 | 189.5 | 80 |
| images/day-d4.jpg | 1024 × 1024 | 157.0 | 80 |
| images/german-village.jpg | 1200 × 800 | 244.4 | 80 |
| images/jinnamgwan.jpg | 1200 × 800 | 261.4 | 80 |
| images/main-map.jpg | 1536 × 1024 | 419.8 | 85 |
| images/pocha.jpg | 1200 × 800 | 186.4 | 80 |
| images/sangju-beach.jpg | 1200 × 800 | 229.7 | 80 |
| images/yeosu-park.jpg | 1200 × 800 | 214.7 | 80 |

총 15개 / 3355.2 KB

메인 지도 한글 라벨 확인: 통영, 남해, 여수, 독일마을, 상주은모래비치, 미국마을, 쏠비치, 해상케이블카, 소노캄, 1일차, 2일차, 3일차.

원본 파일과 기존 수채화 백업 폴더는 보존했다. 생성·수정 프롬프트는 image-generation-prompts.json에 기록했다.

## 브라우저 확인

- Edge, 모바일 390 × 844 / 데스크톱 1280 × 900에서 확인.
- 전체 탭 + D0–D4 전환, 이미지 15개 경로, 가로 넘침 없음 확인.
- 메인 지도 클릭 시 원본 확대, Leaflet 지도 표시, 플랜 A/B, 앵강마켓/브레드밀 지도 버튼 2개 확인.
- 테스트 시각 2026-11-02 14:50에 상주은모래비치 ‘지금’ 표시 확인.
- JavaScript 오류 없음. index.html SHA256 재확인 완료.

## 2026-10-25 위치·일정 수정

- 통영 출발은 11/2 09:00. 전날 안내와 1일차 후속 시간도 함께 수정.
- 남해 숙소 체크아웃은 11/3 11:00, 여수 숙소 체크아웃은 11/4 11:00.
- 수요일: 11:00 체크아웃 → 11:30 진남관·이순신광장 → 12:30 점심 → 13:45 오동도 산책 → 15:00 통영 출발 → 약 17:00 도착.
- 쏠비치 남해의 잘못된 서쪽 좌표를 남동 해안 [34.7035, 128.0253]으로 수정. 공식 주소는 미조면 쏠비치길 21.
- 공식 위치 안내: https://www.sonohotelsresorts.com/solbeach_nh/location?isFooterFrom=Y
- 실제 지도 핀과 메인 지도 모두 수정. 내장 image_gen으로 기존 지도 위치·경로를 편집하고 Pillow로 JPEG 변환.
- 지도 한글 라벨 12개와 2일차 북서 방향 화살표 확인. 지도는 이동 순서 개략도이며 실제 길 안내는 지도 앱 사용.
- 수정 프롬프트는 image-generation-prompts.json의 locationCorrection20261025에 기록.
- 수정한 images/main-map.jpg: 1536 × 1024, 435,569 bytes, JPEG 품질 85.
