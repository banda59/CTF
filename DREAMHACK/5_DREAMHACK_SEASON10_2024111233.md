🔒DREAMHACK SEASON #10
==================

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FLrnBf%2FbtsHCrvddAZ%2FL59BrKuxv7zhbWmkT4XsgK%2Fimg.png)

HxD로 파일을 decode 해보니 .ELF파일이라는 것을 알 수 있었다.
kali linux에서 실행을 해주어야할 것 같다.
 
![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2F3dwYI%2FbtsHB6ydfDC%2FPK7S56tHSKQ5ux0HZYKiRk%2Fimg.png)

시스템을 가동해보니 해당 문구가 나온다.
environment variable (환경 변수)에 관련된 내용을 숙지해야함을 예측해볼 수 있다.

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcfPT9h%2FbtsHDePxvhO%2FSmQiCP1n0kLOSucDkJ4La1%2Fimg.png)


HxD에도 이런 부분을 확인할 수 있다.
 

![](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FdE7MFl%2FbtsHBOSepKX%2FgNgvbwtRi6FkyCF3pZuZ21%2Fimg.png)

바로 3번 하드코딩 시스템을 구동해버리면 /root/flag에 파일이나 디렉토리가 없다고 뜬다.
환경변수를 설정을 해줘야지 제대로 작동할 것 같다는 생각이 든다.

![image](https://github.com/banda59/CTF/assets/165415245/e568a2c4-bb35-4a76-bc58-2406f9fd00fc)


1.set environment variable에 적절한 값을 입력해야 flag를 얻을 수 있을 것 같은데..
어떤 값을 넣어야 하는지 아직 잘 모르겠다.
 

![image](https://github.com/banda59/CTF/assets/165415245/e9fa571e-cdf2-43e3-800b-da2f6091695d)

알아보니 env라는 명령어는 환경 변수를 관리하고
특정 환경 변수로 새로운 명령어를 실행해 프로그램 테스트, 특정 환경 설정으로 실행해야 하는 경우에
유용한 기능이었다.

포너블에 대한 공부가 더 필요할 것 같다.

 ![image](https://github.com/banda59/CTF/assets/165415245/8d334957-3496-4383-ac49-b44211a8fb50)

sane-env에서 flag를 알 수 있다는 flag의 파일에도 접근해보았다.
 
![image](https://github.com/banda59/CTF/assets/165415245/5ea1831c-27cd-4030-84d2-5eba54ba035e)
 
IDA main()파일을 보다보니 cat ~/flag라는 수상한 문구를 발견했다.
(~) 표시는 루트폴더(/)로부터 사용자폴더(username)까지 경로를 축약한 형태이다.

IDA 디컴파일을 통해 구문을 직접 해석해보아야할 것 같은데 아직 포너블에 대한 지식이 부족하다.


