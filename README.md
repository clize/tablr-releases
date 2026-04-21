# Tablr Releases

[Tablr](https://github.com/clize/tablr) 바이너리 배포 리포지토리. 자동 업데이트 용도입니다. 소스코드는 private 리포에 있습니다.

## 최신 버전 다운로드

[**Releases → Latest**](https://github.com/clize/tablr-releases/releases/latest)

## 설치 가이드

### macOS (Apple Silicon)

> Intel Mac은 현재 지원하지 않습니다. 터미널에서 `uname -m` 입력 시 `arm64`여야 합니다.

1. `Tablr-X.X.X-arm64.dmg` 다운로드 후 더블클릭
2. 열린 창에서 **Tablr 아이콘을 Applications 폴더로 드래그**
3. 터미널을 열고 다음 명령 실행:
   ```bash
   xattr -cr /Applications/Tablr.app
   ```
   > 서명되지 않은 빌드라 macOS가 "손상되었다"는 경고를 띄우는데, 이 명령으로 해제됩니다.
4. Launchpad나 Spotlight(⌘+Space)에서 **Tablr** 검색 후 실행

### Windows (x64)

1. `Tablr-Setup-X.X.X.exe` 다운로드 후 실행
2. SmartScreen 경고가 뜨면 **추가 정보 → 실행** 클릭
3. 설치 마법사 따라 완료

## 자동 업데이트

설치 후 앱이 실행될 때 새 버전을 자동으로 체크합니다:

- **Windows**: 백그라운드에서 자동 다운로드 → "재시작 & 설치" 알림
- **macOS**: 상단에 알림 + "다운로드" 버튼 → 새 DMG 받아서 덮어쓰기 설치 (+ `xattr` 재실행)

## 문제 해결

### macOS "손상되었기 때문에 열 수 없습니다"
3번 단계의 `xattr -cr` 명령이 필요합니다. 이미 Applications에 설치한 상태라면 해당 명령만 실행하면 됩니다.

### Windows SmartScreen 경고
서명이 없어서 표시됩니다. **추가 정보 → 실행**으로 우회하세요.
