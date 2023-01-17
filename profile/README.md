# Jubging

<p align="center">
  <br>
  <img src="./">
  <br>
</p>

목차

## 프로젝트 소개

<p align="justify">
한강을 걷다 보면 강변에 쓰레기가 쌓여 있는 모습을 흔히 볼 수 있습니다. 길거리에 버려진 쓰레기는 환경오염의 주범입니다. 쓰레기들은 바람에 날리고 빗물에 씻겨 강이나 해안가로 이동하여 해양 생물체들에게 호흡을 못하게 하고 해양 야생 동물들을 얽혀 죽게 하고 있습니다.

이런 문제를 해결하기 위해 저희는 <strong>줍깅</strong>이라는 서비스를 개발하였습니다.

<p align="justify">
<strong>줍깅</strong>이란, 줍다와 조깅을 결합한 단어로 거리에 버려진 쓰레기를 최대한 많이 주우면서 목적지까지 가벼운 조깅으로 가는 환경보호 운동입니다. 저희는 줍깅 활동을 활성화 시키기 위해 자신이 줍깅 활동으로 배출한 쓰레기의 무게를 측정하는 쓰레기통을 제작하여 배출한 무게 만큼 상점에서 사용 할 수 있는 포인트로 바꿔주는 서비스를 개발하였습니다.
<p align="center">

<br><br>

## 사용자 프로세스

- 사용자는 저희가 제작한 쓰레기통(줍줍이)의 위치를 어플리케이션을 통해 확인합니다. 
- 사용자는 줍깅을 시작하기 전 줍줍이로 이동하여 줍깅에 필요한 봉투와 집게를 제공 받습니다. 
- 줍깅을 진행합니다. 
- 줍깅이 끝나게 되면 사용자는 다시 근처에 있는 줍줍이로 이동하여 집게를 반납합니다.
- 그 후 쓰레기를 배출하기 전에 이 쓰레기가 줍깅 활동을 통해 배출된 쓰레기인지, 포인트를 부정한 방법으로 얻기 위해 실제 쓰레기가 아닌 물체를 넣었는지 인증을 하기 위해 쓰레기의 사진을 촬영하여야 합니다. 촬영된 사진은 줍깅 서버로 전송되어 줍깅 AI가 물건 당 무게를 계산합니다.
- 이 후 사용자가 배출한 쓰레기의 무게가 물건의 개수에 비해 너무 무거울 경우 해당 사진을 별도의 디렉토리에 보관하여 관리자과 확인 할 수 있도록 구현 하였습니다.
- 사진 촬영이 끝나고 다음 단계로 넘어가게 되면 블루투스로 핸드폰과 줍줍이가 연결되어 줍줍이의 뚜껑이 열리게 됩니다. 사용자는 이제 쓰레기를 버리고 핸드폰으로 무게를 확인 할 수 있습니다. 
- 사용자가 확인 버튼을 누르면 줍줍이의 뚜껑이 닫히게 되고 줍깅 활동이 완료되며 사용자는 배출한 쓰레기의 무게를 기반으로 포인트를 얻게 됩니다. 

<p align="center">

</p>

<br>

## 기술 스택

| SpringBoot | AndroidStudio | YOLOv7 |  Arduino  | MariaDB | 
| :--------: | :-----------: | :----: | :-------: | :-----: |
| ![download](https://user-images.githubusercontent.com/57697721/212822963-ea9d4411-aa16-43ad-850f-833ea0f6ec4a.png)|![download](https://user-images.githubusercontent.com/57697721/212823050-29c4b1ac-30aa-472f-bffc-6f7464120a2a.png)|![download](https://user-images.githubusercontent.com/57697721/212823170-bd44aed4-1d2d-4253-a276-2033da9f47cf.png)|![download](https://user-images.githubusercontent.com/57697721/212823246-c60a4f55-e24b-4eed-b1f4-7bf1042ced9e.png)|![download](https://user-images.githubusercontent.com/57697721/212823310-b51e3fa5-6216-465a-a5eb-4cf77a92d041.jpg)|

![download](https://user-images.githubusercontent.com/57697721/212822919-908cc269-21c7-4638-8157-92d4c9360d1a.png)
hubusercontent.com/57697721/212822616-5c9c4e1f-9d2a-4413-9a48-27aa3dafac38.png)


<br><br>


## 구현 기능

### 기능 1

### 기능 2

### 기능 3

### 기능 4

<br>

## 배운 점 & 아쉬운 점

<p align="justify">

</p>

<br>

## 라이센스

MIT &copy; [NoHack](mailto:lbjp114@gmail.com)

<!-- Stack Icon Refernces -->

[js]: /images/stack/javascript.svg
[ts]: /images/stack/typescript.svg
[react]: /images/stack/react.svg
[node]: /images/stack/node.svg
