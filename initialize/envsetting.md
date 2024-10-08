# 윈도우즈 환경설정

키오스크는 윈도우즈 환경을 제공합니다.

세소정 플랫폼이 윈도우즈에서 원활하게 동작할 수 있도록 환경 설정합니다.



## 윈도우즈 설정

### 절전

#### 화면및 절전

하위 항목 모두 `사용 안함`

### 업데이트 해제

관리자 권한으로 CLI 실행

```
sc config wuauserv start=disabled
```

### 작업 표시줄 자동 숨기기

windows의 작업 표시줄이 나타나지 않도록 자동 숨기기 처리

_설정  > 개인 설정 > 작업 표시줄_에서 `작업 표시줄 자동 숨기기` 체크

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

### 계정 / 로그인 옵션

* [ ] 필요 여부 확인되어야 할 항목

#### 추가 설정

windows를 사용하지 않을 경우 언제 다시 로그인 해야 합니까? `사용 안함`

동적 잠금 _체크 되어있을 경우_ `체크해제`



## 시작 프로그램 지정

실행(윈도우 키 + R) 메뉴를 열고 다음을 입력하면, 시작 폴더가 열립니다.

```shell
shell:common startup
```

시작 폴더에 ㄱ와 [#undefined-7](envsetting.md#undefined-7 "mention")과 [#rustdesk](envsetting.md#rustdesk "mention")의단축아이콘을 각각 복사합니다.

시작폴더에 복사된 단축 아이콘들은 윈도우 시작 시 자동으로 실행됩니다.
