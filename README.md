## 1. 'top'

top 명령어는 실시간으로 시스템의 프로세스 및 자원 사용 상태를 모니터링할 수 있는 툴입니다. 기본적으로 CPU, 메모리, 스왑 사용량과 각 프로세스의 사용량을 실시간으로 표시합니다.

### 사용법
'''bash
top
![top]https://github.com/dlsrb11/dlsrb11/blob/main/top.png
주요 화면 설명
* PID: 프로세스 ID
* USER: 프로세스를 실행한 사용자
* PR: 우선순위
* NI: nice 값 (우선순위 조정 값)
* VIRT: 가상 메모리 사용량
* RES: 실제 메모리 사용량
* SHR: 공유 메모리 사용량
* S: 프로세스 상태 (R: 실행 중, S: 대기, T: 중지, Z: 좀비)
* %CPU: CPU 사용 비율
* %MEM: 메모리 사용 비율
* TIME+: 총 CPU 사용 시간
* COMMAND: 실행된 명령어
* 추가 옵션
* c: 명령어와 전체 경로를 표시합니다.
* H: 스레드를 표시합니다.
* p <PID>: 특정 PID의 프로세스를 모니터링합니다.


## 2. ps
ps 명령어는 현재 실행 중인 프로세스의 스냅샷을 보여줍니다. 다양한 옵션을 통해 출력 형식을 조정할 수 있습니다.

주요 옵션
옵션	설명
* a	터미널에 종속되지 않은 모든 프로세스를 출력합니다.
* u	프로세스의 소유자와 CPU, 메모리 사용량을 출력합니다.
* x	제어 터미널이 없는 프로세스도 출력합니다.

예시

ps aux

## 3. jobs

jobs 명령어는 현재 셸 세션에서 백그라운드로 실행 중인 작업 목록을 보여줍니다.

주요 상태
* Running: 실행 중인 작업
* Stopped: 중지된 작업
* Done: 완료된 작업
* Terminated: 종료된 작업

예시
* [1]+  Running                 sleep 100 &
* [2]-  Stopped                 vi

## 4. kill
kill 명령어는 프로세스를 종료하거나 특정 시그널을 보낼 때 사용됩니다.

### 사용법

kill [옵션] &lt;PID&gt; 


주요 시그널
시그널	    설명
* SIGTERM (15)	정상 종료 시그널 (기본 시그널)
* SIGKILL (9)	강제 종료 시그널 (프로세스를 즉시 종료)
* SIGSTOP (17, 19, 23)	프로세스를 일시 정지
* SIGCONT (18, 25, 26)	정지된 프로세스를 다시 실행

예시
* kill &lt;PID&gt;            # 기본 시그널 SIGTERM 사용
* kill -9 &lt;PID&gt;         # SIGKILL 시그널 사용
* kill -SIGSTOP &lt;PID&gt;  # 프로세스 일시 정지
* kill -SIGCONT &lt;PID&gt;   # 프로세스 다시 실행






