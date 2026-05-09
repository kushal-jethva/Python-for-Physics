This is where actual coding start where we can build small system to do something.
Control Flow consists of :
- if-eilf-else
- for loop
- while loop

## if-elif-else
---
to run specific code block when some condition is met we use if-elif-else. 

```python
if condition1:
	then do this
elif condition2:
	then do this
elif condition3:
	then do this
...
else:
	if nothing satisfies than do this
```

we use `if condition:` to start the block and then write the code after an indentation (tab space), it defines that the code block belongs to the if statment and will only be ran if conditon met.

```python
if 1<5:
	print('1 is less than 5')
else:
	print('1 is not less than 5')
```

Condition must be a boolean value. Other values are also accepted
Python treats empty values as False.

```python
a='123' #True
print(if a)

a=1 #True
print(if a)

a=[1,2,3] #True
print(if a)

a=0 #False
print(if a)

a='' #False
print(if a)

a=[] #False
print(if a)
```

This is useful if you want to check if some variable like list is empty or not.

```python
a=[]

if a:
	a.append(1)
	print(a)
else:
	print('a is empty')
```

### Many Conditions
---
If you have multiple conditions we use `elif` (else-if) to include other conditions

```python
a=1

if type(a)==int:
	print('a is an integer')
	
elif type(a)==float:
	print('a is float')
	
elif type(a)==complex:
	print('a is complex')
	
else:
	print('a is of some other data type')
```

### Examples
---
```python
speed=100 #m/s
speed_limit = 70 #m/s

if speed>speed_limit:
	print('you are exceeding speed limit')
	
else:
	print('you are below speed limit')
```

```python
speed= 25 #km/hr
distance= 20 #km
target_time= 1 #hr 

current_time = distance/speed
speed_needed = distance/target_time

if current_time > target_time:
	print('you are', current_time-target_time , 'hr behind.')
	print('increase your speed by', speed_needed-speed,'km/hr')
elif current_time<target_time:
	print('you are', target_time-current_time , 'hr ahead.')
	print('decrease your speed by', speed-speed_needed,'km/hr')
	
elif current_time==target_time:
	print('you are perfectly fine')

'''
else:
	print('you are perfectly fine')
	

else can be used as this was the only condition left
else is used when no more condition left or no condition matched
or can be used when a single condition is left
'''
```

```python
a=2

if a%2==0:
	print('a is even')
else:
	print('a is odd')
```

More cleaner way is-

```python
a=2

print('a is even' if a%2==0 else 'a is odd')

#OR

if a%2==0: print('a is even')
else: print('a is odd')
```


## Loops
---
There are two main type of loops in python `for` and `while` loops.
`for` loop is used for specific range/values.
`while` loop is used for specific condition matched.

### for loop
---
![[for loop.canvas]]
>`NOTE`:
> - range(start,stop,skip)
> - range function takes integer start stop and skip values
> - it creates a sequence from start point to stop point(excluded) and skips no. in between (default is 1)
> - [start,stop)

```python
for i in range(0,5):
	print(i)
```

`for i in range` its function is just as its read , for variable named i in range , then in performs logic block and i values are changed each time block is completed.
![[for loop 2.canvas]]

we can give any variable name as we like-

```python
for _ in range(10,0,-1):
	print(_)
	
for even in range(0,20,2):
	print(even)
```

### Examples
---
```python
# Table of 13

for i in range(1,11): #1 to 10
	print('13 times',i,'=',13*i)
```

```python
# Nested loops

for i in range(1,7): # 1 to 6
	for j in range(i): # 0 to i-1
		print('*'*j)
```

```python
a = ['kushal','himesh','jay','harsh']

# using list
for names in a:
	print(names)
```

```python

time = [1,2,3,4,5,6,7,8]
v = [10] # initial speed m/s
a = 2 #m/s2

for t in time:
	# final speed = u + at
	speed = v[-1] + a*t
	
	# v[-1] give the last speed
	
	v.append(speed)
print(v)
```

zip() is a special function that takes 2  or more iterables (list or tuple) of same length and give one element from both at same time.

```python
# using zip
a=[1,2,3,4,5]
b=[2,4,6,8,10]
c=[]
for x,y in zip(a,b):
	print(x,y)
	c.append(x*y)

print()
print()

for x,y,z in zip(a,b,c):
	print(x,y,z)

```

enumerate(list/tuple) is a function that gives index,value from the list/tuple

```python
a=[10,20,30,40,50]

for index,value in enumerate(a):
	print(index,value)
```

### NOTE
---

|  Function   | Input           | Ouput                                        |
| :---------: | --------------- | -------------------------------------------- |
|   range()   | start,stop,skip | sequence of [start,stop) skipping skip value |
|    zip()    | list,tuple,...  | gives tuple of each value at same index      |
| enumerate() | list,tuple      | gives index,value pair from iterable         |
### range
---
> - takes integer values
> - sequence is [start,stop) skipping skip value
> - default start 0 , default skip 1

### zip
---
> - takes multiple iterables 
> - gives values from each iterables simultaneously

### enumerate
---
> - takes iterable
> - gives index,value pair


## while loop
---

unlike `for loop`, `while loop` runs till a condition is satisfied

![[while loop.canvas]]
```python
a=1
while a<=10:
	a+=1
	print(a)
```

while loop is used when you care about if condition is match and dont know how many time the loop will run, for loop need specific length over which it will loops, and while loop require condition and will loop till the condition is matched

## Example
---
```python
a=10
while True: # will run forever
	a-=1
	print(a)
	if a==0:
		break # explicitly breaking the loop
```

```python
a = 5
factorial = 1

while a!=1: # will break when a==1
	factorial*=a 
	a-=1 # reducing a
	
print(factorial)
```

Let us solve a problem:
*  a ball at height 5 m is thrown upwards with 10m/s speed. Find total time it will take to reach the ground.

```python
u = 10 #m/s
h = 5 # m initial height
dt = 1e-3 # 1 x 10^-3
g = -9.8 #m/s2
T = 0
while h>0:
	# height travelled
	h += u*dt + 0.5*g*dt**2
	# update velocity
	u += g*dt 
	T += dt # total time
	print(h)
	
T-=dt # last negative height dt
print(T)
```



