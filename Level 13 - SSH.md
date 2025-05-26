The password is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. 
**Note:** **localhost** is a hostname that refers to the machine you are working on


- *SSH Key = Public Key + Private Key
	- SSH Key는 public key와 private key의 한 쌍으로 구성
		- private으로 암호화된 메시지를 public으로 복호화하는 방식
	- 서버 접속 시 비밀번호 대신 key 제출

- `ssh <host주소> <옵션>`
	- `-p` : 포트 설정
	- `-i` : 키 파일 사용


```
$ ssh -i sshkey.private bandit14@localhost -p 2220
```





fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
