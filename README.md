# Multiple server with infinite capacity - (M/M/c):(oo/FIFO)
## Aim :
To find (a) average number of materials in the system (b) average number of materials in the conveyor (c) waiting time of each material in the system (d) waiting time of each material in the conveyor, if the arrival  of materials follow poisson process with the mean interval time 10 seconds, serivice time of two lathe machine follow exponential distribution with mean serice time 1 second and average service time of robot is 7seconds.

## Software required :
Visual components and Python

## Theory:
Queuing are the most frequently encountered problems in everyday life. For example, queue at a cafeteria, library, bank, etc. Common to all of these cases are the arrivals of objects requiring service and the attendant delays when the service mechanism is busy. Waiting lines cannot be eliminated completely, but suitable techniques can be used to reduce the waiting time of an object in the system. A long waiting line may result in loss of customers to an organization. Waiting time can be reduced by providing additional service facilities, but it may result in an increase in the idle time of the service mechanism.

![image](https://user-images.githubusercontent.com/103921593/203238035-1c8109bc-cbf2-4c77-baea-c5b682a752ef.png)

## Procedure :

![image](https://user-images.githubusercontent.com/103921593/203238265-176740b0-eae2-4772-90be-5449869ac9b0.png)




## Experiment:
<img width="893" height="547" alt="image" src="https://github.com/user-attachments/assets/c643cb3d-f413-47f1-8a6f-a9285c53d044" />



## Program:
```
importmath
arr_time=float(input("Enterthe meaninterarrival timeof objects fromFeeder(insecs):"))
ser_time=float(input("Enterthe mean interservicetimeof LatheMachine(insecs): "))
Robot_time=float(input("EntertheAdditional timetakenfor theRobot(insecs): "))
c=int(input("Numberof servicecentre: "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("MultipleServerwithInfinite Capacity-(M/M/c):(oo/FIFO)")
print("--------------------------------------------------------------")
print("Themeanarrival rateper second: %0.2f"%lam)
print("Themeanservice rateper second: %0.2f"%mu)
rho=lam/(c*mu)
sum=(lam/mu)**c*(1/(1-rho))/math.factorial(c)
fori inrange(0,c):
sum=sum+(lam/mu)**i/math.factorial(i)
P0=1/sum
if(rho<1):
Lq=(P0/math.factorial(c))*(1/c)*(lam/mu)**(c+1)/(1-rho)**2
Ls=Lq+lam/mu
Ws=Ls/lam
Wq=Lq/lam
print("Averagenumberofobjects inthe system :%0.2f"%Ls)
print("Averagenumberofobjects inthe conveyor: %0.2f"%Lq)
print("Averagewaiting timeofan object inthesystem: %0.2f secs"%Ws)
print("Averagewaiting timeofan object intheconveyor :%0.2fsecs"%Wq)
print("Probability thatthe system isbusy: %0.2f"%(rho))
print("Probability thatthe system isempty: %0.2f"%(1-rho))
else:
print("Warning!ObjectsOver flowwillhappenintheconveyor")
print("--------------------------------------------------------------")
```


## Output :
<img width="734" height="403" alt="image" src="https://github.com/user-attachments/assets/8aa7dfa2-8735-4eb2-b2f6-6c59c6b1b781" />



## Result : 
Thus, the program has been executed successfully and the required parameters have been calculated as per the given
conditions

