- 입력한 port번호로 localhost 연결을 해주는 setuid binary 파일
- connection에서 텍스트 라인을 읽어서 bandit20의 password와 비교하고 맞으면 bandit21 password를 보여줌

- 한 터미널에서는 `./suconnect` 파일을 실행해서 임의의 포트에 접속
- 다른 터미널에서는 `nc -l [port]` 커맨드로 임의의 포트에 접속하고 bandit20의 password를 입력
- `./suconnect` 파일이 값을 받아서 bandit21 password를 반환함

EeoULMCra2q0dSkYj561DX7s1CpBuOBt