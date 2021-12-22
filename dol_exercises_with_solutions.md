


# 100 dol exercises

This is a collection of exercises to help practicing with **dol**.


The whole project is inspired 
by the excellent  <https://github.com/rougier/numpy-100>.
File automatically generated. See the documentation to update questions/answers/hints programmatically.

#### 1. Create a store (★☆☆)


```python
from dol import Store
s = Store()
s['my_key']=12
```
#### 2. Show that a Store has strictly more attributes than a dict


```python
from dol import Store
s = Store()
s['my_key']=12
d = dict()
d['my_key']=12
assert len(set(dir(s))-(set(dir(d))))>0
assert len(set(dir(d))-(set(dir(s))))==0
```
#### 3. Get and set values for an existing key


```python
assert s['my_key']==12
# set a value
s['new_key']=[1,2,3]
assert s['new_key']==[1,2,3]
```
#### 4. Get all items of the store


```python
assert list(s.items())==[('my_key', 12), ('other_key', 'abcde'), ('new_key', [1, 2, 3])]
```
