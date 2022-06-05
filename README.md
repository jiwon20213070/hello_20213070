# 컴퓨터공학과 이지원 20213070


## **리눅스 명령어 (top, ps, jobs, kill) 정리**
------------------------------------------------

|리눅스 명령어|사용 용도|
|:---|:---:|
|top|시스템 프로세스/메모리 사용 현황을 실시간으로 출력|
|ps|현재 실행 중인 프로세스를 보여주는 명렁어|
|jobs|작업이 중지된 상태나 백그라운드 진행 중인 상태를 표시|
|kill|프로세스에 특정한 시그널을 보내는 명령, 옵션 없이 실행하면 종료 신호 보냄|

**top의 명령어 옵션**
|옵션|설명|
|:---|:---:|
|-d 갱신 시간| 갱신 시간 설정(초 단위)|
|-p| 특정 PID값을 갖는 프로세스를 모니터링 할 때 사용|
|-b|배치 모드로 실행하는 옵션, 다른 프로그램이나 파일에 전송할 때 사용|
|-n 값| top명령의 실행 횟수를 지정하는 옵션|


**ps의 명령어 옵션**


|옵션|설명|
|:---|:---:|
|*ps*| pid, cmd 등 프로세스의 기본적인 내용만 출력|
|*ps -e*| 모든 프로세스를 출력|
|*ps -f* | 풀 포맷으로 출력(uid, pid, ppid TTY 등 정보 보여줌)|
|*ps -l* |긴 포맷으로 출력 (풀 포맷+F,SPRI 등 정보를 더 보여줌)|
|*ps -p 1* | 프레스 번호가 1인 프로세스 출력|
|*ps -u*| 특정 사용자의 프로세스 정보를 확인할 때 사용|


`$ ps -ef | more ` 모든 프로세스 풀 포맷 출력, more 명령어 이용하여 페이지 단위로 출력


`$ ps -ef | grep seek` 모든 프로세스를 풀 포맷으로 출력한 목록에서 grep을 이용해 seek이 포함된 행 출력


+)위 옵션 외에도 많은 ps 명령어 옵션
<img width="372" alt="오픈소스 ps" src="https://user-images.githubusercontent.com/106908310/172052270-642671aa-2b89-45a9-ac63-595c87ffc994.PNG">





**jobs의 명령어 옵션**

|옵션|설명|
|:---|:---:|
|jobs|백그라운드 프로세스 출력|
|jobs -l|프로세스 번호(PID)를 추가하여 백그라운드 프로세스 출력


**kill의 명령어 옵션**

|옵션|설명|
|:---|:---:|
|-ㅣ|시그널의 종류 출력|
|-s signal|시그널의 이름을 지정|


## ***vim 매크로 활용법***
-----------------------------------


**Macro는 Vim 명령어들을 기록하고, 이를 반복할 수 있는 기능**

**Macro 사용 시 소스수정이나 추가할 때 매크로를 잘 활용하면 작업의 시간을 많이 줄일 수 있음**

### **Vim Macro** 실행 순서

1) q{name}로 매크로 기록 시작 ex)qa라고 누르면 qa라는 매크로 기록 시작
2) q매크로 기록 종료
3) @{name}로 저장된 매크로 실행
4) @@로 직전에 실행한 매크로 재실행
5) {반복횟수}@{name} 또는 {반복횟수}@@로 저장된 매크로를 '반복횟수'만큼 재실행
