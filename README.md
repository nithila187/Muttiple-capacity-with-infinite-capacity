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
<img width="889" height="549" alt="image" src="https://github.com/user-attachments/assets/24d61520-0a2a-4ea8-b3d1-fb5bc57cb6b8" />



## Program:
```
arr_time=float(input("Enterthe meaninterarrival timeof objects fromFeeder(insecs):"))
ser_time1=float(input("Enterthe mean inter servicetimeof Lathe Machine1(in secs): "))
ser_time2=float(input("Enterthe mean inter servicetimeof Lathe Machine2(in secs): "))
ser_time3=float(input("Enterthe mean inter servicetimeof Lathe Machine3(in secs): "))
Robot_time=float(input("EntertheAdditional timetakenfor theRobot(insecs): "))
lam=1/arr_time
mu1=1/(ser_time1+Robot_time)
mu2=1/(ser_time2+Robot_time)
mu3=1/(ser_time3+Robot_time)
print("-----------------------------------------------------------------------")
print("SeriesQueueswithinfinitecapacity-OpenJacksonNetwork")
print("-----------------------------------------------------------------------")
if(lam< mu1)and(lam< mu2) and(lam< mu3):
Ls1=lam/(mu1-lam)
Ls2=lam/(mu2-lam)
Ls3=lam/(mu3-lam)
Ls=Ls1+Ls2+Ls3
Lq1=Ls1-lam/mu1
Lq2=Ls2-lam/mu2
Lq3=Ls3-lam/mu3
Wq1=Lq1/lam
Wq2=Lq2/lam
Wq3=Lq3/lam
Ws=Ls/(3*lam)
print("Averagenumberofobjects inthe system S1:%0.2f"%Ls1)
print("Averagenumberofobjects inthe system S2:%0.2f"%Ls2)
print("Averagenumberofobjects inthe system S3:%0.2f"%Ls3)
print("Averagenumberofobjects inthe overallsystem : %0.2f"%Ls)
print("Averagenumberofobjects inthe conveyorS1 : %0.2f"%Lq1)
print("Averagenumberofobjects inthe conveyorS2 : %0.2f"%Lq2)
print("Averagenumberofobjects inthe conveyorS3 : %0.2f"%Lq3)
print("Averagewaiting timeofan object intheconveyor S1: %0.2fsecs"%Wq1)
print("Averagewaiting timeofan object intheconveyor S2: %0.2fsecs"%Wq2)
print("Averagewaiting timeofan object intheconveyor S3: %0.2fsecs"%Wq3)
else:
print("Warning!ObjectsOver flowwillhappenintheconveyor")
print("----------------------------------------------------------------------")
```


## Output :
<img width="669" height="394" alt="image" src="https://github.com/user-attachments/assets/e93cba3f-17a1-4042-ac39-1f38f20b8df5" />


## Result : 
Thus, the program has been executed successfully and the required parameters have been calculated as per the given
conditions

