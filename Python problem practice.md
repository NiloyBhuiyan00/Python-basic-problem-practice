```markdown
```
# Sum Items in List

```python
def sum_list(a):
    sum = 0
    for i in a:
        sum+= i
    return sum

a = [1, 4, 6, 8, 4, 7]
print(sum_list(a))
```

# Multiply Items in List
```python
def multi_list(a):
    multi = 1
    for i in a:
        multi*=i
    return multi

a=[1,4,6]
print(multi_list(a))
```

# Get Largest Number in List
```python
def max_number(a):
    maxx = a[0]
    for i in a:
        if maxx < i:
            maxx = i
    return maxx

a=[1,4,6,8,44,7,33]
print(max_number(a))
```

# Get Smallest Number in List
```python
def min_number(a):
    minn = a[0]
    for i in a:
        if i < minn:
            minn = i
    return minn

a=[4,6,8,44,7,33,1]
print(min_number(a))
```

# Count Strings with Same Start and End
```python
def count_strings(a):
    count = 0
    for i in a:
        if len(i) > 2 and i[0] == i[-1]:
            count += 1
    return count

a=['abc','xyz','aba','1221']
print(count_strings(a))
```

# Sort Tuples by Last Element
```python
def sort_tuples(v):
    for i in range(len(v)):
        for j in range(i + 1, len(v)):
            if v[i][1] > v[j][1]:
                v[j], v[i] = v[i], v[j]
    return v

v=[(2,5),(1,2),(4,4),(2,3),(2,1)]
print(sort_tuples(v))
```

# Remove Duplicates from List
```python
def remove_duplicates(a):
    v = []
    for i in a:
        if i not in v:
            v.append(i)
    return v

a=[1,2,2,3,3,4,5,6,6]
print(remove_duplicates(a))
```

# Check if List is Empty
```python
def is_empty(a):
    if len(a) == 0:
        return "empty"
    else:
        return "not empty"

a=[]
print(is_empty(a))
```

# Clone or Copy a List
```python
def clone_list(a):
    return a.copy()

a=[1,2,3,4]
print(clone_list(a))
```

# Find Words Longer Than n
```python
def find_words_longer_than(v, n):
    count = 0
    for i in v.split():
        if len(i) > n:
            count += 1
    return count

v="i love machine learning"
print(find_words_longer_than(v, 3))
```

# Check Common Member Between Two Lists
```python
def common_member(a, b):
    for i in list(set(a)):
        for j in list(set(b)):
            if i == j:
                return True
    return False

a=[1,2,5]
b=[1,2,2,5]
print(common_member(a, b))
```

# Remove Specific Elements from List
```python
def remove_specific_elements(v):
    b = []
    for i in v:
        if i == v[0] or i == v[4] or i == v[5]:
            continue
        else:
            b.append(i)
    return b

v=['Red','Green','White','Black','Pink','Yellow']
print(remove_specific_elements(v))
```

# Remove Even Numbers from List
```python
def remove_even_numbers(a):
    v = []
    for i in a:
        if i % 2 != 0:
            v.append(i)
    return v

a=[1,2,3,4,5]
print(remove_even_numbers(a))
```

# Generate Square Numbers in Range
```python
def generate_squares(n):
    m = []
    for i in range(1, n + 1):
        m.append(i**2)
    return m[6:]

n = 30
print(generate_squares(n))
```

# Generate All List Permutations
```python
import itertools

def generate_permutations(v):
    return list(itertools.permutations(v))

v = [1, 2, 3]
print(generate_permutations(v))
```

# Calculate Difference Between Lists
```python
def list_difference(list1, list2):
    return list(set(list1) - set(list2))

list1=[1,3,6,8,9]
list2=[1,3,4,8,9]
print(list_difference(list1, list2))
```

# Access List Indices
```python
def access_index(a):
    return a.index(57)

a=[1,23,5,73,67,57]
print(access_index(a))
```

# Convert List to String
```python
def convert_list_to_string(a):
    return "".join(a)

a=["N","I","L","O","Y"]
print(convert_list_to_string(a))
```

# Find Index of List Item
```python
def find_index(a):
    return a.index(5)

a=[1,2,3,4,5,6]
print(find_index(a))
```

# Flatten Shallow List
```python
def flatten_list(a):
    v = []
    for sublist in a:
        for item in sublist:
            v.append(item)
    return v

a=[[1,2,3],[2,3],[4,5],[6,7]]
print(flatten_list(a))
```

# Append One List to Another
```python
def append_lists(v):
    b = []
    for sublist in v:
        if isinstance(sublist, list):
            b.extend(sublist)
        else:
            b.append(sublist)
    return b

v=[[2,3],[5],[5,6],[[5]],[4,5,6]]
print(append_lists(v))
```

# Select Random Item from List
```python
import random

def random_choice(a):
    return random.choice(a)

a=[1,3,5,6,7]
print(random_choice(a))
```

# Get Unique Values from List
```python
def get_unique_values(a):
    v = []
    for i in a:
        if i not in v:
            v.append(i)
    return v

a=[1,4,9,16,25,25,4]
print(get_unique_values(a))
```

# Count Frequency of List Elements
```python
def count_frequency(a):
    count = {}
    for i in a:
        if i in count:
            count[i] += 1
        else:
            count[i] = 1
    return count

a=[1,4,9,16,25,25,4,4,4,4,4]
print(count_frequency(a))
```

# Count Elements in List Within Range
```python
def count_elements_in_range(list, min, max):
    for i in list:
        if min <= i <= max:
            print(i)

a=[1,4,9,16,25]
count_elements_in_range(a, 2, 10)
```

# Compute Primes Using Sieve of Eratosthenes
```python
def prime_numbers(n):
    v = []
    for j in range(2, n + 1):
        for i in range(2, j):
            if j % i == 0:
                break
        else:
            v.append(j)
    return v

n = 11
print(prime_numbers(n))
```

# Create List with Range Concatenation
```python
def create_list_with_range(a, n):
    v = []
    for i in range(1, n):
        for j in a:
            v.append(j + str(i))
    return v

a = ['p', 'q']
n = 5
print(create_list_with_range(a, n))
```

# Find Common Items in Lists
```python
def common_items(m, n):
    return sorted(list(set(m) & set(n)))

m = [1,3,5,7,9,2,6]
n = [3,7,5,9]
print(common_items(m, n))
```

# Swap Every n-th and (n+1)th Values
```python
def swap_values(list):
    for i in range(0, len(list)-1, 2):
        list[i], list[i+1] = list[i+1], list[i]
    return list

list = [0,1,2,3,4,5]
print(swap_values(list))
```

# Convert Integers List to Single Integer
```python
def convert_to_single_integer(n):
    sum = ""
    for i in n:
        sum += str(i)
    return int(sum)

n = [11, 33, 50]
print(convert_to_single_integer(n))
```
```
