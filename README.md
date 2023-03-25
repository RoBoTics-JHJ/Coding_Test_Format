<p align="center"><img width="100%" height="100%" src="/example.png"></p>

 ## IDEA 
 특별한 설정 없이 main, input, output 3개의 디렉토리를 한 화면에 띄운 뒤에 main.py를 실행시키면
 
 main에서 input을 읽은 뒤에 output에서 결과를 보여주도록 한다. 
 
 한 번에 전체를 볼 수 있어서 편리하고 디버깅을 수월하게 할 수 있다. (코테 문제의 여러 예제 input을 손쉽게 넣어볼 수 있음)
 
 * vscode나 pycharm 상관없이, 어떠한 IDE에서도 별도로 terminal configuration을 수정할 필요가 없음
 
 ## 사용방법
 코테 __1문제당 1개의 디렉토리__ 로 관리할 수 있도록 설계했다. 

 레포지토리를 __로컬에 clone한 뒤, "(문제 제목)"이라는 디렉토리만 남겨두고 사용__ 하면 된다.
  
```
여러 문제 관리하는 방법 ex)인구 이동, 아기 상어 2문제

📁 인구이동
  - main.py
  - input.txt
  - output.txt
📁 아기 상어
  - main.py
  - input.txt
  - output.txt
```

```  
main.py 

⬇️ 실제 코드
# 표준 입출력 파일 설정 ####################################################
import os
import sys
os.chdir(os.path.dirname(__file__))
sys.stdin = open('input.txt', 'r')
sys.stdout = open('output.txt', 'w')
###########################################################################

설명
os.chdir(os.path.dirname(__file__)) >> 현재 python 파일이 있는 디렉토리를 "현재 작업 경로"로 지정
sys.stdin = open('input.txt', 'r') >> 표준입력을 "input.txt" 파일로 지정
sys.stdout = open('output.txt', 'w') >> 표준출력을 "output.txt" 파일로 지정

💡 TIP1
"main.py", "input.txt", "output.txt" 3가지 파일을 모두 열고, 한 화면에 모두 볼 수 있도록 분할한다.
그리고
1. 코테 문제에 있는 input 예제를 input.txt에 복붙한 뒤
2. #### .. ####의 아래부터 코드를 작성하고
3. run을 하면 output.txt에서 결과를 확인할 수 있다.

💡 TIP2. output을 IDE의 기본 Terminal에서 사용하고 싶은 경우
"sys.stdout = open('output.txt', 'w')" 부분을 주석처리 하거나 코드를 지우면 된다.

💡 TIP3
#### .. #### 아래를 모두 드래그 복사하면 백준이나 프로그래머스에 코드를 붙여서 바로 실행시킬 수 있다. 
```
