# Jubging

<img src="https://user-images.githubusercontent.com/57697721/212832750-776c8823-8ac1-4fe2-8b9c-dbf6ff88de38.png" width="300" height="350">


## Project Introduction

<p align="justify">
한강을 걷다 보면 강변에 쓰레기가 쌓여 있는 모습을 흔히 볼 수 있습니다. 길거리에 버려진 쓰레기는 환경오염의 주범입니다. 쓰레기들은 바람에 날리고 빗물에 씻겨 강이나 해안가로 이동하여 해양 생물체들에게 호흡을 못하게 하고 해양 야생 동물들을 얽혀 죽게 하고 있습니다.

이런 문제를 해결하기 위해 저희는 <strong>줍깅</strong>이라는 서비스를 개발하였습니다.

<p align="justify">
<strong>줍깅</strong>이란, 줍다와 조깅을 결합한 단어로 거리에 버려진 쓰레기를 최대한 많이 주우면서 목적지까지 가벼운 조깅으로 가는 환경보호 운동입니다. 저희는 줍깅 활동을 활성화 시키기 위해 자신이 줍깅 활동으로 배출한 쓰레기의 무게를 측정하는 쓰레기통을 제작하여 배출한 무게 만큼 상점에서 사용 할 수 있는 포인트로 바꿔주는 서비스를 개발하였습니다.
<p align="center">

<p align="justify">
As you walk along streets, you can often see garbage along the sidewalk. Garbage thrown away on the street is the main culprit of pollution. Garbage is blown by the wind and moved by rain to rivers or coasts which is harmful for marine lives. Garbage causes many other problems too.

To alleviate this problem, we thought that it is important to reduce garbage on streets. So we developed this application named "<strong>Jubging</strong>"

<p align="justify">
 "Jubging" is Korean word for "Plogging" which is combination of Swedish word plocka up(picking up) and jogga(jog). Plogging is a fitness trend started in Sweden where you just have to pick up garbage while you jog. To promote this fitness trend, we made a special garbage can that measures the weight of the garbage picked up by users. Our Service converts the weigth of garbage into points. Users can use the points in our market to buy various products.
<p align="center">

<br><br>

## User Process

- 사용자는 저희가 제작한 쓰레기통(줍줍이)의 위치를 어플리케이션을 통해 확인합니다. 
- 사용자는 줍깅을 시작하기 전 줍줍이로 이동하여 줍깅에 필요한 봉투와 집게를 제공 받습니다. 
- 줍깅을 진행합니다. 
- 줍깅이 끝나게 되면 사용자는 다시 근처에 있는 줍줍이로 이동하여 집게를 반납합니다.
- 그 후 쓰레기를 배출하기 전에 이 쓰레기가 줍깅 활동을 통해 배출된 쓰레기인지, 포인트를 부정한 방법으로 얻기 위해 실제 쓰레기가 아닌 물체를 넣었는지 인증을 하기 위해 쓰레기의 사진을 촬영하여야 합니다. 촬영된 사진은 줍깅 서버로 전송되어 줍깅 AI가 물건 당 무게를 계산합니다.
- 이 후 사용자가 배출한 쓰레기의 무게가 물건의 개수에 비해 너무 무거울 경우 해당 사진을 별도의 디렉토리에 보관하여 관리자과 확인 할 수 있도록 구현 하였습니다.
- 사진 촬영이 끝나고 다음 단계로 넘어가게 되면 블루투스로 핸드폰과 줍줍이가 연결되어 줍줍이의 뚜껑이 열리게 됩니다. 사용자는 이제 쓰레기를 버리고 핸드폰으로 무게를 확인 할 수 있습니다. 
- 사용자가 확인 버튼을 누르면 줍줍이의 뚜껑이 닫히게 되고 줍깅 활동이 완료되며 사용자는 배출한 쓰레기의 무게를 기반으로 포인트를 얻게 됩니다. 

- User checks the location of the garbage can through our application.
- User goes to the garbage can to receive tongs and plastic bags needed for plogging.
- User plogs
- When plogging is done, user returns to the garbage can near by and return the tong.
- User has to take a picture of the garbage to verify whether the user put actual garbage. (To prevent users to gain points in a dishonest way) We use yolo to estimate the approximate weight of the garbage in the image.
- If the estimated weight is much more lighter than the measured weight, the image is saved in the server for managers to check.
- After taking a picture, user has to connect with the garbage can through bluetooth. Then the garbage can opens itself. User can throw the garbage and check the weight with their smartphone.
- When user press the confirm button, the garbagecan closes itself and user gets points based on the weight of the garbage. 
<p align="center">

</p>

<br>

## Tech Stack

| SpringBoot | AndroidStudio | YOLOv7 |  Arduino  | MariaDB | 
| :--------: | :-----------: | :----: | :-------: | :-----: |

![image](https://user-images.githubusercontent.com/57697721/212826703-6ab0a6b9-6602-46d3-814c-e7136278b4b5.png)

<br><br>


## Features

### Map
- 구글 맵과 연동하여 현재 줍줍이의 위치를 지도에 표시해줍니다.
  
- Marks location of the garbage cans using google map
  
### plogging data
- 사용자는 줍깅을 시작하여 자신이 줍깅을 하며 뛴 거리, 속도, 소비 칼로리 등을 알 수있습니다.
- 사용자가 쓰레기를 줍줍이에 버리고 나면 줍줍이가 무게를 측정하여 사용자에게 배출한 무게를 알려줍니다.

- User can check the distance, velocity, calories etc while plogging.
- User can chgeck the weight of the garbage
  
### Garbage verifying AI
- 사용자가 마일리지를 얻기 위하여 쓰레기가 아닌 무거운 물체 (돌, 물이 찬 물병 등)을 배출하는 행위를 방지하기 위해 인증 사진을 사용하여 AI가 사용자가 배출한 물체가 쓰레기가 맞는지 판별합니다.
- 쓰레기가 아닌 물체로 판별될 경우 해당 사진을 서버의 특정 디렉토리에 저장하여 관리자가 따로 관리 할 수 있도록 구현했습니다.

- To prevent users throwing away heavy objects that are not garbage (rocks, bottle full of water), AI checks whether the garbage thrown by the user is an actual garbage.
- If it is not verified as an actual garbage, it is saved in the server so that managers can check.

### Sharing
- 사용자가 촬영한 사진과 본인이 기록한 줍깅 데이터를 인스타에 공유 할 수 있습니다.
- 사용자가 촬영한 사진위에 배출한 쓰레기 무게, 총 이동 거리, 걸음 수 등의 데이터가 포함됩니다.

- User can share the plogging data through instagram

### Points
- 배출된 무게 만큼 마일리지로 환산하여 사용자에게 제공됩니다.
- 환산된 마일리지는 앱내의 마일리지 샵에서 여러가지 물품을 구매 할 수 있습니다.

- User gets points based on the weight of the garbage.
- User can buy products with the points

### Hardware (줍줍이)
- 뚜껑<br>
![image](https://user-images.githubusercontent.com/57697721/212826865-8863f9f0-b0f1-46ff-a786-0e702598b98d.png)
- Bluetooth Module (HC-06)<br>
![image](https://user-images.githubusercontent.com/57697721/212826972-177706d8-d595-498f-a373-aee8dcab4266.png)
- Weight sensor (Load cell, HX711)<br>
![image](https://user-images.githubusercontent.com/57697721/212827034-3ee0ecdf-68d0-4d68-b20b-5eb59a715e9c.png)
- Model <br>
![image](https://user-images.githubusercontent.com/57697721/212827086-61566bb6-f136-43ee-b416-5e05924cd401.png)
![image](https://user-images.githubusercontent.com/57697721/212827104-077ac370-571c-4893-8620-b01bdc0eb00a.png)
![image](https://user-images.githubusercontent.com/57697721/212827115-026ed719-4e4d-44a5-8231-3db057170dbf.png)
![image](https://user-images.githubusercontent.com/57697721/212827132-2d7a87a1-2736-4679-bb85-463bbe54624b.png)

## How to run
### Application
- prerequisite : git, Android Studio
1. git clone https://github.com/JUBGING/Jubging_Android.git
2. open folder with android studio
3. Put Googl Map Api Key in the manifest file.
4. Connect AVD or your smartphone.
5. 어플리케이션을 통해 줍깅 활동을 시작하여면 근처에 줍줍이와 블루투스로 연결이 되어야 합니다.

### Hardware
- Prerequisite : Git, Arduino, Arduino uno r3, hc-06, hx711, loadcell sensor, servo motor, 1.5v battery x8, jumper cable, arduino cable, 9v battery
1. git clone https://github.com/JUBGING/jubging_arduino.git
2. open file with arduino. 
3. connect the arduino board and build the code.
4. Execute the code.
5. connect servo motor to 6,7, bluetooth module's txd, rxd to 4,5, load cell's dout, sck to 2,3

## Demo Video
https://youtu.be/oS_OXPgWMsM

<br>
