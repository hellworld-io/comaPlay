# Play Framework 정리

## PlayFramework???
* [Play Site](https://www.playframework.com/)
* 빨리 쉽게 만들기 위해 유용히 사용가능.
* 고속(애자일) 개발을 위한 웹 프레임워크.
* Fullstack Framework
* All In one
* Deployless Architecture
* Template Engine
* 다양한 Datastore 지원.

## Play 실행
* debug
	* play sbt console에서 run으로 실행하면 사용가능.
* test
	* play sbt console에서 test으로 실행하면 test case에 대한 실행가능.
* production
	* play sbt console에서의 실행이 아닌 기본 console에서 activator(play) start "옵션" 을 실행하여 사용가능.

## Play 개발시 좋은점
* error message가 브라우져에 정확하게 나타남.
* play 서버가 실행중일 때는 서버에 요청시에 자동으로 컴파일을 해주기 때문에 이클립스에서 자체 컴파일 옵션을 꺼두는게 좋음.
* IDE 자체 컴파일이 필요없기 때문에 일반 에디터나 IntelliJ Community버전을 사용해도 무방함.


## 설치 및 설정
### 설치
#### Activator 설치

* [Download](https://www.playframework.com/download)에서 최신버전 다운로드
* 다운로드 완료된 압축파일을 원하는 위치에 압축해제 
``` ex) /Users/yoonjungboo/coma_dev/play/activator-1.2.10-minimal ```

* 압축 해제한 폴더까지의 경로를 환경변수에 추가.
	* [참고](https://www.playframework.com/documentation/2.3.x/Installing)

* brew를 이용한 설치
``` brew install typesafe-activator ```

* activator -help 명령어를 이용하여 설정확인.

#### Activator 실행
* 신규 생성할 프로젝트 폴더로 이동
	```
    	mkdir /Users/yoonjeongbu/coma/dev/comaPlay/helloPlay
		cd /Users/yoonjeongbu/coma/dev/comaPlay/helloPlay
    ```
* 해당 폴더에서 activator 명령어 실행.
![activator 실행](./img/activator_run.png)
* 위 화면이 표시되면 기본 설정 화면이 브라우져에 나타난다. (http://127.0.0.1:8888/home)
* activator new [어플리케이션명] 실행.
``` activator new helloplay ```
![activator new helloplay 실행](./img/helloplay_new.png)

* 생성하고자 하는 어플리케이션 번호 입력
* 각종 라이브러리 및 플러그인 다운로드 후 helloplay이라는 폴더가 생성됨.
* 해당 폴더로 이동.
* activator 명령어 실행
![activator application 실행](./img/activator_application.png)
* play sbt가 실행되면(그림참조) run 명령어로 생성하 어플리케이션 실행
![activator application 실행](./img/activator_application_run.png)
* 서버가 정상적으로 실행되면 http://localhost:9000 으로 확인
* 이상없이 실행되면 application 생성 및 구동완료.
* 가끔 오류가 발생하는 경우가 있음. (아직 안정적이지는 못한듯한 느낌.)


#### play 버젼설치

* [Download](https://www.playframework.com/download#older-versions)에서 2.2버전대를 다운로드
* 다운로드 완료된 압축파일을 원하는 위치에 압축해제 ex) /Users/yoonjungboo/coma_dev/play2/play-2.2.5
* 압축 해제한 폴더까지의 경로를 환경변수에 추가.
	* [참고](https://www.playframework.com/documentation/2.3.x/Installing)

* play -help 명령어를 이용하여 설정확인.


#### play Eclipse 프로젝트 생성하기.

* 새로이 생성한 프로젝트 폴더로 이동.
* 해당폴더에서 activator(play) 명령어 실행하여 play sbt콘솔로 이동.
* sbt 콘솔에서 eclipse 명령어 실행. (play소스파일까지 같이 만들고 싶으면 eclipse with-source=true
 명령어 사용.)
* eclipse 프로젝트 작업이 완료되면 해당 폴더를 eclipse에 프로젝트로 import하여 확인이 가능.