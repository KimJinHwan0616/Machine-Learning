https://wikidocs.net/92110
># Matplotlib
>그래프
>### 산점도, 선, 막대, 히스토그램
>### 파이, 박스 플롯, 히트맵, 다중
```
colors = ['색깔', ..., '색깔']
```
+ ### 색깔
  ``r``: 빨강, ``b``:파랑, ``g``: 초록, ``k``: 검정, ``w``: 하양, ``y``: 노랑, ...

+ ### 마커
    ``o``: 원, ``x``: 엑스, ``^``: 삼각형, ...

---
## 산점도
두 변수의 관계를 점으로 표현
```
plt.scatter(
    테이블_변수['속성1'], 테이블_변수['속성2']    # x축, y축
    , alpha = 1          # 투명도(0~1)
#   , s = 마커 크기                       
#   , colors = '색깔'    # 색깔(단색)
#   , c = colors        # 색깔(다색)
#   , cmap = '컬러맵'     
    )

plt.xlabel('속성1')    # x축 이름
plt.ylabel('속성2')    # y축 이름
plt.show()
```
+ ### 컬러맵
  ```
  https://wikidocs.net/141538
  ```

## 선
```
plt.plot( 
    테이블_변수['속성1'], 테이블_변수['속성2']
    
    , label = '범례'
    , '색깔+마커+선'    
    )
    
plt.show()
```

+ ### 종류
    ``-``: 실선, ``--``: 점선, ...

+ ### 적분
  >x축
  >```angular2html
  >plt.fill_between( 
  >    테이블_변수1[인덱스n:인덱스m]     # x축 범위(n~m)
  >    , 테이블_변수2[인덱스m:인덱스n]   # y축 범위(m~n)
  >
  >#   , color = '색깔'   # 색깔
  >#   , alpha = 투명도   # 투명도
  >    )
  >```
  >y축
  >```angular2html
  >plt.fill_betweenx( 
  >    테이블_변수2[인덱스m:인덱스n]     # y축 범위(m~n) 
  >    , 테이블_변수1[인덱스n:인덱스m]   # x축 범위(n~m)
  >
  >#   , color = '색깔'   # 색깔
  >#   , alpha = 투명도   # 투명도
  >    )
  >```
  >다각형
  >```angular2html
  >plt.fill(
  >    [값1, ..., 값n], [값a, ..., 값z]    # 가로: 값1~값n, 세로: 값a~값z
  >#   , color = '색깔'   # 색깔
  >#   , alpha = 투명도   # 투명도
  >    )
  >```

## 막대
``` 
plt.bar(                          # 수직(수평: barh)
    테이블_변수['속성1'], 테이블_변수['속성2']
    , width/height = 너비/높이     # 너비
    , color = color               # 색깔
    , linewidth = 두께            # 테두리 두께
    , edgecolor = '색깔'          # 테두리 색깔
    )

plt.show()
```

## 히스토그램
도수분포표 그래프
```
plt.hist( 
    테이블_변수['속성']
    , bins = 구간 수         # 구간 수
    , cumulative = True     # 누적 히스토그램
    )
    
plt.show()
```

## 파이
범주형 비율을 원형으로 표현
```
explode = [ 값1, ..., 값n ]

plt.pie( 
    테이블_변수['속성1']             # 비율
    , labels=테이블_변수['속성2']    # 이름
    , autopct='숫자 형식'   # 숫자 형식
    , startangle='각도'    # 시작 각도(-360 ~ 360)
    , c=colors             # 색깔
    , explode=explode      # 중심-그래프 간격
    , shadow=True          # 그림자
    , wedgeprops=스타일     # 부채꼴 스타일
    )
    
plt.tight_layout()
```
+ ### 스타일
  ```
  {'width': 반지름 비율(0~1), 
  'edgecolor': '테두리 색상', 
  'linewidth': 테두리 선 너비}
  ```


## 박스 플롯
최대/최소(끝), 사분위 수(상자) 
```
plt.boxplot(
    테이블_변수['속성']
    , vert=False      # 가로
    , notch=True      # 95% 신뢰구간
    )
   
plt.show()
```

## 히트맵
숫자 데이터를 색상을 이용하여 표현
```
plt.matshow()

plt.show()
```

## 다중
```angular2html
plt.subplot(행, 열, 번호)
plt.그래프()

plt.tight_layout()
```