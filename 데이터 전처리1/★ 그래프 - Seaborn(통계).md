># Seaborn
>Matplotlib 업그레이드(색상)
>### 막대그래프,
```angular2html
import seaborn as sns
```

## 막대그래프
```
sns.barplot(
    data = (테이블)변수    # 테이블 이름
    , x = '속성'      # x축
    , y = '속성'      # y축
    , hue = '속성'    # 그룹별 속성
    )

plt.show()
```

## 히스토그램/밀도
가로: 분포, 세로: 빈도
```
sns.histplot/kdeplot( x/y='속성' )     # x/y - 세로/가로
plt.show()
```

## 박스 플롯 ㅇ
최대/최소(끝), 사분위 수(상자) 
```
sns.boxplot( x=(리스트)변수.속성 )
```
