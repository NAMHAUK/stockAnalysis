# StockAnalysis

주식 데이터를 분석하여 고안한 총 6개의 매매 전략에 대해 승률과 기대수익률을 계산하였습니다. 각 전략은 다음과 같습니다.
## 1. 공매도가 셀트리온에 미치는 영향 분석
2017년부터 2022년 7월 14일까지 셀트리온의 종가와 일별 공매도 거래대금, 공매도 잔고, 시가 총액 대비 공매도 잔고의 비중 사이의 관계를 분석하였습니다  

## 2. 공모주, 기관경쟁률 1000:1 이상 공모주 청약, 1) 상장 첫날 시가에 매도,2) 상장 첫날 종가에 매도 시 각각의 확률과 평균 수익률 비교

**대상**  

1) 모든 신규 공모주 (2012.7. 14 ~ 2022. 7. 14, 20년)  

2) 기관 경쟁률 1000 : 1 이상인 신규 공모주(2012. 7. 14 ~ 2022. 7. 14, 10년)  

**매수, 매도 시기**  

1) 상장 첫날 시가 매도  
2) 상장 첫날 종가 매도  
3) 상장 일주일 이후 종가 매도  
4) 상장 한달 이후 종가 매도  

**분석**  

1) 각 경우에 대해서 수익이 날 확률  

2) 수익에 대한 평균 수익률, 손해에 대한 평균 수익률  
## 3.  연말 대주주 기준일 전일 종가 매수, 대주주 기준일 다음 날 1) 시가 매도, 2) 종가 매도
**대상**  
1) KOSPI 200 ETF(2001년 말  ~ 2021년  말)  

2) KOSDAQ 150 ETF(2001년 말  ~ 2021년 말)  

3) 삼성전자(2001년 말  ~ 2021년 말)  

4) 셀트리온(2011년 말  ~ 2021년 말)  

5) 카카오(2011년 말  ~ 2021년 말)  

6) 네이버(2011년 말  ~ 2021년 말)  



**매수, 매도 시기**  

1) 대주주 기준일 종가 매수, 다음날 시가 매도  

2) 대주주 기준일 종가 매수, 다음날 종가 매도  

**분석**  

1) 각 경우에 대해서 수익이 날 확률  

2) 수익에 대한 평균 수익률, 손해에 대한 평균 수익률  

## 4. 하락장 삼성전자 금융투자 수급 매매
금융투자는 짧게 매매하는 경향성을 보인다. 따라서 하락장에서 금융투자의 강한 수급에 올라타 짧게 매매하는 전략을 고안하였다. 하락장은 고점 대비 25% 이상 하락한 3개월 이상의 기간을 기준으로 선정하였다.

## 5. 고배당주 배당락전일 / 배당락일 매매 전략

### 1) 배당락전일 현물 매수 전략

공매도를 위해 대주 거래를 한 경우, 주식의 본 소유자에게 배당금을 지급하여야 한다. 때문에 배당일이 다가오면 공매도 물량을 청산하기 위해 숏커버링 물량이 들어올 가능성이 있다. 또한, 배당락전일은 배당 이익을 취하기 위한 매수세가 분명하다. 따라서, 배당락전일 현물을 매수하는 전략을 고안하고 검증하였다.

### 2) 배당락일 공매도 전략
고배당주의 경우, 단순 배당 이익만을 취하기 위해 배당락전일 들어온 매수 수급이 배당락일 매도할 가능성이 높다. 이로 인해 배당락이 발생하는데, 배당락이 발생하면 매도세가 강할 확률이 높다. 따라서, 배당락일 공매도 숏을 진입하는 전략을 고안하고 검증하였다.


## 6. 장에 따른 요일별 시가매수 종가매도 기대수익률 분석

각 장의 성격별 기간
#### 하락장
#### - 2002-07-15 ~ 2003-04-28
#### - 2007-11-01 ~ 2008-11-21
#### - 2018-02-01 ~ 2020-04-02
#### - 2021-08-05 ~ 2022-07-15 
#### 평타장
#### - 2006-04-20 ~ 2007-02-02
#### - 2011-05-03 ~ 2017-01-11
#### 상승장
#### - 2003-04-28 ~ 2006-04-20 
#### - 2007-02-02 ~ 2007-11-01 
#### - 2008-11-21 ~ 2011-05-03
#### - 2017-01-11 ~ 2018-02-01
#### - 2020-04-02 ~ 2021-08-05 

KOSPI (2002-07-15 ~ 2022-07-15)의 data를 위와같이 하락장,평타장,상승장으로 구분하였습니다.
그 후 각 요일별로 시가,종가 차이를 저장하여 이 차이가 양수면 승리, 음수면 패배라고 가정하였습니다.
승률,수익률, 패율, 손실률을 얻어서 matplotlib을 이용하여 승률,패율은 꺾은선 그래프로, 수익률,손실률은 막대그래프로 다음과 같이 나타내었습니다.
최종적으로 승률*수익률 + 패율*손실률을 계산하여 기대수익률을 구하였습니다.





#### 개발팀원
  + 한양대 컴퓨터소프트웨어학부 남하욱
  + DGIST 기초학부 박병현
  + KAIST 전산학부 안태찬
  
