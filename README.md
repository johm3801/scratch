# Scratch

스크래치를 활용하여 간단한 게임을 만들어 봅시다.  
방향 키 조작으로 캐릭터를 움직이며, 퀴즈를 맞히는 형식의 게임입니다.  
****
### 스프라이트 만들어보자
스크래치를 다운받은 후 실행했을 때의 첫 화면은 아래와 같습니다.
![scr1](./images/1.png)
<br><br/>
<br><br/>
여기서 기존의 고양이 스프라이트(캐릭터)를 삭제하고 날아가는 모양의 스프라이트로 대체하겠습니다.
![scr2](./images/2.png)
기존의 고양이 스프라이트를 삭제한 후, 우측하단의 '스프라이트 고르기' 아이콘을 클릭하여 'Cat Fyling'을 검색하여 선택해 줍니다. 좌측상단의 '모양'에서 확인해보면 위와 같이 'cat flying-a', 'cat flying-b'가 추가된 것을 확인할 수 있습니다.
<br><br/>
<br><br/>
마찬가지 방법으로 'Glass water', 'Monkey' 스프라이트를 생성해줍니다.
![scr3](./images/3.png)
<br><br/>
<br><br/>
### 배경 만들어보자

다음으로 배경을 변경하겠습니다. 기존의 흰 배경을 삭제하고 'farm', 'desert', 'light'를 각각 검색하여 추가해줍니다.
![scr4](./images/4.png)
<br><br/>
<br><br/>
### 코드를 짜보자

게임에 쓰일 캐릭터, 배경을 세팅해 주었으니 본격적으로 캐릭터 별 코드를 짜봅시다.
<br><br/>
* **게임 시작(?)**

>원숭이가 등장하면서 게임이 시작됩니다. 이야기 형식으로 만들어 보겠습니다.
>![scr8](./images/8.png)
>게임을 시작했을 때 farm에서 원숭이가 등장해 물을 구해 줄 것을 부탁하고 사용자가 '응'이라고 대답을 하면 배경이 desert로 바뀌도록 하였습니다.
<br><br/>
<br><br/>
* **방향키로 캐릭터 조작**  

>오늘 만들어볼 게임에서 고양이의 역할은 물을 구하러 다니는 것! 방향키를 눌러서 상하좌우 움직일 수 있도록 만들어보겠습니다.
>세 개의 스프라이트 중에 고양이 캐릭터를 선택해주고 좌측상단 '코드'에서 작성합니다.
>![scr5](./images/5.png)
>위 사진과 같이 우측방향 키 조작을 할 수있는 코드를 짤 수 있습니다. 마찬가지로 왼쪽, 위, 아래까지 완성해보겠습니다.
>![scr6](./images/6.png)
><br><br/>
><br><br/>
>코드들을 무한반복하기에 넣어주고, 방향 키를 누르지 않았을 때는 'cat flying-b', 방향 키를 눌렀을 때는 'cat flying-a'모양으로 바꾸어 주기 위해 중간에 코드를 추가해 줍니다.
>![scr7](./images/7.png)
><br><br/>
><br><br/>
>배경이 'desert'일때만 고양이가 적절한 위치에서 나타나도록 몇 개의 코드를 더 추가해줍니다.
>![scr9](./images/9.png)
<br><br/>
<br><br/>
* **변수 설정하기**  
>게임에 나올 변수를 설정해 봅시다.  
>이 게임에서는 퀴즈를 풀 때의 제한시간, 물 총 두 개의 변수를 만들텐데 먼저 물부터 만들어봅시다.
><br><br/>
><br><br/>
>![scr10](./images/10.png)
>먼저 우측하단에서 물컵의 사이즈를 적당히 줄여 25로 맞춰주겠습니다.
><br><br/>
><br><br/>
>![scr11](./images/11.png)
>좌측 상단에서 코드>변수>변수만들기 에서 변수이름을 'water'로 지정하고 '모든 스프라이트에서 사용' 선택하여 새로운 변수를 만들어줍니다.
><br><br/>
><br><br/>
>![scr12](./images/12.png)
>같은 방법으로 '제한시간' 변수도 만들어주면 위 사진과 같이 실행화면에서 변수 두 개가 생성된 것을 확인할 수 있습니다.
<br><br/>
<br><br/>
* **물 코드 만들어보자**  

>![scr14](./images/14.png)
>배경이 'desert'일 때만 물컵이 보이도록 코드를 만들어줍니다.
><br><br/>
><br><br/>
>![scr15](./images/15.png)
>변수 'water'가 4가 될때까지 물컵을 무작위 위치로 이동하도록 코드를 짜 줍니다.
><br><br/>
><br><br/>
* **퀴즈 만들어보자**  

>원숭이 스프라이트에서 신호 이벤트와 제한시간 변수를 사용하여 코드를 만들어 줍니다.  제한 시간은 7초로 설정했습니다.
>![scr16](./images/16.png)
><br><br/>
><br><br/>
>![scr17](./images/17.png)
>위 사진과 같이 q1 신호를 받았을때의 스크립트를 작성합니다. 질문을 만들고, 정답여부와 제한시간에 따라 물을 획득할 지 획득하지 못할 지 결정됩니다.
><br><br/>
><br><br/>
>퀴즈를 네 번 맞추면 게임이 종료되도록 앞서 만든 코드블럭을 네 번 복사해서 일부 수정해주고 아래에 추가하겠습니다.
>![scr18](./images/18.png)
><br><br/>
><br><br/>
>마찬가지로 제한시간 코드와 질문 코드를 각각 세번씩 더 복사하여 q2, q3, q4를 만들어줍니다. 신호와 질문 내용, 대답, 'water'변수 값을 알맞게 수정해주세요.
>![scr19](./images/19.png)
><br><br/>
><br><br/>
>퀴즈 4문제를 맞추면 게임이 끝나도록 설정해보겠습니다.  
>clear 신호를 만들고 아래와 같이 코드를 만들어줍니다.
>![scr20](./images/20.png)
><br><br/>
><br><br/>
>앞서 만들었던 q4신호에서 clear 신호를 추가하여 코드를 조금 수정해줍시다.
>![scr21](./images/21.png)
<br><br/>
<br><br/>
* **마무리**  
 
>깃발 모양을 클릭해 게임을 실행해보면, 제한시간 변수에 수정이 필요해 보입니다.
>또, 게임을 한 번 완수한 후에 다시 실행하려 할 때, 'water' 변수 값이 4로 되어있어 게임 실행에 오류가 있는 점,  
>고양이가 'desert'에서 물을 구할 때도 원숭이가 보이고 'light'배경일 때 원숭이가 나타나지 않는 점,  
>고양이 크기가 너무 큰 점을 수정하겠습니다.
><br><br/>
><br><br/>
>![scr22](./images/22.png)
>원숭이 스프라이트에서 코드를 추가해 주었습니다.
><br><br/>
><br><br/>
>마지막으로 고양이의 크기를 50으로 조절해 주면 완성! 수고하셨습니다 :)
