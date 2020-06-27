# 구성
마이크로서비스를 구현하기 위한 기술 스택은 여러가지가 있지만 이책에서는 아래 기술을 활용해 마이크로 서비스를 구현합니다. 

* 스프링 부트 2.0
* 스프링 이니셜라이저
* 메이븐
* 인텔리제이 IDEA
* 컴포넌트 스캔
* 스프링 애플리케이션 컨텍스트
* 스프링 설정
* 스프링 표현식 언어(SpEL-Spring Expression Language)



## Mac

### JDK, Maven, Intellij-ce 한번에 설치하는 스크립트
```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install caskroom/cask/brew-cask
brew tap caskroom/versions
brew cask install java8
```



### JDK 설치

JDK는 Java Development Kit의 약자로 Java 어플리케이션을 개발하기 위해 설치해야 하는 플랫폼입니다.

또한, JDK는 Oracle JDK, OpenJDK가 있으며 책에서는 Oracle JDK 설치를 설명합니다.

Mac에서는 homebrew라는 패키지 관리 도구를 활용해 설치할 수 있습니다.

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install caskroom/cask/brew-cask
brew tap caskroom/versions
brew cask install java8
brew install maven
brew install intellij-idea-ce
```



프로파일에 설정합니다.

```bash
vi ~/.bash_profile   ## zsh를 사용할 경우 vi ~/.zshrc

# 제일 아랫쪽에 아래 내용 입력후 저장
export JAVA_HOME=jdk-install-dir
export PATH=$JAVA_HOME/bin:$PATH

# 아래 명령어로 변경된 프로파일 적용
source ~/.bash_profile
```



### Maven 설치

homebrew를 이용해 아래와 같이 설치 합니다.

```bash
brew install maven
```



### Intellij-ce설치

Intellij-ce 는 커뮤니티 버전입니다. 해당 버전도 homebrew를 통해 설치할 수 있습니다.

```bash
brew install intellij-idea-ce
```



(사견 입니다.)

Intellij를 설치하는 방법으로는 여러가지가 있지만 개인적으로는 Jetbrain (Intellij 만든 회사)홈페이지에서 ToolBox 어플리케이션을 이용해 설치하는 것을 추천합니다.

해당 어플리케이션을 이용하면 본인의 프로젝트 확인 및 IDEA 업데이트를 손쉽게 할 수 있고 다른 Jetbrain사의 프로그램을 한번에 활용할 수 있습니다.

아래와 같이 원하는 솔루션 설치를 할 수 있습니다.
<br>
<img src="../../images/jetbrain-toolbox-01.PNG" width="35%" height="35%" >

프로젝트 생성시 Toolbox에서 통합관리 가능합니다.
<br>
<img src="../../images/jetbrain-toolbox-02.PNG" width="35%" height="35%" >



### Spring-Initializer 로 샘플 프로젝트 생성

graph를 구성하고 나면 `Session` 오브젝트를 만들어서 graph를 실행할 수 있습니다. op 생성함수에서 다른 graph를 지정해줄 때까지는 default graph가 `Session`에서 실행됩니다. 관련 내용은 [Session class](../api_docs/python/client.md#session-management)에서 확인할 수 있습니다.



## Windows

