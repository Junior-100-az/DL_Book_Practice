# DL_Book_Practice

#Series()

import pandas as pd

#test_sr = [[100, 99, 95], index = ["신기쥬니어", "코피퐝", "브베옥슬"]]    #시리즈는 판다스에 있는거라 판다스 객체에 시리즈 메서드를 갖다써야함. ()도 잊지말고. 

test_sr = pd.Series([100, 99, 95], index = ["신기쥬니어", "코피퐝", "브베옥슬"])

print(test_sr)

print(f"인덱스 값:{test_sr.index}")
print(f"밸류 값:{test_sr.values}")

#_______________________________________________________________________________________________________
#DataFrame()

stats_num = [[70, 60, 90], [90, 70, 10], [70, 90, 50]]
stats = ["힘", "민첩", "지능"]
races = ["blood elf", "orc", "goblin"]

df = pd.DataFrame(stats_num, columns = stats, index = races)   #저 클래스의 역할을 대행해주는 객체 df. 
print(df)
print()
print(f"컬럼:{df.columns}")    #이거도 시리즈랑 비슷하게 가면 된다. 이 객체가 컬럼을 불러오는거다.
print(f"인덱스:{df.index}")    
print(f"값:\n{df.values}")                                #값은 밸류로 접근하면 된다.

#________________________________________________________________________________________________________

#Generating DataFrame

#리스트. 뭔가 싹 펼쳐두고 설명을 추가하는 느낌?
mate_data = [[95, "Castigation", "28.86 %"],
             [83, "Pallux", "21.44 %"],
             [52, "Manute", "16.95 %"]
             ]  

df = pd.DataFrame(mate_data, columns = ["Parse %", "Name", "Amount"], index= [1, 2, 3])
print(f"데이터 프레임 값:{df.values}")
print(f"데이터 프레임 컬럼:{df.columns}")
print(f"데이터 프레임 인덱스: {df.columns}")
print(f"토탈\n:{df}")
                                           #로그 사이트 따라 만들기 꽤 색다른 경험인데? 내가 만드는거잖아 ㅋㅋㅋ

#딕셔너리. 각각의 컬럼이 키값이 되고, 덩어리를 퉁퉁 만드는 감성?
#키는 리스트 형태로 넣을 수도 있다.

mate_data2 = { "Parse %" : [95, 83, 52],
              "Name" : ["Castigation", "Pallux", "Manute"],
               "Amount" : ["28.86 %", "21.44 %", "16.95 %"]
}

df = pd.DataFrame(mate_data2, index = [1, 2, 3])



print(df.head(2))
print()
print(df.tail(2))
print()
print(df["Name"])  #불규칙.이건 리스트 인덱싱 감성. (해당 컬럼 가져오기) 주의: 문자열 형식임.
print()
print(df["Parse %"])
print()
print(df["Amount"])


















             

