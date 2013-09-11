## 실행환경
전자정부 표준프레임워크의 실행환경은 스프링 프레임워크를 중심으로 구성되어 있습니다. 개발환경이 개발의 편이성을 위해서 구성되어 있다면, 실행환경은 실제 서비스에 배포되는 프레임워크와 라이브러리로 구성되어 있습니다. 실행환경의 중심이 되는 스프링 프레임워크에 대한 이해가 있다면 애플리케이션 개발이 어렵지 않을 것입니다. 실행환경 구성을 살펴보고 스프링 프레임워크의 기본을 다루어 보겠습니다.

### 실행환경 개요  
실행환경은 8가지 서비스 그룹으로 구성됩니다. 그림과 같이 공통기반 위에 화면처리, 업무처리, 데이터처리, 연계통합, 배치처리, 모바일 화면처리, 모바일 디바이스 API 레이어(Layer)들이 있습니다.   

<그림> 실행환경 구성 (2.6)  
<img src="./imgs/rte.stack.01.png" style="width: 100%" alt="실행환경 구성 (2.6)">

#### 공통기반 (Foundation Layer)  
공통기반 레이어는 아래 그림과 같이 구성되어 있습니다. 20가지 기능별 컴포넌트들은 실행환경의 각 레이어에서 공통적으로 사용되는 기능을 제공합니다.    
<그림> 공통기반 레이어 구성  
<img src="./imgs/rte.stack.02.foudndation.png" style="width: 100%" alt="공통기반 레이어 구성">

AOP, Cache, Compress/Decompress, Encryption/Decryption, Excel, File Handling, File Upload/Download, FTP, ID Generation, IoC Container, Logging, Mail, Marshalling/Unmarshalling, Object Pooling, Property, Resource, Scheduling, Server Security, String Uril, XML Manipulation 이상 20가지의 공통기능을 제공합니다.
이 중에서 가장 주의깊게 봐야할 것이 IoC Container입니다. 스프링의 핵심이고, 이것을 기준으로 표준프레임워크의 애플리케이션 패턴이 이루어집니다. 나머지 기능들도 각기 중요한 역할을 하기 때문에 후반에 하나씩 살펴보겠습니다.   

#### 화면처리 (Presentation Layer)  
화면처리 레이어는 MVC(Model-View-Controller) 패턴에서 View에 해당합니다. 화면처리 레이어의 구성은 다음과 같습니다.  
<그림> 화면처리 레이어 구성  
<img src="./imgs/rte.stack.03.presentation.png" alt="화면처리 레이어 구성">  

Spring MVC, Internationalization, Ajax Support, Security, UI Adaptor 이상 5가지 기능을 제공합니다.  
MVC 패턴의 프레임워크는 스프링 MVC, 스트럿츠(Struts), 웹워크(Webwork) 등이 있지만, 표준프레임워크에서는 스프링 MVC를 채택하였습니다.  
국제화(Internationalization) 기능은 다국어를 처리하는 방법입니다. 스프링 MVC의 LocaleResolver를 이용합니다. 브라우저 헤더, 세션, 쿠키 등에 있는 언어 정보를 이용해서 해당 언어로 페이지를 보여주는 기능입니다.  
Ajax 지원은 AjaxTags 라이브러리를 이용합니다. Ajax를 이용해 자주 사용되는 기능을 custom tag형태로 제공합니다.  
인증, 권한 같은 일반적인(통상적인) 개념의 Security 서비스는 Spring Security를 활용한 공통기반 레이어에서 제공합니다. 화면처리 레이어의 Security 서비스는 입력값 유효성 검증 기능을 제공한다. 스프링과 연결되는 자카르타 커먼스 밸리데이터(Jakarta Commons Validator)를 이용합니다.  
UI 어댑터는 표준프레임워크와 RIA(Rich Internet Application) 솔루션을 연결하기 위한 기능입니다. 마이플랫폼 등의 상용 솔루션과 연결을 지원하는 기능입니다.    

#### 업무처리 (Business Logic Layer)  
업무처리 레이어는 업무 프로그램의 업무 로직을 담당하는 레이어로서, 업무 흐름 제어, 에러 처리 등의 기능을 제공합니다.  
<그림> 업무처리 레이어 구성  
<img src="./imgs/rte.stack.04.bizlogic.png" alt="업무처리 레이어 구성">  

업무처리 레이어는 Spring Web Flow, Spring 이상 2가지 오픈소스를 사용합니다. 
 

#### 데이터처리 (Persistence Layer)  
#### 연계통합 (Integration Layer)  
#### 배치처리 (Batch Layer)  
#### 모바일 화면처리 (Mobile Presentation Layer)  
#### 모바일 디바이스 API (Mobile Device API Layer)  


### 스프링 프레임워크  

### 스프링 IoC/DI  

### 스프링 MVC  

## 실행환경 구성

### MyBatis와 데이터베이스  

### 오픈소스 프로젝트 소개

## 공통 컴포넌트  

### 공통 컴포넌트 구성  

## 모바일 표준프레임워크  
스마트폰의 등장과 생활 속에서 강력한 파급효과를 보이면서, 업무를 모바일 환경에서 적용하려는 노력이 많아지고 있습니다. 스마트폰에 있는 웹브라우저는 가장 발전이 빠른 웹킷엔진을 사용하고 있습니다. 품질이 좋은 오픈소스가 많이 활용되기 때문입니다. 

### 모바일 표준프레임워크 구성  

#### jQueryMobile 
#### viewport


