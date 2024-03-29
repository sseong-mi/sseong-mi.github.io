---
title: "[Mathematical] Monte Carlo Methos 수학적 기초 지식"

categories:
 - Mathematical
tags:
  - math
  - deep learning
search: true

---

## 우분투 아나콘다 다운로드 및 설치

1. [아나콘다 홈페이지](https://www.anaconda.com/products/distribution) 에서 리눅스 설치파일을 찾는다. 
2. 리눅스 설치파일의 링크 주소를 복사한다. 
3. 우분투에서 설치 파일을 다운로드 할 디렉토리로 이동한 후 다음의 명령어를 실행시킨다. 
   
```
wget "아까 복사한 설치 파일 링크"
```
   
4. 다운로드가 끝났다면 `sh` 명령어를 이용해 다운로드 한 bash 파일을 실행시킨다. 
5. 다운로드 진행 중 아나콘다의 설치 경로를 원하는 곳으로 설정할 수 있다. 

## 우분투 아나콘다 환경 변수 PATH 설정 

우분투에서 아나콘다를 설치한 후에 `conda` 명령어를 사용하려 했는데 다음과 같은 오류가 발생했다. 

```
conda: command not found
``` 

찾아보니 환경 변수 PATH 설정으로 인한 오류라고 한다.   
아래의 코드를 실행하여 문제를 해결했다.   

``` 
export PATH="home/smwoo/programs/anaconda3/bin:$PATH"
```

`home/smwoo/programs/anaconda3` 를 개인의 경로에 맞춰 변경하여 넣으면 된다. 

코드 실행 후에 터미널에 다시 접속하면 `conda`가 잘 작동하는 것을 확인할 수 있다!

참고: <https://stackoverflow.com/questions/35246386/conda-command-not-found>


## 아나콘다 base enviroment 자동 활성화 해제

아래의 명령어를 통해 base 환경 자동 활성화를 해제할 수 있다. 
```
conda config --set auto_activate_base false
```
이후 터미널을 재시작하면 자동 활성화가 꺼진 것을 확인할 수 있다!