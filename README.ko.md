# 한글 사용을 위한 추가 설명
* views/*.tt 파일이나 어딘가에 한글(또는 일본어나 중국어, 베트남어 같은 2 byte 문자들)을 쓰면 오류가 발생하는 경우에 참고하기 바랍니다.
* `heroku logs` 명령을 이용하여 로그를 보면 아래와 같은 메시지가 있을 경우에 해결책입니다.
```
Wide character in syswrite at /app/local/lib/perl5/Starman/Server.pm 
```

# 해결책
* app.psgi 파일이 있는 디렉토리에서 config.yml 파일을 만듭니다. 파일 내용은 아래와 같습니다.
```
$ cat config.yml
charset: "UTF-8"
$
```
