---
layout: single
title: "Ubuntu 22.04.03 에서 wine(win-app 실행) 설치"
categories: Ubuntu
tags: [OS,Linux,ubuntu,wine]
toc: true
toc_sticky: true
toc_label: 목차
author_profile: true
sidebar:
    nav: "docs"
search: true
use_math: false
created: "{{date}} {{time}}"
---

---
# *1. Wine ( WineHQ)*  
---
## Wine (:WineHQ)란?

### 1) Windows 시스템에서 Linux 시스템을 사용하는 방법은 여럿 있지만, 그중에서도 [[WSL(Windows subsystem for Linux)]] 은 그 중에서도 별도의 [VM(Virtual Machine)] 엔진 없이 MicroSoft의 지원으로 사용할 수 있는 가상화시스템으라고 할 수 있다. 또한 많은 라이브러리, 프로그램, App, 엔진이 Windows 와 Linux 버전으로 제공된다. 

### 2) 반대로 Linux 에서  Windows 시스템 Application으로만 계발된 경우 직접적으로 사용하기 위한 방법을 제공하는 것이 *Wine*  이다. Wine은 Linux에서 Windows API를 호환하여 Windows App을 실행할 수 있도록 하는 오픈소스 프로젝트입니다. 

### 3) Wine을 사용하면 VM이 없이도 Linux 환경에서 Windows App을 실행할 수 있다

### 4) 와인HQ(WineHQ)는 와인(Wine) 프로젝트의 공식 홈페이지 [WineHQ](https://www.winehq.org/)

### 5) 설치 과정
#### (1) Wine 저장소 key 추가
```bash
wget -qO- https://dl.winehq.org/wine-builds/winehq.key | sudo apt-key add -
```

#### (2) 저장소 추가
```bash
sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ impish main'
```

#### (3) 페키지 목록 업데이트
```bash
sudo apt update
```

#### (4) WineHQ의 stable 버전을 설치
```bash
sudo apt install --install-recommends winehq-stable
```

#### (5) Ubuntu 저장소에서 직접 설치
```bash
# cpu os 아키텍쳐 정보 확인
lscpu
# i386 아키텍처 펙키지 추가
sudo dpkg --add-architecture i386
# Wine 설치 64 32 모두 설치
sudo apt install wine64 wine32
```

#### (6) 설정 및 설치 버전 확인
```bash
winecfg
wine --version
```

#### (7) 제거
```bash
sudo apt remove --autoremove wine64 wine32
```

#### (8) App 설치
```bash
wine <App_name>
```


---
### playonlinux 설치, 사용, 제거
```bash
sudo apt install playonlinux

playonlinux

sudo apt autoremove playonlinux
```