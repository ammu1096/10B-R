# 10B-R
#F-test- SST
x<-c(16,26,27,23,24,22)
y<-c(33,42,35,32,28,31)
#x<-c(9,11,13,11,15,9,12,14)
#y<-c(10,	12,10,14,9,8,10)
#x<-c(20,16,26,27,23,22,18,24,25,19)
#y<-c(17,23,32,25,22,24,28,16,31,33,20,27)
print("enter the level of significance")
alpha<-scan()
n1<-length(x)
n2<-length(y)
sd1<-sd(x)
sd2<-sd(y)
if (sd1>sd2) { fvalue<-sd1^2/sd2^2 
} else fvalue<-sd2^2/sd1^2
xbar<-mean(x)
ybar<-mean(y)
print("mean of x, mean of y, SD of x , SD of y")
values<-c(xbar,ybar,sd1,sd2)
print(round(values,digits=4))
print("F value using program")
print(round(fvalue,digits=4))
F<-var.test(x,y)
print("F value using built in ")
print(F)
print("Table value for two-tailed test:")
if (sd1>sd2) { ftab<-qf(1-alpha,n1-1,n2-1)
} else ftab<-qf(1-alpha,n2-1,n1-1)
print(round(ftab,digits=3))




output:


#F-test- SST
> x<-c(16,26,27,23,24,22)
> y<-c(33,42,35,32,28,31)
> #x<-c(9,11,13,11,15,9,12,14)
> #y<-c(10,	12,10,14,9,8,10)
> #x<-c(20,16,26,27,23,22,18,24,25,19)
> #y<-c(17,23,32,25,22,24,28,16,31,33,20,27)
> print("enter the level of significance")
[1] "enter the level of significance"
> alpha<-scan()
1: 3
2: 4
3: 6
4: 7
5: 8
6: 99
7: 5
8: 
Read 7 items
> n1<-length(x)
> n2<-length(y)
> sd1<-sd(x)
> sd2<-sd(y)
> if (sd1>sd2) { fvalue<-sd1^2/sd2^2 
+ } else fvalue<-sd2^2/sd1^2
> xbar<-mean(x)
> ybar<-mean(y)
> print("mean of x, mean of y, SD of x , SD of y")
[1] "mean of x, mean of y, SD of x , SD of y"
> values<-c(xbar,ybar,sd1,sd2)
> print(round(values,digits=4))
[1] 23.0000 33.5000  3.8987  4.7645
> print("F value using program")
[1] "F value using program"
> print(round(fvalue,digits=4))
[1] 1.4934
> F<-var.test(x,y)
> print("F value using built in ")
[1] "F value using built in "
> print(F)

	F test to compare two variances

data:  x and y
F = 0.6696, num df = 5, denom df = 5, p-value = 0.6706
alternative hypothesis: true ratio of variances is not equal to 1
95 percent confidence interval:
 0.09369826 4.78524246
sample estimates:
ratio of variances 
         0.6696035 

> print("Table value for two-tailed test:")
[1] "Table value for two-tailed test:"
> if (sd1>sd2) { ftab<-qf(1-alpha,n1-1,n2-1)
+ } else ftab<-qf(1-alpha,n2-1,n1-1)
Warning message:
In qf(1 - alpha, n2 - 1, n1 - 1) : NaNs produced
> print(round(ftab,digits=3))
[1] NaN NaN NaN NaN NaN NaN NaN
