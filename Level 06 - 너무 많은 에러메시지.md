- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
- 'Permission denied'

- `find` 옵션
	- `find -user` : 지정한 사용자 소유
	- `find -group` : 지정한 그룹 소유
	- `find -size` : 파일 크기로 찾기


- 에러 메시지 때문에 원하는 결과를 찾기 어려운 경우 -> **표준 에러 리다이렉션을 이용
	- 표준 출력(1)
	- 표준 에러(2)
	- 백그라운드(&)

- 모든 에러를 출력하지 않으려면
	- **`2>/dev/null`
		- e.g. `$ find / -size 33c 2>/dev/null`
- 'Permission denied'만 제거하려면
	- 표준 에러를 표준 출력으로 리다이렉션 후 grep하기
	- **`2>&1 | grep -v Permission`
		- "표준 에러(2)를 백그라운드(&)로 표준 출력(1)에 보내라(>)"
		- e.g. `$ find / -size 33c 2>&1 | grep -v Permission`

