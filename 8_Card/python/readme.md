## ver 2
- oversamplingSMOTE&ADASYN test<br>
adasyn:0.9275212252<br>
smote:0.9359255753<br>
-> 성능 개선 안 됌
- child num,family_size
5명 초과->6으로 하나의 클래스로 합침
-one hot encoding

## ver 3
- scaling
bellshape: standardscaler
나머지: minmaxscaler
- days birth
나이대 별로 나누기
- income total
구간 10개로 지정
- days_employed
n =500

## ver 4
- 차원축소(PCA)
- 시각화 된 것 보고 scaling 다시 생각해보기
- days_employed:n=2,500 성능 차이 확인을 위해서
n=2로 한 열을 아예추가해서 평가해보았으나 차이 없어서 n=500으로 하기로 결정

## ver 5
- scaling 한 후 모델성능 차이 확인(이민영님 시각화 참고하여 조금 방법 수정)
- 결과
1. scaling:xgboost:no pca : 0.8543297831
2. scaling:xgboost:pca(family size랑 child num) : 0.8550151303
3. scaling:xgboost:pca(family size랑 child num, work phone이랑 phone) : 	0.8551579135	
4. no scaling:xgboost : (제출예정) <br>

-> pca하면 할수록 성능 저하<br>
※기본 전처리<br>
DAYS_BIRTH:AGE로 변환<br>
GENDER, CAR, REALITY, EDU_TYPE,FAMILY_TYPE,HOUSE_TYPE,INCOME_TYPE:라벨인코딩<br>
INCOME_TOTAL:10개 구간 분할<br>
DAYS_EMPLOYED,BEGIN_MONTH:구간화<br>
CHILD_NUM,FAMILY_SIZE:6이상 모두 6으로<br>
