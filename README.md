# OS X First Settings of My Style

어느 웹 개발자의 개인 스타일 맞춤형 OS X 개발환경 세팅.  
**```OS X 10.10 Yosemite``` 를 기준으로 작성했습니다.**

[펭귄너구리](http://blog.doortts.com)님의 글(어떤 개발자의 맥환경 <https://github.com/doortts/env-of-mac>) 을 보고, 저도 개인적인 정리 차원에서 올려둡니다.


## 시스템 환경설정

- 일반
  - 스크롤 막대 보기 - 항상 체크
 
- 트랙패드
  - 탭하여클릭하기 체크
  - 세손가락으로 드래그하기 체크
  - App Expose 체크
  - (트랙패드의 모든 항목 체크)

- Dock
  - 확대 체크 (2/3 범위선택)
  - 화면에서의 위치 - 왼쪽 체크
  - 응용 프로그램 아이콘 속으로 윈도우 최소화 체크

- 보안 및 개인 정보
  - 다음에서 다운로드한 App - 모든 곳 체크
 
- 핫코너
  - 좌측 상단 - Mission Control
  - 우측 상단 - 알림센터
  - 좌측 하단 - 응용프로그램 윈도우
  - 우측 하단 - Launchpad

- 키보드
  - 키반복 최대한 빠르게, 반복지연시간 최대한 짧게
  - 모든 F1, F2 등의 키를 표준 기능 키로 사용 체크
  - 보조 키 - Caps Lock 키를 ^Control 키로 변경
  - 텍스트탭
    - 자동으로 맞춤법 수정 체크해제
  - 단축키탭
    - 손쉬운 사용 - 색상반전 체크
    - Spotlight - Spotlight 검색 보기 - opt + space 로 변경  
      (ctrl + space 단축키는 Alfred에서 사용)
    - 전체 키보드 접근 - 모든 컨트롤 선택

- 공유
  - 컴퓨터명 변경

- 손쉬운 사용
  - 확대/축소 - 확대/축소하려면 스크롤 동작을 다음 조합키와 함께 사용 체크
 
- Finder
  - view 관련 설정  
 
## AppStore
- Update
- *Memoery Clean*
- *iPhoto, Pages, Numbers, Keynote.*
- *wunder list* (to-do app)
- *Airmail* (mail client $1.99) : 차기 버전 나왔으나 구매 고민중..
- *Xcode*
  - *Command Line Tools*
  ```SHELL
  $ xcode-select --install
  ```

## 구름입력기 설치
<http://gureum.org/> 세벌식 사용자 및 vi 사용자에게 유리  
- esc키로 로마자 자판으로 전환 (vi모드) 체크
- 자판 전환시 스페이스 입력 방지 (IntelliJ 등) 체크
- 한자 및 이모티콘 입력에 편리함 (opt+enter)

***
## Homebrew 설치
- http://brew.sh 설치 명령어 참조

### Homebrew 로 설치하기

#### brew cask 설치 (http://caskroom.io)
```SHELL
$ brew install caskroom/cask/brew-cask
```
application beta판도 cask로 설치하고 싶으면 아래 명령 추가 
```SHELL
$ brew tap caskroom/versions
```


#### git, zsh, tmux, node and more...
```SHELL
$ brew install git
$ brew install zsh
$ brew install tmux
$ brew install node
$ brew install tig		// Text-mode interface for git
$ brew install tree
$ brew install watch
$ brew install hub
$ brew install jq
```

##### oh-my-zsh
```SHELL
$ curl -L http://install.ohmyz.sh | sh
```
#### rbenv
```SHELL
$ brew install rbenv ruby-build
...
$ echo 'eval "$(rbenv init -)"' >> ~/.zshrc
...
$ rbenv install 2.1.2 // ruby 2.1.2 install
$ rbenv global 2.1.2  // set ruby 2.1.2 global
```

### dotfiles 적용 (for zsh)
- 추후 작성

### Homebrew cask 로 application 설치

#### Terminal
```SHELL
$ brew cask install iterm2
```

#### Browser 
```SHELL
$ brew cask install chromium
$ brew cask install firefox
$ brew cask install firefoxdeveloperedition
``` 

#### Editor
```SHELL
$ brew cask install sublime-text3
$ brew cask install macvim
$ brew cask install haroopad
```

#### Tools

```SHELL
$ brew cask install alfred
$ brew cask install bettertouchtool
$ brew cask install caffeine
$ brew cask install coconutbattery
$ brew cask install diffmerge
$ brew cask install dropbox
$ brew cask install transmission
$ brew cask install vagrant
```
##### brew cask install alfred 설치후, 

- alfred scope 에 Caskroom 포함
  ```SHELL
  brew cask alfred link
  ```

#### multimedia

```SHELL
$ brew cask install mplayerx
$ brew cask install simple-comic
$ brew cask install vlc
```

#### 협업 Tools
```SHELL
$ brew cask install hipchat
$ brew cask install slack
```

#### JAVA IDE
```SHELL
$ brew cask install intellij-idea-eap   // IntelliJ IDEA Early Access Program (EAP)

## 가상머신 설치
- VirtualBox [Download](https://www.virtualbox.org/wiki/Downloads)
- (유료) Parallels Desktop 또는 VMWare Fusion

<!--
#### 압축해제 프로그램

Bandizip X - http://www.bandisoft.co.kr/bandizip/x/
-->

---
## JDK 설치

### JDK8 설치

1. 터미널에서 ```java``` 또는 $```javac``` 입력후,
2. 추가정보 버튼 클릭. (Oracle JDK download 사이트로 포워딩)

***

## 유용한 팁
1. 모두 표시 (CMD+OPT+SHIFT+H) 단축키 추가 및 Dock Icon (숨김시) 투명 적용  
   <http://macnews.tistory.com/1054>
   ![macnews icon](http://cfile27.uf.tistory.com/original/206B013E4FE755FD15303C "macnews.tistory.com")
```SHELL
$ defaults write com.apple.dock showhidden -bool YES && killall Dock
```

2. 개발자에게 추천하는 OS X 훑어보기(QuickLook) 플러그인 6종 + α  
   <http://macnews.tistory.com/830> ![macnews icon][mnfavi]



## Java IDE 설치
 
* Eclipse IDE [Download](<http://www.eclipse.org/downloads/>)

 
### Sublime Text 설정

[Sublime Text][st] 설정하기

#### Package Control 설치

* https://sublime.wbond.net/installation

#### 환경설정파일

* [전체](https://gist.github.com/rkJun/5733996)
   - [Default (OSX).sublime-keymap](https://gist.github.com/rkJun/5733996#file-default-osx-sublime-keymap)
   - [Package Control.sublime-settings](https://gist.github.com/rkJun/5733996#file-package-control-sublime-settings)
   - [Preferences.sublime-settings](https://gist.github.com/rkJun/5733996#file-preferences-sublime-settings)

[st]: http://sublimetext.com

+ [cobalt2 theme](https://github.com/wesbos/cobalt2) 추가 

<!--
### 추가폰트 적용
서체관리자
* 나눔고딕코딩  
   <http://dev.naver.com/projects/nanumfont>
* 나눔바른고딕
* 주아체
* 한나체
-->
<!-- * Monaco for Powerline -->
