NahamCon CTF 2024 - Uriel
============
<dr>

***

# 핵심 KEY 🔑 
URL 인토딩된 문자를 이중 디코딩하는 방식을 이해한다.   
프로그래밍 언어를 통해 간편하게 URL 디코딩을 하는 방법을 취득한다.   
<br>
#### URL 인코딩 (Encoding)
```
url 인코딩은, 안전하지 않은 ASCII나 URL에 포함될 수 없는 특수문자를 보다 안전하게 나타내기 위해    
"%" 다음에 두 개의 16진수로 문자를 대체하는 과정이다.   
url인코딩의 변환 방식은 각 문자를 % 기호와 함께, 뒤에 두 자리를 16진수로 표현할 수 있다.   
```
 <br><br><br>
***
# WRITEUP 🔒 
 <br><br>
 ![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/a2a6a772-3cc1-46d5-8e84-a5b07cb65632)

<br><br>

해당 문제를 확인해보면 길게 나열되어 있는 %00... 형태로 되어있는 문자들을 확인할 수 있다.   
이를 모듈을 통해 URL 디코딩해서 해석해보아야겠다는 생각이 든다.   
 <br>
이번 CTF에서는 디코딩을 위해 Python의 'urllib.parse' 모듈을 이용해보도록 하겠다.   
 <br><br>
사용 예시)   
```
import urllib.parse

encoded_str = "%25%36%36%25%36%63%25%36%31%25%36%37%25%37%62%25%33%38%25 ... "
decoded_str = urllib.parse.unquote(encoded_str)
print(decoded_str)
```
<br>
Python의 'urllib.parse'는 위와같이 입력해서 디코딩된 문자열을 print할 수 있는 방식이다.   
파이썬 뿐만 아니라 자바스트립트, PHP 에서도 사용할 수 있다.   
 <br><br><br><br>

***
 
#### 첫 번째 디코딩
<br><br>
![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/8cb0f01f-924f-4a0d-82bf-a05d637173e5)
<br>
![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/2569475c-22bf-42fa-b035-2b035bee9e2f)
<br><br>

첫 번째 디코딩을 해보니, 문자열은 더 짧아졌지만 여전히 %00 ... 형태로 출력되는 것을 확인할 수 있다.   
<br>
```
%66%6c%61%67%7b%38%65%66%65%62%36%36%61%37%31%39%62%37%35%61%34%62%37%63%36%33%34%64%38%38%35%37%38%38%64%66%63%7d

** Process exited - Return Code: 0
** Press Enter to exit terminal
```
<br>
이제 결과값으로 출력된 해당 문구를 다시한번 디코딩해줄 것이다.   
 
 <br><br><br>
 
#### 두 번째 디코딩
<br><br>

![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/d1930636-4eb4-4b7d-bc26-e532a90e863d)
<br>
![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/a737e17c-8e5e-4caa-bf1f-7b9656507433)
<br><br>
 
디코딩 된 문자열을 다시한번 디코딩 해보니,<br>
해당 값을 얻어낼 수 있다.<br>
```
flag{8efeb66a719b75a4b7c634d885788dfc}
```
 <br><br><br>
flag를 알아냈다.
 
<br>
![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/cbf8a413-0038-4d89-8bdd-f9a3d71d7b1e)
<br>
<br>

붙여넣으면 Success 문구가 뜨며 성공한다.   
###### 성공!
