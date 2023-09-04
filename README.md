
- 게임 리그오브레전드의 게임전적확인 사이트를 크롤링하는 코드입니다.   
- 수정할점 :   
    - 크롤링한 게임 기록이 모두 패일경우 오류가 발생함.


# 게임 전적 사이트 크롤링
> 파일이름 : op.gg crawing.py

- 개요 : 게임 리그오브레전드의 게임전적확인 사이트를 크롤링하는 소스코드 입니다
 
- 전체적인 코드흐름:
   셀레니움을 통해 전적갱신시간을 확인하여 몇시간 전 또는 몇일전에 마지막으로 업데이트가 되었다면 전적갱신 버튼을 눌러 데이터를 최신으로 불러옵니다   
   그후 맨아래쪽의 더보기 버튼을 눌러 총 100게의 기록을 불러올수있도록 4번(더보기 버튼을 누를때마다 20게의 기록을 추가로 불러옵니다. 최초 20개의 기록을 기본적으로 불러옴 20+20*4)을 누릅니다.
   html을 불러온후 beautifulsoup를 이용하여 원하는 정보를 뽑아
   판다스로 정리를 합니다

- 현제는 승률을 계산하는 것까지 구현 되어있습니다.

- 버그 :
만약 전적이 승리가 없고 패배의 기록만 있는경우 오류가 발생합니다.


----


# schoolmenu.py

- 학교 기숙사 식단을 크롤링하는 코드입니다.
