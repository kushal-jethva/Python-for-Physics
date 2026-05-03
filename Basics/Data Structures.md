
Data structure is a way of organizing and storing data so that it can be accessed and modified efficiently.

In Python there are mainly 4 data structures that we are going to learn, However you can create your own data structure using them.
* Lists
* Dictionary
* Tuples
* Sets

## Lists
---
Think of a list as a container that stores multiple values in order.

```python
# Lists
a=[1,2,3,4,5] # syntax to create list
```

To create a list simply add data separate by comma in a square brackets


### List Manipulation
---
Accessing data stored in list
Just like matrices, we use indexes to access values stored in lists.

```python

a=[1 , 2 , 3 , 4 , 'name' , 1+2j , 1.02 , True] 
#Lists can store multiple data types together.
print(a[0]) 

#Format to access data
# list[index]
```

Index in list starts with 0 from left and also -1 from right.

```python
a    =     [ 1 , 2 , 3 , 4 , 5 ]
#index       0   1   2   3   4
#also       -5  -4  -3  -2  -1
```

Negative indexing is used if you don't know length of list and want to access data from last.

### Slicing
---
To access subset of list we use list slicing.

```python

# Format: list[start:stop:skip]
# NOTE: stop index is excluded


a=[1,2,3,4,5]
print(a[0:2]) # output: [1,2]

# by default skip = 1

print(a[:3]) #output:  [1,2,3]
print(a[2:]) #output:  [3,4,5]
print(a[::2]) #output: [1,3,5]
```

| Format     | Output                                 |
| ---------- | -------------------------------------- |
| `[:]`      | all values                             |
| `[::2]`    | every second value                     |
| `[::-1]`   | Reversing List                         |
| `[2:3]`    | value at 2 index (we skip end index 3) |
| `[4:1:-1]` | values from 4 to 2 in reverse order    |
### Adding Data points
---
```python
a=[3,4,5,6]

a.append(4) # will add 4 at the end of the list

a.extend([2,3,4]) # will extend the list and add this points at last

a.insert(0,2) # insert value 2 at 0th index
```

Formats:
* list.append(data)
* list.extend(list)
* list.insert(index,data)

### Other Methods
---

```python
a=[1,2,3,4,5]

a.pop(2) # deletes value at index 2
print(a) # [1,2,4,5]

a.remove(4) # removes the value provided
print(a)    # [1,2,5]

print(len(a)) # gives the length of list
# output: 3

a.clear() # delets all item in list
del a     # delets variable a from memory

#clear() removes all items from the list, while del removes the variable itself
```

```python
b=[1,2,2,5,2,3]

print(b.count(2)) # gives no. of value occurence in list


b.sort() # sorts the list acsending oreder (in-place)
print(b) 

#in-place means it will change the value of variable

# sorted(list) gives new sorted list instead of changing in-place

b.reverse() # same as b[::-1] but in-place 
print(b)

print(b.index(5)) # gives the index of the value 5

a=b.copy() # copies b into a

```

```python
#changing values

a=[1,2,3,4,5]
a[0]=3  # cahnges value at index 0 to 3
print(a) #output: [3,2,3,4,5]
```

```python
# nested list

a  =         [ [ 1 , 2 ] , [ 3 , 4 ] ]
#inner index     0   1       0   1 
#outer index       0           1  

# equivalent to matrix
#   [ 1    2 ]
#   [ 3    4 ]

print(a[0][0])   #a[0] calling first index value ; [1,2]
                 #a[0][0] calling fisrt index of
                 #first index value; 1 
```

### More functions
---

```python

a=[1,2,3,4,5,6,7]


print(sum(a)) # gives sum of all the value
print(max(a)) # gives maximum value present in a
print(min(a)) # gives minimum value present in a

```

```python

a=2
c=7
b=[1,2,3,4,5]

print(c in b)
print(a in b) # gives boolean value
# it checks if a is present in b
```

```python

a=[1,2,3,4]
b=[6,7]

c=a+b  # creted new combined list (union)
print(c)
```

```python

a=[1]

print(a*4) # gives [1,1,1,1]
# The list is repeated 4 times
```

# NOTE
---
> Remember Functions   function_name(input)->output

* sum(list)
* max(list)
* min(list)
* len(list)
* list.append(value)
* list.extend(list)
* list.insert(index,value)
* list.pop(index)
* list.remove(value)
* list.sort()
* list.reverse()
* list.copy()
* list.clear()


# Dictionary
---
In list we store value by position(index) but in Dictionary we store values by labels to better keep track of different data represented.

```python

data={ 'name':'VED' , 'class':6 , 'age':11 }

#here name class age are labels, called keys in python
#and VED 6 11 are called values

BMI_data={'height':180,'weight':75}

# list inside dictionary
student_data={
			  'students':['Hitaksh','Ved','Aditya'] ,
			  'marks': [88,90,99]
			  }

matrix={ 0: [1,2],
		 1: [3,4] }
```

To create a dictionary remember the format
inside curly bracket key and value separated by colon

```python
a = { key1 : value1 , key2 : value2 ...}
```

keys should not be duplicate, it will cause error while accessing the values.
Dictionary keys do not have to be strings. Numbers can also be used as keys.

Or you can use dict() constructor

```python
values=dict(name='ved', age=11 , gender='male')
```

## Accessing values
---
In list we use index to get values but here we use keys to get corresponding values.

```python
a={1:0 , 2:3}
print(a[1])
print(a[2])

BMI_data={'height':180,'weight':75}

print(BMI_data['height'])
print(BMI_data['weight'])
```

adding values

```python
a={ 0:0 , 1:1 , 2:2 }
a[3]=3  #FORMAT: dictionary[key]=value
a[4]=4

print(a)
```

Updating values

```python
a={ 0:1 , 1:1 , 3:3 }
print(a)
a[0]=0
print(a)
```

To update multiple values at same time we can use

```python
a={ 0:1 , 1:1 , 3:3 }
a.update({0:0,1:2,3:2})
print(a)
```

### Other functions
---
```python
a={0:0,1:1,2:2,'name':'jiya','marks':[20,10,30]}

print(a.keys()) # returns all the keys
print(a.values()) # returns all the values
print(a.items()) # return key value pair in tuple format
```

## Tuple
---
It is same as list except it is immutable i.e. its values cannot be changed once created. Think of representing x and y coordinate but you don't want to change them further in the code.

```python
x_y = (30,40)
```
created using round brackets and values are separated by commas.

we can access values using indexes same as list.
```python
xyz=(30,40,50)

x=xyz[0]
y=xyz[1]
z=xyz[2]
print(x,y,z)

# you can also define
x,y,z = xyz #this will broadcast values to variables                accorrding to the index

print(x,y,z)
```
We have only 2 methods for tuples

```python

name=('ved','hitaksh','himesh','issac')
print(name.count('himesh')) # counts occurence of himesh
print(name.index('himesh')) # returns index of himesh
```


## Set
---
Same as sets in maths, it does not allows duplicate values, not in ordered format and immutable (values cannot be altered).

```python
values={0,1,2,3,4,'name',True,0.001}
```

simply use curly brackets to define a set


### Operations on set
---

```python 
data1={0,1,2,3,4,5}
data2={6,7,8,9,0,1,2,3}

union = data1 | data2
intersection = data1 & data2

differenc = data1 - data2 
#values in data1 but not in data2

symmetric_diff = data1 ^ data2
#values in data1 or data2 but not in both
```

```python
data={0,1,2,3,4}

data.add(5) #add value
data.update({6,7,8}) #add multiple values
data.remove(0) #removes value 0, if not present raise error
data.discard(1) #remove value 1, if not present does not raise error

data.clear() #removes all values
```