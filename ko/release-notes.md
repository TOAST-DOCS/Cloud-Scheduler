<!-- pre-align:aligned sig=9a6130697b7f -->

<a id="release-notes"></a>
## Cloud Scheduler 릴리스 노트 { #release-notes }

**Application Service > Cloud Scheduler > 릴리스 노트**

<a id="april-28-2026"></a>
## 2026. 04. 28. { #april-28-2026 }
<a id="feature-updates"></a>
### 기능 개선/변경 { #feature-updates }
* 대상 템플릿을 사용하여 일정/일정 템플릿 생성 시 민감 정보가 화면에 노출되지 않습니다.
* 대상 템플릿을 사용하여 일정/일정 템플릿 복사 시 민감 정보를 제외한 정보만 복사됩니다.

<a id="november-25-2025"></a>
## 2025. 11. 25. { #november-25-2025 }
<a id="added-features"></a>
### 기능 추가 { #added-features }
* 일정 실행 결과 검증 기능이 추가됩니다.

<a id="september-23-2025"></a>
## 2025. 09. 23. { #september-23-2025 }
<a id="september-23-2025-feature-updates"></a>
### 기능 개선/변경 { #september-23-2025-feature-updates }
* 일정 실행 실패 시 오류 원인을 쉽게 확인할 수 있도록 로그 메시지를 개선했습니다.

<a id="june-24-2025"></a>
## 2025. 06. 24. { #june-24-2025 }
<a id="bug-fixes"></a>
### 버그 수정 { #bug-fixes }
* 파라미터(Request Body)를 JSON 객체로만 입력해야 하는 버그를 수정했습니다.

<a id="may-27-2025"></a>
## 2025. 05. 27. { #may-27-2025 }
<a id="may-27-2025-bug-fixes"></a>
### 버그 수정 { #may-27-2025-bug-fixes }
* 시작/종료 일시 시간대에 대한 콘솔 메시지를 수정했습니다.

<a id="april-29-2025"></a>
## 2025. 04. 29. { #april-29-2025 }
<a id="april-29-2025-bug-fixes"></a>
### 버그 수정 { #april-29-2025-bug-fixes }
* 일정 생성 및 수정 시 Cron 표현식을 매주 일요일로 설정하면 일정 실행 시간이 노출되지 않는 버그를 수정했습니다.

<a id="march-25-2025"></a>
## 2025. 03. 25. { #march-25-2025 }
<a id="march-25-2025-added-features"></a>
### 기능 추가 { #march-25-2025-added-features }
* 대상 템플릿 기능이 추가됩니다.

<a id="march-25-2025-feature-updates"></a>
### 기능 개선/변경 { #march-25-2025-feature-updates }
* 일정과 템플릿 생성 및 수정 시 파라미터의 크기를 256KB로 제한하도록 수정했습니다.

<a id="january-21-2025"></a>
## 2025. 01. 21. { #january-21-2025 }
<a id="january-21-2025-feature-updates"></a>
### 기능 개선/변경 { #january-21-2025-feature-updates }
* 일정 생성 시 제한 조건 추가
  * 일정 생성 및 수정 시 URL의 길이를 255자로 제한하도록 수정했습니다.
  * 일정 생성 및 수정 시 파라미터의 크기를 56KB로 제한하도록 수정했습니다.
  * 일정 생성 및 수정 시 시작 일시를 현재 시간으로부터 5분 이후로만 설정 가능하도록 수정했습니다.
* 일정 및 템플릿 검색 시 검색어 앞, 뒤 공백을 무시하도록 수정했습니다.
* 오류 메시지를 수정했습니다.

<a id="december-24-2024"></a>
## 2024. 12. 24. { #december-24-2024 }
<a id="december-24-2024-added-features"></a>
### 기능 추가 { #december-24-2024-added-features }
* 일정 템플릿 기능이 추가됩니다.

<a id="november-26-2024"></a>
## 2024. 11. 26. { #november-26-2024 }
<a id="november-26-2024-bug-fixes"></a>
### 버그 수정 { #november-26-2024-bug-fixes }
* 일정 실행이 간헐적으로 실패하는 버그를 수정했습니다.

<a id="oct-29-2024"></a>
## 2024. 10. 29. { #oct-29-2024 }
<a id="release-of-a-new-service"></a>
### 신규 서비스 출시 { #release-of-a-new-service }
* Cloud Scheduler는 다양한 작업을 원하는 일정에 따라 실행하도록 설정할 수 있는 서비스입니다.