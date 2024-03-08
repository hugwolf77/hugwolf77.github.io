---
layout: single
title: WSL(Windows subsystem for Linux)
categories: windows
tags: [OS,Windows,WSL]
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
# *WSL(Windows subsystem for Linux)*
---

### 1) WSL(Linux용 Windows 하위 시스템)은 별도의 가상 머신 또는 이중 부팅 없이 Windows 컴퓨터에서 Linux 환경을 실행할 수 있는 Windows의 기능

### [microsoft-doc:wsl](https://learn.microsoft.com/ko-kr/windows/wsl/about)

### 2) Docker DeskTop을 windows 시스템에 설치하기 위해서는 OS 기능 설정의  wsl 사용, Hyper-V, 가상 시스템 사용 등을 사용가능으로 설정하고, WSL이 설치되어 있어야 한다.

### 3) 별도의 VM 엔진 없이, wsl 설치와 Microsoft store 에서 Linux 배포판을 손쉽게 설치하여 사용할 수 있는 방법이다.

### 설치
```bash
wsl --install
wsl --install <Distribution Name>
```

### 설치 가능한  Linix 배포판 확인
```bash
wsl --list --online
```

### 설치된 Linux 배포판 확인
```bash
wsl --list --verbose
```

### 기본 배포 Linux 설정
```bash
wsl --set-default <Distribution Name>
```

### Powershell or CMD에서 특정 배포판의 특정 User 로 실행
```bash
wsl --distribution <Distribution Name> --user <User Name>
```
### WSL 종료
```bash
wsl --shutdown
```

### 등록된 배포판 제거 
```bash
wsl --unregister <DistributionName>
```