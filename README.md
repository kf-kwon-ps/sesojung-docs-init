# 필수 프로그램의 설치와 설정

키오스크 생산 후 출하 전 초기화 가이드입니다.

## 크롬

크롬 설치 후 단축아이콘을 바탕화면에 생성.



## 원격  접속 프로그램

[rustdesk-1.2.3-1-x86\_64.exe](https://github.com/rustdesk/rustdesk/releases/download/1.2.3-1/rustdesk-1.2.3-1-x86\_64.exe)



## 결제 에이전트

VAN에 따라 결제 에이전트 구성이 변경되며, VAN Agent와 Mtouch Agent를 각각설치해야 합니다.

현재 지정되는 VAN은 KOVAN과 KSNET입니다.

{% tabs %}
{% tab title="KOVAN (V POS)" %}

{% endtab %}

{% tab title="KSNET (KSCAT)" %}
## Agent 설정

### KSNET 에이전트

[#ksnet](./#ksnet "mention")를 다운로드한 후 kscat 에이전트를 실행합니다.

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

<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### mTouch 결제 에이전트

[#mtouch](./#mtouch "mention")를다운로드하세요.

실행 파일을 더블클릭하여 실행한 후 최소화 또는 창닫기를 하면&#x20;

mTouch 결제 에이전트는 설정 과정이 없습니다.
{% endtab %}
{% endtabs %}







## 홍보 미디어 다운로드

대기화면의 홍보 미디어를 정해진 디렉토리에 다운로드 합니다.

도스 명령어 실행환경 (CLI)에서 다음 명령을 실행합니다.

```shell

mkdir c:/media && curl -o c:/media/media720p.mp4 http://kwonps.iptime.org:8200/media/media720p.mp4
// c 드라이브에 media 디렉토리를 생성합니다.
// media 디렉토리에 media.mp4 파일을 다운로드 합니다.
```

또는 다음 URL에서 미디어 파일을 다운로드 후 `c:/media` 디렉토리에 저장합니다.

```url
http://kwonps.iptime.org:8200/media/media.mp4
```
