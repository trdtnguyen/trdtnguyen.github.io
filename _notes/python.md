---
title: "Python Note"
collection: notes
---

A simple note for python programming

[Nutshell](#nutshell) | [Print](#print) | [Array](#array)

# Nutshell
### Install:

`$ sudo apt-get install python-pip -y`

### Check location of a package
`$ sudo pip3 show <package_name>`

### To set a python version as default:
* To check the current python version:

Python 2.*
`$ python --version`

Python 3
`$ python3 --version`

The simple safe way is use alias. Add into your `~/.bashrc` or `~/.bash_aliases`

`alias python=python3`

# Print

# String
```python
a = "Bubu"
b = "is a fat pet"
c = a + " " + b # output: "bubu is a fat pet"
```
* Convert a type to string using `str()` function
```python
a = tem
b = 1
c = a + b #Error
c = a + str(b) # c = "tem1"
```
# Array
* Array in Python is implement as a list data structure
* Elements in an array could be in various type
```python
a = [1, 2.3, "girl", 2+0j]
```
* Two lists could be concat using `+`
* `len(array)`: return length of the array

# Loop

A common loop syntax in C/C++ is:
```C
for (i = 0; i < n; i++){
  loop body
}
```
In Python, the loop becomes:
```python
for i in range(0, n):
<tab> loop body
```
Note the colon `:` is required at the end of the loop statement

A better alternative (although longer) way is using while loop. It's better because you can easily control the iterator variable with while loop.
```python
count = 0
while True:
  print(count)
  count += 1
  if count >= 10:
    break
```
