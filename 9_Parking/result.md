달라지는 것만 표기
# ver0(baseline)
단지(면적으로 열 추가해서) & random forest 127.0467346939

# ver1
단지(<b>평균</b>) & 자격유형 A, C 대입 & random forest 120.7916326531

# ver2
단지(평균) & random forest drop_duplicate 120.5579591837

단지(평균) & <b>svr</b> drop_duplicate 245.7002485916

# ver3
age_gender_info와 합치려고 준비

# ver4
age_gender_info 포함(1,1gender,2,2gender,3,3gender) / 평균 random forest drop_duplicate 123.2816326531	<br>
age_gender_info 포함(1,1gender,2,2gender,3,3gender&<b>나이대10으로 나눔</b>) /평균 random forest drop_duplicate <b>116.8657142857</b>
