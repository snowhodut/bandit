The password is stored in the file **data.txt**, which contains base64 encoded data

- BASE64 : 바이너리 데이터를 공통 ASCII 문자로 표현하기 위해 사용하는 인코딩 방법
	- 아스키 문자 하나가 64진법의 숫자 하나를 의미

- `base64` : base64로 인코딩하는 커맨드
- `base64 -d` : base64로 인코딩된 텍스트 파일을 디코딩, 원본 텍스트를 표준 출력에 인쇄하는 커맨드

```
$ base64 -d data.txt
```



- base64로 인코딩된 문자열은 '=' 문자로 끝나는 경우가 많음
	- grep을 사용하여 '=' 문자로 끝나는 문자열을 찾으면, base64로 인코딩된 부분을 찾을 수 있을 것
```
grep = data.txt | base64 -d
```
