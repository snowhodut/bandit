The password is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

- `strings` : 실행 파일의 ASCII 문자를 찾아 화면에 출력하는 커맨드
	- binary file or object file에 있는 모든 인쇄 가능한 문자열을 추출하여 출력

- `grep` : 파일에서 특정 문자열이나 패턴을 찾는 커맨드
	- 정규 표현식을 사용
	- 작은따옴표 사용
		- 특수 문자가 있는 경우 따옴표 필요X

```
strings data.txt | grep ===
```
