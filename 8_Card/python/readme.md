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
