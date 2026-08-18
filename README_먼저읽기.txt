WRC 2026 현장 가이드 · Release 1.0.1

#이번 변경
- Android Chromium용 자체 앱 설치 버튼 추가 (첫 실행 화면 + 결과 화면)
- `beforeinstallprompt`를 문서 초기에 받아 설치 이벤트 누락 가능성을 줄임
- Service Worker를 앱 초기화보다 먼저 등록하고 시작 시 업데이트 확인
- manifest에 `id`, `prefer_related_applications:false`를 명시하고 GitHub Pages 하위 경로에 맞게 `start_url`/`scope`를 상대 경로로 유지
- 캐시 버전 `v1-0-1`; 온라인일 때 새 HTML을 우선 확인하고 오프라인에서는 캐시로 실행
- 기존 Release 1.0과 같은 IndexedDB 이름을 사용하므로 같은 GitHub Pages 주소에서 업데이트하면 기존 메모/방문기록/사진을 유지하도록 설계

#GitHub Pages 업데이트
현재 저장소가 `nedslee/WRC2026-App`이라면 GitHub 웹에서:
1. 저장소 → Add file → Upload files
2. 이 ZIP을 PC에서 푼 뒤, 폴더 안의 `index.html`, `manifest.webmanifest`, `sw.js`, `icons`, `sample-data` 등을 저장소 최상위에 드래그
3. 같은 이름 파일은 새 파일로 교체되도록 업로드
4. 아래 Commit changes 클릭
5. `Settings → Pages` 설정은 이미 Pages가 동작한다면 변경할 필요 없음
6. 몇 분 뒤 `https://nedslee.github.io/WRC2026-App/` 새로고침

업데이트 후 Android Chrome에서 웹페이지를 열면 첫 사용자 화면과 `결과` 메뉴에 앱 설치 버튼이 표시됩니다. 브라우저 정책 때문에 자체 설치창을 제공하지 않는 순간에는 버튼이 바로 수동 설치 안내를 표시합니다.

#출국 전 최종 점검
1. 홈 화면 앱으로 실행
2. 사용자 이름 설정
3. 고해상도 지도 원본 등록
4. 결과 → 오프라인 준비 상태 → 다시 점검
5. 비행기 모드 → 앱 완전 종료 → 홈 화면 아이콘으로 재실행
6. 업체 검색, 상세, 지도 확인
7. 전체 백업 JSON 1회 생성
