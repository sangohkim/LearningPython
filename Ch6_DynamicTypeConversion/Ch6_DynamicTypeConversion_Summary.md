# Summary2. Dynamic Type Conversion
*Types of variables are converted dynamically by changing references.*
### Variables, Objects, References
The process of allocation in Python
1. Making objects
2. Make variables
3. **Link(Reference)** the objects and variables  
    * *Reference* is made by pointer in C
    * **Change of a variable means the change of linkage.**
        <pre><code>a = 4
      a = 'spam'</code></pre>
* Variable: an item of system tables to provide memories for linkage of objects and variables.
* Object: memory allocated enough to express the value what itself means
* Reference: pointer that link variables and objects automatically
    + *Type* is decided by the objects which variables are linked.
    * If there're no references at an object, the memory will be returned by garbage collector.
### Shared Reference
> If the objects what variables references is immutable, this does not matter. In this section, I wrote cases except it.
<pre><code>L1 = [2, 3, 4]
L2 = L1
L1[0] = 3</code></pre>
The script above doesn't act like its intention. To elaborate, L2 will be changed as well.  
Like this, Shared Reference could make errors in our script, when variables reference mutable objects.  
To prevent it,  
<pre><code>L1 = [2, 3, 4]
L2 = L1[:]
import copy
L3 = copy.copy(L1)
L4 = copy.deepcopy(L1)
'''
deepcopy vs copy ?
If we just copy, it just changes the surface but nested references are the same.
However, if we deepcopy, it copies the surface as well as the nested references.

L1 = [1, [1, 2, 3]]
import copy
L2 = copy.copy(L1)
L3 = copy.deepcopy(L1)
L1[1].append(4) # L2 = [1, [1, 2, 3, 4]], L3 = [1, [1, 2, 3]]
'''
</code></pre>
### Shared Reference and Comparation
1. '=='
This only checks the values are same.
<pre><code>a = 3
b = 3
a == b  # True
c = [1, 2]
d = [1, 2]
c == d  # False
</code></pre>
2. 'is'
This checks whether the references are same.
<pre><code>a is b  # True
c is b  # False</code></pre>

### Question
1. When different variables reference same immutable objects, are their references same?