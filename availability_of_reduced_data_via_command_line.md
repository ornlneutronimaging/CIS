[HOME](index.md)

# Availability of reduced data using a terminal

At the end of each experiment, the local contact needs to record the availability of the data. 

There are 2 ways to do this:

* using the command line (Preferred)
* using the browser

## Command line

1. Go to the **analysis.sns.gov** server. You can either use ThinLinc and open a terminal there, or directly from
a terminal session on your computer and type

```
ssh analysis.sns.gov
``` 

2. Start the script for your instrument

* for CG1D

```
/HFIR/CG1D/shared/CIS/confirm-cg1d
```

* for SNAP

```
/SNS/SNAP/shared/CIS/confirm-snap-imaging
```

3. Answers the questions

```
-bash-4.2$ /HFIR/CG1D/shared/CIS/confirm-cg1d

++++++++++++++++++++++++++++++++
+ CG1D reduction confirmation +
++++++++++++++++++++++++++++++++

IPTS To Confirm? ->
```

Let's use IPTS # **28918** for this example

```
IPTS To Confirm? -> 28918
```

Hit **ENTER**

```
--------------------------------
1 -> No
2 -> Yes
3 -> Partially
4 -> Unknown
5 -> None Expected
--------------------------------
Data Availability? ->
```

In our case, let's enter **3**

```
Data Availability? -> 3
```

Hit **ENTER**

```
--------------------------------
1 -> Auto Reduction
2 -> With Scripts
3 -> By CIS
--------------------------------
Reduction Type? ->
```

let's enter **2**

```
Reduction Type? -> 2
```

Hit **ENTER**

```
Submission Number? (If not sure, press [Enter]) ->
```

Just hit **ENTER**

```
Any Comments? (If no comments, press [Enter]) ->
```

Feel free to provide any feedback, such as **Reduced by IS** for example

```
Any Comments? (If no comments, press [Enter]) -> Reduced by IS
```

Hit **ENTER**

The program will give you a summary of what it is about to submit

```
++++++++++++++++++++++++++++++++++++++++
+             Info Summary             +
++++++++++++++++++++++++++++++++++++++++

Instrument        : CG1D
IPTS To Confirm   : 28918
Data Availability : Partially
Reduction Type    : With Scripts
Submission Number : 1.1
Comments          : Reduced by IS

++++++++++++++++++++++++++++++++++++++++

All look good? ([Y/y]N/n) ->
```

Hit **N** or **n** if you want to change anything, otherwise **Y** or **y**

```
Submitting IPTS confirmation to database...
usage: confirm-data [-h] [-s {Unknown,No,Yes,Partially,None Expected}]
                    [-c COMMENT]
                    instrument ipts submission-number {Auto,CIS,Scripts}
confirm-data: error: argument submission-number: invalid int value: '1.1'

Success!
```

