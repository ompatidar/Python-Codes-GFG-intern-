import json
import time
s=open("Record.json",'r')
dc=s.read()
s.close()
d=json.loads(dc)
for i in d:
    print(i,d[i])
usr=input("Enter your name ")
usm=input("enter mail id")
umo=int(input("mobile no"))
ui=str(int(input("Id:")))
qn=int(input("Quantity:"))
if(qn<=d[ui]["qn"]):
    print("Name:",d[ui]["Name"])
    print("Price:",d[ui]["price"])
    print("_"*20)
    print("Total:",d[ui]["price"]*qn)
    d[ui]["qn"]=d[ui]["qn"]-qn
    txn = usr+","+usm+","+str(umo)+"\n"+d[ui]['Name']+","+str(d[ui]['price'])+time.ctime()+"\n"
else:
    print("_"*20)
    print("Sorry qn you want not in the stock")
    print("We have only:",d[ui]["qn"])
    yn=input("If still you want to buy qm we have then press Y:")
    if(yn=="Y" or yn=="y"): 
        print("Name:",d[ui]["Name"])
        print("Price:",d[ui]["price"])
        print("_"*20)
        print("Total:",d[ui]["price"]*d[ui]["qn"])
        txn = usr+","+usm+","+str(umo)+"\n"+d[ui]['Name']+","+str(d[ui]['price'])+time.ctime()+"\n"
        d[ui]["qn"]=d[ui]["qn"]-d[ui]["qn"]
        print("Updated Dict")
        print("<","-"*20,">")
    else:
        print("<","-"*20,">")
        print("Thank you:-) for your valuable time")
js=json.dumps(d)
jd=open("Record.json",'w')
jd.write(js)
jd.close()
fd=open('Sales.txt','a')
fd.write(txn)
fd.close()
