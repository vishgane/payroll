# payroll
PAYROLL
W1={"Jan":31,"Feb":28,"Mar":31,"Apr":30,"May":31,"June":30,"July":31,"Aug":31,"Sept":30,"Oct":31,"Nov":30,"Dec":31 }
n=int(input('No of days present ='))
D=W1[input("Wage Month =")]
G=16000
print("Gross Wages =", G)
A=round((G/D)*n)
print("Actual salary =", A)

print("DEDUCTION")
if (A>=15000):
    pf=round(15000*12/100)
else:
    pf=round(A*12/100)
print("EPF employee share @ 12% =", pf)
if (A>21000):
    es=round(21000*0.75/100)
else:
    es=round(A*0.75/100)
print("ESI employee share @ 0.75% =", es)
if (A>0):
    lwf=50
else:
    lwf=0
print("LWF employee share =", lwf)
o=int(input("Other Deduction ="))
T=pf+es+lwf+o
print("Total Deduction =", T)
N=A-T
print("Net Salary =", N)

print("BILLING")
if (A>=15000):
    PF=round(15000*13/100)
else:
    PF=round(A*13/100)
print("EPF employer share @ 13% =", PF)
if (A>21000):
    ES=round(21000*3.25/100)
else:
    ES=round(A*3.25/100)
print("ESI employer share @ 3.25% =", ES)
if (A>0):
    LWF=50
else:
    LWF=0
print("LWF employer share =", LWF)

B=A+PF+ES+LWF

print("Billing amount =", B)
