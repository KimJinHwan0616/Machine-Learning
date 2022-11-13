# Seaborn
Matplotlib 업그레이드(색상)
```angular2html
import seaborn as sns

(리스트)변수1 = [값1, ..., 값n]
(리스트)변수2 = [값1, ..., 값n]
```

## 막대그래프
항목별 갯수
```
sns.countplot(
    data=(테이블)변수
    x/y = '속성'          # x/y축 - 세로/가로
    hue = '속성'          # 범례
    [, palette='종류']    # 팔레트 종류
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
