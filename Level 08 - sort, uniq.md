The password is stored in the file **data.txt** and is the only line of text that occurs only once
- 유일한 라인(한 번만 반복되는 라인) 찾기

- `sort` : 정렬 커맨드
- `uniq` : 입력 내용에서 중복된 항목을 걸러내는 커맨드
	- `uniq -u` : 중복되지 않는 라인만 표시
	- `uniq -d` : 중복되는 라인만 표시
	- `uniq -c` : 각 라인별 중복 횟수를 표시(오름차순으로)

```
$ sort data.txt | uniq -u
```


- sort, uniq 함께 사용하는 다른 예제
```
$ sort data.txt | uniq -d -c | sort -nr
// uniq -c의 결과를 내림차순으로 재정렬
```
