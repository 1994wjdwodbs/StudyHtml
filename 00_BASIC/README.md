# 인터넷 구성 요소 및 제약

## 웹 서버
HTTP 프로토콜을 사용해서 클라이언트가 브라우저를 통해서 요청하는 데이터를 제공하는 인터넷 서비스 프로그램<br/>

### 경량 웹 서버 기능
제한된 자원을 가진 시스템에 사용할 수 있도록 웹 서버의 기능을 제한하고 최적화할 필요가 있음<br/>

> __웹 서버 기능__ <br/>
> 제한된 시스템 자원의 효율적인 사용 – 프로세스/메모리 처리 개선<br/>
> 라즈베리파이와 쉽게 통합 및 이식성이 높아야 함<br/>
> 웹 페이지의 동적 생성 지원 - CGI 및 서버측 스크립트 프로그램<br/>
> 설정 가능한 보안 모델 (제거 가능) – SSL, DAA<br/>
> 기타 로그 파일, 가상 서버, 인증 서버 등의 범용 웹 서버 기능 제한<br/>

> __웹 서버 응용__ <br/>
> 원격 시스템 감시 - 라즈베리파이의 상태 정보나 자료를 확인<br/>
> 원격 제어 - 동적으로 라즈베리파이의 설정 변경<br/>

### 웹 서버 개요
<p align="center">
    <img src="images/브라우저_서버_인터페이스.JPG"><br/> 
    <span><b>웹 브라우저 및 서버</b></span>
</p>

### 웹서버 시스템 구성
보통 __HTTP서버 + 웹응용프레임워크 + 데이터베이스__ 로 구성 (LAMP(Linux + Apache + MySQL + PHP), MAMP, WAMP)<br/>

#### HTTP 서버

|       이름      |            사용   플랫폼           |     라이센스    |                                                                          설 명                                                                         |
|:---------------:|:----------------------------------:|:---------------:|:------------------------------------------------------------------------------------------------------------------------------------------------------:|
|      Apache     |     Unix,   Linux, Windows, Mac    |        APL      |     - 세계에서   가장   많이 사용하는 HTTP   서버     -   Perl,   Python, PHP, JSP 등   다양한 언어 지원 및 모듈 기능     -   http://www.apache.org    |
|     lighttpd    |     Unix,   Linux, Windows, Mac    |        BSD      |     - FastCGI,   SCGI, HTTP proxy, WebDAV   지원     - OpenSSL을   통한 SSL,   TLS 지원     -   http://www.lighttpd.net                                |
|       nginx     |     Unix,   Linux, Windows, Mac    |        BSD      |     - 동적   웹 페이지를 제공하는 HTTP   서버.     - 고부하(동시 10000개   접속)에도   저메모리(~2.5MB)   처리.     -   http://nginx.org/              |

#### 웹 응용 프로그램(프레임워크)
동적 웹 컨텐츠를 생성하는 __CGI 및 스크립트 프로그램__ , 웹 응용 프레임워크를 설치하여 웹 응용 프로그램을 구동<br/>

|     사용 언어     |     종류                                                                          |
|-------------------|-----------------------------------------------------------------------------------|
|     Java          |     Struts, Wicket, Eclipse RAP,   Google Web Toolkit, JSF, JBoss Seam, Spring    |
|     Javascript    |     node.js, SproutCore                                                           |
|     Perl          |     Catalyst, Dancer                                                              |
|     PHP           |     Zend Framework                                                                |
|     Python        |     Django, Flask, Bottle, CherryPy, Grok,   Pylons, web2py                       |
|     Ruby          |     Camping,   Ruby On Rails, Sinatra                                             |

#### 데이터베이스(DB)
특정 조직의 업무를 수행하는데 필요한 상호 관련된 데이터들의 모임<br/>

#### DBMS(DataBase Management System)
사용자와 데이터베이스 사이에서 사용자의 요구에 따라 정보를 생성해 주고 데이터베이스를 관리해주는 소프트웨어<br/>
> __DBMS 특징(5)__ <br/>
> 무결성 : 부적절 자료 저장 방지<br/>
> 일관성 : 삽입/삭제/갱신/생성 후에도 데이터 (변함없이) 일정<br/>
> 회복성 : 장애 발생 시, 특정 상태 복구 성질<br/>
> 보안성 : 불법 노출/변경/손실 보호 성질<br/>
> 효율성 : (응답 시간/저장 공간 활용) 최적화 → 요구 조건 만족<br/>

__SQL 데이터베이스__ <br/>
: MySQL(오픈소스 SQL DB), SQLite(하나의 파일이나 메모리에 데이터베이스를 두는 SQL DB), MsSQL, Oracle, MariaDB, ...<br/>
__NoSQL 데이터베이스__ <br/>
: 전통적인 RDBMS와 다른 DBMS, 데이터 저장에 고정된 테이블 스키마 필요 X, 조인 연산 사용 X, 수평적 확장 가능<br/>
(Ex : Redis (Key/Value), MongoDB(Document), ...)<br/>


## HTTP 프로토콜

### 종단 시스템(end-system)
최종 사용자(end-user)를 위한 애플리케이션을 수행하는 주체<br/>

### 라우터(router)
종단 시스템이 속한 네트워크와 다른 네트워크를 연결함으로써 서로 다른 네트워크에 속한 종단 시스템끼리 상호 데이터를 교환할 수 있도록 하는 장비<br/>

### 종단 시스템과 라우터
<p align="center">
    <img src="images/라우터_인터넷.JPG"><br/> 
    <span><b>시스템 간 인터넷 통신</b></span>
</p>

### 프로토콜(protocol)
종단 시스템과 라우터간, 라우터와 라우터간, 그리고 __종단 시스템과 종단 시스템간 통신을 수행하기 위한 정해진 절차와 방법__ <br/>
(네트워크 요소들 간에 상호작용을 기술하는 알고리즘과 자료구조)<br/>
__네트워크 요소들 간에 주고받는 메시지의 형식과 메시지의 수신 시 취할 동작 및 에러를 어떻게 다룰 것인가__ 를 기술<br/>

### 패킷(packet)
송수신되는 데이터의 블록, 링크 계층에서는 프레임(frame), ISO(International Standards Organization)에서는 PDU(Protocol Data Unit)<br/>
, 상위의 응용 계층에서는 메시지(message)라 함.<br/>

#### TCP/IP 프로토콜
__인터넷의 핵심 프로토콜인 TCP와 IP를 포함한 각종 프로토콜__ <br/>
운영체제에서 구현을 제공하며, 일반 애플리케이션은 운영체제가 제공하는 TCP/IP 프로토콜의 서비스를 사용하여 통신을 수행<br/>

<p align="center">
    <img src="images/인터넷_프로토콜.JPG"><br/> 
    <span><b>인터넷 프로토콜 계층 구조</b></span>
</p>

#### HTTP 프로토콜
월드 와이드 웹(WWW) 상에서 정보를 주고받는 프로토콜이며 주로 HTML 문서를 주고받음, TCP/UDP 및 포트번호 80 사용<br/>
__클라이언트와 서버 사이에 요청(request) 및 응답(response) 방식의 프로토콜__ <br/>

