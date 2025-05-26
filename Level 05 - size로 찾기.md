- 1033 bytes in size

- 파일 크기 기준으로 검색하기
- find는 강력한 명령어이기 때문에 숨겨진 파일도 함께 출력됨
```
find ./* -size 1033c
```

- `find ./* -size +[volume]` -> \[volume] 이상 크기의 파일
- `find ./* -size -[volume]` -> \[volume] 이하 크기의 파일

- 사이즈 단위
	- b : 블록
	- c : **바이트
	- k : 키로 바이트
	- w : 2바이트 워드
	- m : 메가 바이트
	- g : 기가 바이트