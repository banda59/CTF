NahamCon CTF 2024. QRRRRRRRR
============================
<br><br>
 ![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/67c8242b-2f61-4c2a-baf3-88bd5018a559)
<br><br>
# 핵심 KEY.🔑 
기본 QR코드의 구성 형태를 알아본다.
다양한 형태의 QR코드를 알아보고 이를 스캔할 수 있는 방법을 탐색한다.  
<br><br><br>
***
 <br>
# WRITEUP.🔒 
 <br><br>
 ![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/26d03e75-0621-4483-9404-ef6a6af9b204)
<br><br>


먼저 QR code Decoder을 통해 QR코드를 복구해보려고 했지만 복구가 되지 않았다.   
타 디코더 사이트에서도 오류문구가 출력되었다. 그래서 직접 이어붙이기로 했다.   
 <br><br>
 
 ![img1 daumcdn](https://github.com/banda59/CTF/assets/165415245/a01234ae-34b0-4e86-831b-d1c0b2564719)

<br><br>

그 다음으로는 Photoshop의 ruler 기능을 이용해서 n등분해 정사각형 형태로 이어붙일 수 있을지 확인해보았다.   
하지만 이상하게 여겨졌던 점은 QR코드를 등분하기도 애매했고, 또한 각각의 위치에 있어야할 위치 심볼이 하나밖에 없다!!   
 <br>
따라서 아예 긴 코드 형식으로 되어있는 독립적인 QR코드가 있는게 아닐까? 하고 추측해볼 수 있었다.   
 
 <br><br>
![image](https://github.com/banda59/CTF/assets/165415245/7bdf215c-63c4-40fc-9610-434da1095ab2)


<br><br>
구글링을 해보니 QR코드를 발명한 덴소( 株式会社デンソー) 컴퍼니에서 새로 발명한 rMQR이라는 QR코드였다.   
이제 코드를 스캔할 수 있겠다.
 <br>
 
하지만 해당 QR code는 일반적인 코드 스캐너나 카메라로 인식이 불가했는데,   
SCANDIT app이 이를 지원한다고 해서 이 어플리케이션을 설치했다.
 <br><br>
![image](https://github.com/banda59/CTF/assets/165415245/516f9c09-b9c9-46de-b927-006d2d3db22a)


![image](https://github.com/banda59/CTF/assets/165415245/5bfde858-8b54-4741-9ab2-610a0182ff41)



 <br><br><br>
```
flag{a44557e380e3baae9c21c738664c6142}
```
<br>
ANY CODE를 누른 후 스캔해보니 해당 내용을 확인할 수 있었다.
 <br><br>
 
![image](https://github.com/banda59/CTF/assets/165415245/c15604f2-fc9f-457c-a489-a8f56593ff70)
 <br><br><br>
플래그를 입력하면 Success 문구가 뜨며 정상적으로 제출이 된다.   
<br>
성공!
