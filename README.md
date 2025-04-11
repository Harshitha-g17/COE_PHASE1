# COE_PHASE1

#BASED ON EXAM SCORE CALCULATING TOTAL SCORE AND GRADE

project=int(input("enter project score"))
external=int(input("enter external score"))
internal=int(input("enter internal score"))
if project>=50 and external>=50 and internal>=50:
    total_score=(project*70)/100+(external*20)/100 +(internal*10)/100
    if total_score>=90:
        print("A grade")
    elif total_score>=70:
        print("b grade")
    else:
        print("c grade")
else:
    print("fail")


#GENERATING ELECTRIC BILL BASED ON UNITS

prev=int(input("enter previous value"))
pres=int(input("enter present value"))
units=prev-pres
total=0
if units<=50:
    total=50*0.50
elif units<=150:
    total=50*0.50+(unit-50)*0.75
elif units<=250:
    total=50*0.50+(100*0.75)+(unit-150)*1.25
else:
    total=50*0.50+(100*0.75)+(100*1.25)+(unit-250)*2.50

bill=total+(total*18)/100
print(bill)



#GENERATING BILL BASED ON FESTIVAL AND NON-FESTIVAL DAY OFFERS

meal_type=int(input("enter your meal type 1.veg 2.non-veg 3.combo"))
quantity=int(input("enter the quantity"))
festival=input("enter festival 1.yes 2.no")
veg=150
non_veg=200
combo=300
if(festival=='1'):
    if(meal_type==1):
        total=veg*quantity
        bill=total-(total*10)/100
    elif(meal_type==2):
        total=non_veg*quantity
        bill=total-(total*10)/100  
    else:
        total=combo*quantity
        bill=total-(total*10)/100     
else:
    if(meal_type==1):
        bill=veg*quantity
    elif(meal_type==2):
        bill=non_veg*quantity 
    else:
        bill=combo*quantity    
    
print(bill)
if(bill>=1000):
    print("add free desert")
bill=bill+(bill*5)/100
print(bill)
    
#EDUCATION – SCHLORSHIP ELIGIBILITY EVALUATOR

student_name=input()
percentage_10=int(input())
percentage_12=int(input())
percentage_ug=int(input())
family_income=int(input())
if(percentage_10>85 and percentage_12>85 and percentage_ug>85 and family_income<300000):
    print("FULL Scholarship is eligible by ",student_name)
elif( percentage_ug>70 and family_income<500000):
    print("Partial Scholarship is eligible by",student_name)
else:
    print("not eligible for scholarship")
