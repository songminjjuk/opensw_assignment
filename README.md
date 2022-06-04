# 1. 리눅스 명령어 : top, ps, jobs, kill 명령어 조사하기
## top: 시스템의 상태를 전반적으로 가장 빠르게 파악 가능(CPU, Memory, Process)
### 실행 전 옵션
+ -b: batch모드
+ -n: top 반복횟수 제한
### 실행 후 옵션
+ shift + p: CPU 사용률 내림차순
+ shift + m: 메모리 사용률 내림차순
+ shift + t: 프로세스가 돌아가고 있는 시간 순
+ -b: Batch 모드로 작동
+ -s: 보안 모드 작동
### 사용 예
$ top [option]
***
## ps: 현재 실행중인 프로세스 목록과 상태를 보여줌
### 옵션
+ -e: 실행중인 모든 프로세스 정보 출력
+ -f: 프로세스에 대한 자세한 정보 출력
+ u: 프로세스 소유자의 이름, CPU의 사용량, 메모리 사용량 등 상세 정보 출력
+ a: 터미널에서 실행한 프로세스의 정보를 출력
+ x: 실행 중인 모든 프로세스의 정보 출력
### 사용 예
$ ps [option]
***
## jobs: 백그라운드에 실행되고 있는 프로세스나 중지된 프로세스의 목록 출력
### 옵션
* -l: 프로세스 그룹 ID를 state 필드 앞에 출력
* -n: 프로세스 그룹 중에 대표 프로세스 ID를 출력
* -p: 각 프로세스 ID에 대해 한 행씩 출력
### 사용 예
$ jobs [option] [job ID]
***
## kill: 프로세스에 특정한 신호를 보내는 명령어, 종료 시킬 때 많이 사용함
### signal 옵션
![kill -l](https://user-images.githubusercontent.com/102357118/171993598-49b4e843-6425-4fed-a0b2-16d7b625b492.PNG)
### 사용 예
$ kill [signal] [pid]

$ kill -9 1234

signal의 default 값은 15이다.
***
# 2. vim 에디터에서 매크로 사용방법에 대하여 조사하기 (q , @)
## 매크로: 특정한 움직임 또는 입력을 저장함으로써 단순하면서 반복되는 동작을 쉽고 빠르게 해주는 것임
q + 알파벳을 눌러 특정 알파벳에 매크로를 저장할 수 있다.
### 매크로 사용 순서
1. q + a       a키에 recording 시작
2. 반복을 위한 내가 원하는 동작
3. q             recoding 종료
4. @a          1회 실행 

or @@         방금 실행한 매크로 실행

or 10@a       매크로 10회 실행
