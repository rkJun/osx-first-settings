# OS X First Settings of My Style

어느 웹 개발자의 개인 스타일 맞춤형 OS X 개발환경 세팅.  
**```OS X 10.10 Yosemite`` 를 기준으로 작성했습니다.**

[펭귄너구리](http://blog.doortts.com)님의 글(어떤 개발자의 맥환경 <https://github.com/doortts/env-of-mac>)
을 보고, 저도 개인적인 정리 차원에서 올려둡니다.


## 시스템 환경설정

- 트랙패드
  - 탭하여클릭하기 체크
  - 세손가락으로 드래그하기 체크
  - App Expose 체크
  - (트랙패드의 모든 항목 체크)

- Dock
  - 확대체크 (2/3 범위선택)

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
  - 조합키 - Caps Lock 키를 ^Control 키로 변경
  - 단축키탭 - 전체 키보드 접근 - 모든 컨트롤 선택

 
## AppStore
- Update
- *Xcode*
  - *Command Line Tools*
  ```SHELL
  $ xcode-select --install
  ```

## 구름입력기 설치
<http://gureum.org/> 세벌식 사용자 또는 vi 사용자에게 유리  
- esc 키 로마자전환 활성
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
$ brew install peco		// Simplistic interactive filtering tool
$ brew install tree
$ brew install watch
$ brew install hub
$ brew install jq
```

##### oh-my-zsh
```SHELL
$ curl -L http://install.ohmyz.sh | sh
```

## dotfiles 적용 (for zsh)


### Homebrew cask 로 application 설치

#### Terminal
```SHELL
$ brew cask install iterm2
```

#### Browser 
```SHELL
$ brew cask install chromium
$ brew cask install google-chrome
$ brew cask install firefox
``` 

#### Editor
```SHELL
$ brew cask install sublime-text
$ brew cask install sublime-text3
$ brew cask install macvim
$ brew cask install haroopad
$ brew cask install atom
```

#### Tools

```SHELL
$ brew cask install xmind
$ brew cask install caffeine
$ brew cask install alfred
$ brew cask install bettertouchtool
$ brew cask install diffmerge
$ brew cask install cakebrew
$ brew cask install coconutbattery
$ brew cask install dropbox
$ brew cask install transmission
$ brew cask install virtualbox
$ brew cask install f-lux		// Better lighting for your Mac

```

#### multimedia

```SHELL
$ brew cask install mplayerx
$ brew cask install simple-comic
$ brew cask install vlc
```

#### 압축해제 프로그램

Bandizip X - http://www.bandisoft.co.kr/bandizip/x/

---
## JDK 설치

### JDK8 설치

1. 터미널에서 ```java``` 또는 $```javac``` 입력후,
2. 추가정보 버튼 클릭. (Oracle JDK download 사이트로 포워딩)


***
<!--
## 유용한 팁
1. 모두 표시 (CMD+OPT+SHIFT+H) 단축키 추가 및 Dock Icon (숨김시) 투명 적용  
   <http://macnews.tistory.com/1054>
   ![macnews icon](http://cfile27.uf.tistory.com/original/206B013E4FE755FD15303C "macnews.tistory.com")
   
   $```defaults write com.apple.Dock showhidden -bool YES && killall Dock```

2. 웹브라우저용 스타일 시트 적용  
   <http://macnews.tistory.com/162> ![macnews icon][mnfavi]

[mnfavi]: http://cfile27.uf.tistory.com/original/206B013E4FE755FD15303C "macnews.tistory.com"

3. 개발자에게 추천하는 OS X 훑어보기(QuickLook) 플러그인 6종 + α  
   <http://macnews.tistory.com/830> ![macnews icon][mnfavi]

-->

## Java IDE 설치
 
* Eclipse IDE [Download](<http://www.eclipse.org/downloads/>)

<!--
## 가상머신 설치
* VMWare Fusion
* Parallels 
* VirtualBox

Vmware Fusion 삭제 관련 링크 :  
<http://kb.vmware.com/selfservice/microsites/search.do?cmd=displayKC&docType=kc&docTypeID=DT_KB_1_1&externalId=1017838>

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

### NTFS 외장하드 사용하기

[OS X 에서 NTFS 쓰기. FUSE for OS X, 그리고 NTFS-3G](http://rkjun.wordpress.com/2013/07/14/os-x-%EC%97%90%EC%84%9C-ntfs-%EC%93%B0%EA%B8%B0-fuse-for-os-x-%EA%B7%B8%EB%A6%AC%EA%B3%A0-ntfs-3g/)

또는,

[How to Write to NTFS External Disk Drives from OS X 10.8 Mountain Lion](http://crosstown.coolestguyplanettech.com/os-x/44-how-to-write-to-a-ntfs-drive-from-os-x)  
brew 로 설치하기 (fuse4x, ntsfs-4g)


### 추가폰트 적용
서체관리자
* 나눔고딕코딩  
   <http://dev.naver.com/projects/nanumfont>
* 나눔바른고딕
* 주아체
* 한나체
* Monaco for Powerline
-->