---
title: AdGuard 로그 수집하는 방법
sidebar_position: 3
---

다양한 문제의 분석 및 진단을 위해 지원 서비스는 AdGuard 로그 파일이 필요할 수 있습니다. 이 파일에는 소프트웨어에서 발생한 모든 오류에 대한 기록이 있습니다. AdGuard 로그를 수집하여 지원 팀에 보내는 방법을 살펴보겠습니다.

1. AdGuard 설정을 엽니다. *일반 설정* 섹션으로 이동하여 아래로 스크롤한 후 *로깅 레벨*을 *디버그*로 전환합니다.

![디버그 로깅 레벨 *border](https://cdn.adtidy.org/content/kb/ad_blocker/windows/solving-problems/adg-logs-1.png)

2. 문제를 재현합니다.

- 지원 팀이 빨리 문제를 해결할 수 있도록 문제 재현 시간을 지정해 주십시오.

3. *로그 내보내기* 버튼을 클릭하여 기록된 로그를 내보냅니다.

![로그 내보내기 *border](https://cdn.adtidy.org/content/kb/ad_blocker/windows/solving-problems/adg-logs-2.png)

- 어느 폴더에서나 압축된 로그파일을 저장합니다.

4. **주의**: 로그를 내보낸 후 로깅 레벨을 *기본*으로 다시 설정합니다. *디버그* 로깅 레벨이 켜져 있으면 프로그램이 느려집니다.

5. 문제를 재현한 시간을 알려 주고 자세히 설명하여 AdGuard 지원 팀에 **support@adguard.com**으로 압축된 로그파일을 보내 주세요.

### 추적 로그 {#trace-logs}

가끔 지원 팀은 **추적 로그**를 보내달라고 요청할 수 있습니다. 추적 로그를 수집하는 방법은 다음과 같습니다.

1. Stop AdGuard by right-clicking the AdGuard icon in the tray menu and choosing *Exit AdGuard*:

![AdGuard 종료 *mobile](https://cdn.adtidy.org/content/kb/ad_blocker/windows/solving-problems/adg-logs-3.png)

서비스를 실행 상태로 두지 마십시오.

![AdGuard 서비스 중지 *mobile_border](https://cdn.adtidy.org/public/Adguard/kb/newscreenshots/En/eng_logs_4.png)

2. 콘솔을 엽니다(시작 패널에 `cmd` 입력).

3. 64비트 Windows를 사용하는 경우, `C:\"Program Files (x86)"\Adguard\Adguard.exe /trace` 명령으로 앱을 실행합니다. 32비트 Windows를 사용하는 경우, `C:\"Program Files"\Adguard\Adguard.exe /trace` 명령으로 앱을 실행합니다.

4. *디버그* 로깅 레벨을 선택합니다.

![디버그 *border](https://cdn.adtidy.org/content/kb/ad_blocker/windows/solving-problems/adg-logs-1.png)

5. 문제를 재현합니다.

- 지원 팀이 빨리 문제를 해결할 수 있도록 문제 재현 시간을 지정해 주십시오.

6. *로그 내보내기* 버튼을 클릭하여 기록된 로그를 내보냅니다.

![로그 내보내기 *border](https://cdn.adtidy.org/content/kb/ad_blocker/windows/solving-problems/adg-logs-2.png)

7. **주의**: 로그를 내보낸 후 로깅 레벨을 *기본*으로 다시 설정합니다. *디버그* 로깅 레벨이 켜져 있으면 프로그램이 느려집니다.

로그파일은 커도 문제가 없습니다. 문제를 해결하기 위해 정보가 많을수록 좋습니다.
