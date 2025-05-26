The password is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!)

- hexdump : 컴퓨터 데이터를 16진수로 표시한 것
	- 주로 디버깅이나 리버스 엔지니어링 때 사용됨

- `xxd` : hexdump를 만들거나 복원하는 커맨더
	- **`xxd -r`** : 16진수 데이터를 바이너리 데이터로 변환]

- `tar -xvf`
- `bzip2 -d`
- `gunzip`


```
$ xxd -r data.txt
```

```
mkdir /tmp/myname
cp data.txt /tmp/myname
cd /tmp/myname

(/tmp/myname$) xxd data.txt > zipfile
file zipfile      // 파일 종류 확인 및 정보 출력

// 압축 해제 시 확장자 필수이므로, mv 커맨더로 파일 이름 바꿔주기
mv zipfile zipfile.tar
tar -xvf zipfile.tar

mv zipfile zipfile.gz
gunzip zipfile.gz

mv zipfile zipfile.bz
bzip2 -d zipfile.bz
```


wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw