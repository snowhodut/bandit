The password is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

- Rot13 : 알파벳 글자를 13자리만큼 밀어내 만드는 암호 알고리즘.
	- 알파벳 총 글자 수 : 26개
- `tr 'A-Za-z' 'N-ZA-Mn-za-m'`
	- '대문자 알파벳 A부터 Z, 그리고 소문자 알파벳 a부터 z' -> 'N부터 Z, 그 다음을 A부터 M, n부터 z, 그 다음을 a부터 m' 순서로 치환하라는 뜻
	- tr = transliterate

```
$ cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```