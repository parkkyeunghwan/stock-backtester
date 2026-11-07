[주식 전략 백테스터 - 모바일 앱(PWA) 설치 방법]

■ 폴더 구성 (전부 같은 폴더에 두세요)
  index.html / sw.js / manifest.webmanifest / icon-*.png

■ 1단계: 웹에 올리기 (GitHub Pages, 무료)
  1) github.com 가입 후 New repository 생성 (이름 예: stock-backtester, Public)
  2) "uploading an existing file" 로 이 폴더의 파일 전부 업로드 후 Commit
  3) Settings > Pages > Branch: main / (root) 선택 후 Save
  4) 1~2분 뒤 https://내아이디.github.io/stock-backtester/ 주소가 생깁니다
  ※ 주식 CSV 데이터는 서버로 올라가지 않고 폰 안에서만 처리됩니다.
  ※ Netlify Drop(app.netlify.com/drop)에 폴더를 끌어다 놓아도 됩니다.

■ 2단계: 폰에 설치
  - 아이폰(Safari): 주소 접속 > 공유 버튼 > "홈 화면에 추가"
  - 안드로이드(Chrome): 주소 접속 > 메뉴(⋮) > "홈 화면에 추가" 또는 "앱 설치"

■ 오프라인 사용
  최초 1회는 인터넷으로 접속해야 합니다(차트 라이브러리와 글꼴을 폰에 저장).
  그 이후에는 비행기 모드에서도 실행됩니다.
  (선택) chart.umd.min.js 파일을 같은 폴더에 넣어 두면 더 안정적입니다.

■ 저장 전략 옮기기 (PC -> 폰)
  브라우저 저장소는 기기·브라우저·설치 앱마다 따로입니다.
  PC에서 "내보내기(JSON)" > 폰으로 전송 > 폰 앱에서 "가져오기" 하세요.
  아이폰은 Safari에서 쓰던 데이터가 홈 화면 앱과 공유되지 않으므로,
  홈 화면에 설치한 뒤 그 앱 안에서 가져오기를 하세요.

■ 데이터 불러오기
  - 종목 1개: 상단 "CSV 파일"에서 폰 저장소의 파일 선택
  - 여러 종목: "폴더 스캔" 탭 > "CSV 여러 개 선택" 후 스캔
  (종목이 수십 개면 폰에서는 시간이 오래 걸릴 수 있습니다.)

■ 업데이트
  파일을 새 버전으로 교체해 올리면, 앱을 다시 열 때 자동 반영됩니다.
  반영이 안 되면 sw.js 의 const V='bt-v83' 값을 올려 주세요.
