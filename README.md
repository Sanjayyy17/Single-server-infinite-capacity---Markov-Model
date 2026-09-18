# Single server with infinite capacity (M/M/1):(oo/FIFO)
![image](1.png)

This is a queuing model in which the arrival is Marcovian and departure distribution is also Marcovian,number of server is one and size of the queue is also Marcovian,no.of server is one and size of the queue is infinite and service discipline is 1st come 1st serve(FCFS) and the calling source is also finite.

## Procedure :

![imAGE](2.png)



## Experiment:


 
## Program
```
arr_time = float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time = float(input("Enter the mean inter service time of Lathe Machine (in secs): "))
Robot_time = float(input("Enter the Additional time taken for the Robot (in secs): "))

lam = 1 / arr_time
mu = 1 / (ser_time + Robot_time)

print("------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(00/FIFO)")
print("------------------------------------------------------------")

print("The mean arrival rate per second : %0.2f" % lam)
print("The mean service rate per second : %0.2f" % mu)

if (lam < mu):
    Ls = lam / (mu - lam)
    Lq = Ls - lam / mu
    Ws = Ls / lam
    Wq = Lq / lam

    print("Average number of objects in the system : %0.2f" % Ls)
    print("Average number of objects in the conveyor : %0.2f" % Lq)
    print("Average waiting time of an object in the system : %0.2f secs" % Ws)
    print("Average waiting time of an object in the conveyor : %0.2f secs" % Wq)
    print("Probability that the system is busy : %0.2f" % (lam / mu))
    print("Probability that the system is empty : %0.2f" % (1 - lam / mu))

else:
    print("Warning! Objects Over flow will happen in the conveyor")

print("------------------------------------------------------------")
```

## Output :
<img width="1124" height="654" alt="image" src="https://github.com/user-attachments/assets/c8b94a78-fce6-4dcc-86ce-bd38cd497065" />

## Result :
Thus, the M/M/1 queueing model with infinite capacity is analyzed, and the mean arrival rate, mean service rate, average number of objects, average waiting time, and the probabilities of the system being busy and empty are calculated.
