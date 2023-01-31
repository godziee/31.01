# 31.01

from random import *


#1

index=""
maakonnad=["Tln","Narva","K-Järve","Ida-Virumaa","Tartu","Tartumaa","Viljandi","Pärnumaa","Saaremaa"]
while True:
    try:
        index=int(input("Anna index: "))
        if index<99999 and index>10000:
            break
    except:
        print("Anna õige index!")
i=index//10000 #1,2,3,4,5,6,7,8,9
print(f"{index} on {maakonnad[i-1]}") #0,1,2,3,4,5,6,7,8
if i in [1,2,3]: 
    print("Jääta koju!")
else:
    print("Kanna maski!")


    
#2

number=[]
osa1=[]
osa2=[]
print("")
for i in range(20):
    number.append(randint(1,20))
if len(number)%2==0 and len(number)>=2:
    n=int(len(number)/2)
    for i in range(1,n+1): #1, ....n
        osa1.append(number[i-1])
    for j in range(n+1, len(number)+1): #n+1,.....len()
        osa2.append(number[j-1])
    osa1.reverse()
    osa2.reverse()
    osa2.extend(osa1)
    print(osa2)
else:
    print("Viga!")



#3 

arv=[]
kogus=int(input("Kogus: "))
for i in range (kogus):
    arv.append(randint(-100,100))
print(arv)
max_arv=max(arv)
ind=arv.index(max_arv)
print("позиция",ind)
print("число",max_arv)
max_arv=round(max_arv/kogus,2)
arv.insert(ind,max_arv)
arv.pop(ind+1)
print(arv)
