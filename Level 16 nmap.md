- 포트스캔
	- 운영 중인 서버에서 열려 있는 TCP/UDP 포트를 검색하는 것
```
nmap -sT localhost -p 31000-32000
```

![[{3BB339B7-F001-498E-A813-E0E73D6A3C14}.png]]
```
$ openssl s_client -connect localhost:31790 -quiet
```
- `ssh -i`
	- ssh 클라이언트가 특정 개인 키 파일을 사용하여 원격 서버에 연결하도록 지시하는 옵션
	- 기본적으로 SSH는 `~/.ssh/id_rsa`와 같은 기본 키 파일을 사용하지만 -i 옵션으로 다른 키 파일을 지정할 수 있게 됨
```
ssh -i ../../tmp/threefiftynine/ssh-rsa.pub bandit17@localhost-p 2220
```

