# 환경설정

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



## 크롬 설정

단축아이콘의 등록 정보의 명령을 다음과 같이 변경

**개발 서버용**

{% tabs %}
{% tab title="일반 디버깅 모드" %}
핀치 제스쳐 허용

```
"C:\Program Files\Google\Chrome\Application\chrome.exe" --user-data-dir="C:\chrome-dev" --disable-web-security --disable-notifications https://kioskdev.sesojung.com/
```
{% endtab %}

{% tab title="키오스크 모드" %}
핀치 제스쳐 허용

```
"C:\Program Files\Google\Chrome\Application\chrome.exe" --user-data-dir="C:\chrome-dev" --disable-web-security --disable-notifications --kiosk https://kioskdev.sesojung.com/"
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
개발 서버 접속 시에는 핀치 제스쳐를 허용합니다.
{% endhint %}

**상용 서버용**

{% tabs %}
{% tab title="키오스크 모드" %}

{% endtab %}

{% tab title="일반 디버깅 모드" %}

{% endtab %}
{% endtabs %}

{% tabs %}
{% tab title="키오스크 모드" %}
핀치 제스쳐 불가

```
"C:\Program Files\Google\Chrome\Application\chrome.exe" --user-data-dir="C:\chrome-prod" --disable-web-security --disable-notifications --disable-pinch --kiosk https://ki.sesojung.com/"
```
{% endtab %}

{% tab title="일반 디버깅 모드" %}
핀치 제스쳐 허용

```
"C:\Program Files\Google\Chrome\Application\chrome.exe" --user-data-dir="C:\chrome-prod" --disable-web-security --disable-notifications https://ki.sesojung.com/"
```
{% endtab %}
{% endtabs %}

{% hint style="info" %}
상용 서버 접속 시에는 '일반 디버깅 모드'에서만 핀치 제스처를 허용합니다.
{% endhint %}

변경된 단축아이콘은 시작프로그램으로 등록하여 윈도우가 시작될 때마다 접속하도록 합니다. ([#undefined-14](envsetting.md#undefined-14 "mention"))

### 세소정 초기 환경

크롬에서 [세소정 키오스크](https://ki.sesojung.com)(https://ki.sesojung.com)로 접속하여 키오스크를 인식하고 플랫폼과 연결하기 위해 초기화를 수행합니다.

키오스크 초기화는 **새소정 키오스크 웹페이지에 접속 할 때마다** 수행됩니다.



보통은 자동으로 초기화를 처리하지만 키오스크의 정보를 활용할 수 없을 경우  다음 과정을 거칠 수 있습니다.

#### 키오스크 장치 연결

키오스크와 장치들과 연결 실패

## rustdesk 설정

### 영구 비밀번호

rustdesk 설치 후 영구 비밀번호를 지정해야 합니다.

rustdesk를 실행하여 좌측 패널의 `설정`을 클릭합니다.

설정화면의 좌측 패널에서 `security`를 선택한 후 우측 패널에서 `영구 비밀번호`를 설정합니다.

영구 비밀번호는 사전 정의된 값을 입력합니다.

알파미트의 업무 담당자에게 rustdesk ID와 영구비밀번호를 전달합니다.

## 결제 에이전트 설정

### KSNET 에이전트

[#ksnet](../#ksnet "mention")의 kscat 파일을 실행 후 에이전트를 실행합니다.

에이전트는 다음 두가지 방법 중 선택할 수 있습니다.

{% tabs %}
{% tab title="윈도우 task bar" %}
task bar의 아이콘을 더블클릭하여 실행
{% endtab %}

{% tab title="설치 위치에서 실행" %}
C:\kscat 디렉토리에서 KSCAT.EXE 파일 실행
{% endtab %}
{% endtabs %}

에이전트 실행 후 다음과 같이 설정합니다.

1. 실행하여 "1. 암호화 리더기"의 `'자동 검색'` 클릭합니다.
2. 포트가 정상적으로 잡히면 `'테스트'`하여 무결성 을 점검합니다.
3. 상기 1\~2번이 모두 완료되면 하단의 `'서비스 시작'`을 클릭하여 에이전트 실행을 완료합니다.

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### mTouch 결제 에이전트

[#mtouch](../#mtouch "mention")의  실행 파일을 더블클릭하여 실행한 후 최소화 또는 창닫기합니다.

mTouch 결제 에이전트는 설정 과정이 없습니다.



## 시작 프로그램 지정

실행(윈도우 키 + R) 메뉴를 열고 다음을 입력하면, 시작 폴더가 열립니다.

```shell
shell:common startup
```

시작 폴더에 [#ksnet](envsetting.md#ksnet "mention")와 [#undefined-7](envsetting.md#undefined-7 "mention")과 [#rustdesk](envsetting.md#rustdesk "mention")의단축아이콘을 각각 복사합니다.

시작폴더에 복사된 단축 아이콘들은 윈도우 시작 시 자동으로 실행됩니다.
