NahamCon CTF 2024 - Copypasta 
=======================
![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/e7403ef0-ebd9-406f-aa75-563b31b085e8)

# 핵심 KEY 🔑 
#### 리눅스(Linux)의 Netcat(nc) 명령어를 이해한다.    
 <dr> <dr>

Netcat(nc)란 TCP, UDP 프로토콜을 사용하여 네트워크 연결을 통해 데이터를 전송하고 수신할 수 있도록 만들어진 명령줄 도구이다.    
넷캣에는 '서비스 테스트'라는 기능이 있는데, 이 기능에서 특정 host의 특정 port로 이동하여 서비스가 제대로 작동하는지를 테스트할 수 있다.    
(웹 서버, FTP 서버, SSH 서버 등)   
기본적으로는 특정 호스트의 특정 포트에서 해당 포트가 열려있는지, 또는 파일을 전송할 수 있는 방법을 제공한다.   
  <dr>

![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/34cb2d98-e9cd-45a4-ae3b-a40a9f5df885)

 <dr>

start를 누르면 해당 명령어가 뜨는데, nc와 31476이라는 포트번호가 뜨는 것을 보아하니넷캣 명령어를 사용해주어야 한다는 것을 알 수 있다.
  <dr>
 <dr>
 <dr>
  <dr>

***
# WRITEUP🔐
 <dr>
 
![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/f3634777-1901-4267-ad75-97d85b4ea495)

  <dr>



해당 명령어를 칼리 리눅스에 입력하니, 포트 연결에 성공하면서 해당 내용이 나타났다.   
하지만 flag는 보이지 않는다.   
  <dr>

이때 보이는 문구를 복사해서 메모장에 붙여넣어보니   
 <dr>
 <dr>

```
I'd just like to interject for a moment. What you're referring to as Linux, is  
in fact, GNU/Linux, or as I've recently taken to calling it, GNU plus Linux.    
Linux is not an operating system unto itself, but rather another free component 
of a fully functioning GNU system made useful by the GNU corelibs, shell        
utilities and vital system components comprising a full OS as defined by POSIX. 
                                                                                
Many computer users run a modified version of the GNU system every day, without 
realizing it. Through a peculiar turn of events, the version of GNU which is    
widely used today is often called Linux, and many of its users are not aware    
that it is basically the GNU system, developed by the GNU Project.              
                                          flag{1f68e019b29650f6e8ea15a7808f76fd}                                                    
There really is a Linux, and these people are using it, but it is just a part of                                                    
the system they use. Linux is the kernel: the program in the system that                                                            
allocates the machine's resources to the other programs that you run. The kernel                                                    
is an essential part of an operating system, but useless by itself; it can only                                                     
function in the context of a complete operating system. Linux is normally used                                                      
in combination with the GNU operating system: the whole system is basically GNU                                                     
with Linux added, or GNU/Linux. All the so-called Linux distributions are really                                                    
distributions of GNU/Linux!
```
 <dr>
 <dr>

 
가려져 있던 추가된 내용을 확인할 수 있다.
  <dr>
 <dr>
 <dr>

 
```
flag{1f68e019b29650f6e8ea15a7808f76fd}
```
 <dr>

flag를 발견했다.
 
  <dr>
 <dr>
 <dr>
***
 <dr>

 
 ![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/abf1b780-6632-4497-90d3-c148e9f920da)

 <dr>

이후 해당  flag를 제출하면 Success 문구와 함께 성공적으로 반영이 되었다.   
성공!
