# BaekJoon-Code-Extractor
지금까지 제출한 백준 "맞았습니다" 코드를 추출하는 프로그램 입니다.
![image](https://user-images.githubusercontent.com/31213158/126604636-7b4bb754-5328-4721-a0af-c3ccac8a0c0a.png)


# 작동 방식
* ID와 로그인 쿠키값을 제공받고 그 ID에 해당하는 맞았습니다 페이지로 이동해 현재 페이지의 지금까지 맞은 코드를 전부 추출합니다.
  추출후엔 시간복잡도가 낮은 순서대로 정렬하고 (오름차순),  시간이 같다면 메모리가 낮은 순으로 정렬합니다.
* 그 후 정렬이 끝나면 맨 앞에 있는 것을 뽑고 파일로 저장합니다.  즉 시간복잡도, 메모리가 적게 든 코드를 좋은 코드라고 판단하고 우선 저장합니다.
  뒤에 또 똑같은 문제가 나오면 그땐 다운로드 받지 않고 그냥 넘어갑니다.

* 50점, 100점 등 점수가 있는 서브테스크 문제의 경우에도 나중에 제출한것이 점수가 더 높을것이라고 간주하고 상대적으로 더 앞쪽에 있을것이기 때문에 이런식으로 다운로드 했습니다.
* 똑같은 문제가 또 나왔는데 언어가 다를경우엔 확장자를 달리하여 저장합니다.
  * 지원언어는 Python, C++, C 이며 다른언어는 txt 확장자로 저장됩니다. (이 부분은 추후 수정될 예정입니다.)

# Requirements
```python
pip install beautifulsoup4
pip install requirements
```

사용전 위의 라이브러리를 설치 해주세요.

# How to Use
```python
python3 main.py
```
위 명령어로 프로그램을 실행하시면 백준 ID와 쿠키값 "OnlineJudge" 를 요구합니다.
ID는 백준 ID를 입력하시면 되겠으며 쿠키값의 경우에는 우선 백준에 가서 로그인을 하신 후 F12를 눌러 크롬 개발자 콘솔을 엽니다.

![image](https://user-images.githubusercontent.com/31213158/126604177-c4bc0656-893b-44c6-afae-7b10ee271a9a.png)

그 후 Application 항목을 클릭한 후 왼쪽의 Cookies 탭을 눌러 백준 사이트(www.acmipc.net)를 누릅니다.

오른쪽에 OnlineJudge 값이 표시되며 해당 Value값을 (rr8avifo...) 복사하여 프로그램에 제공해주시면 됩니다.

소스코드는 main.py 파일과 동일한 경로에 Problem Solve라는 폴더가 생성되며 그곳에 저장되게 됩니다.


***주의할 점***  
로그인 후 나오는 OnlineJudge 값을 알기만 하면 다른 컴퓨터에서도 똑같이 당신의 ID로 로그인을 한 것과 동일한 효과를 낼  수 있습니다.

<u>OnlineJudge 값을 절대 모르는 타인에게 유출시키지 마세요.</u>  
본 프로그램의 경우 쿠키값을 추출하거나 다른곳에 유출시키지 않습니다.



