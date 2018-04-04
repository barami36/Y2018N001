└─jks
    └─y2018.n001
        ├─common
        │  ├─crypto
        │  │  └─aes256
        │  │      ├─crypto
        │  │      │  ├─engines
        │  │      │  ├─modes
        │  │      │  ├─paddings
        │  │      │  └─params
        │  │      └─util
        │  │          └─encoders
        │  ├─exception
        │  ├─model
        │  │  └─byteconvertable
        │  ├─props
        │  └─utils
        └─fixedtag
            ├─dao
            ├─dto                 ;dto  처리
            ├─mybatis
            ├─netty               ;netty  관련 모듈
            │  ├─codec
            │  ├─core
            │  │  └─processor
            │  └─utils
            ├─service
            └─web                 ;controller 목록


            
 구현 방식
 1. Ognl 적용
 2. lombok 적용
 3. api는 restful 형태로 구성 
 ==> 참고 프로젝트: http://dev.seeroo.co.kr/svn/sr-ar/trunk/api
 
 
 
### eclipse에서 maven으로 패키징 만들때   

####1. 로컬 
> clean package -Dspring.profiles.active=local(프로파일)

####2. 개발 
> clean package -Dspring.profiles.active=dev(프로파일)

### 톰켓에서 war로 배포할 때
tomcat/bin안에 setenv.sh(리눅스) or setenv.bat(윈도우)파일을 만든다. 

*윈도우*
> set JAVA_OPTS=%JAVA_OPTS% -Dspring.profiles.active=dev

*리눅스*
> export JAVA_OPTS="$JAVA_OPTS -Dspring.profiles.active=dev"
