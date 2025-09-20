# Reverse String program

str = 'prashant'
rev = ""
strlen = len(str)
 
for i in str: 
    rev = i+rev
    
print(rev)

----------------------------------
# Find common letters
def find_common_letters(str1, str2):
    return sorted([char for char in set(str1.lower()) if char in str2.lower()]) 

Example usage
str1 = input("Enter first string: ")
str2 = input("Enter second string: ")
result = find_common_letters(str1, str2)
print("Common letters:", ", ".join(result) if result else "No common letters found")

--------------------------------------------

# Count character frequency in word
def count_freq(str):
    result = {}
    for i in str:
        if i in result:
            result[i] = result[i] +1
        else :
            result[i] = 1
    
    return result
    
dd = 'aasssfvv'
find = count_freq(dd)
print(find)

-----------------------------------------------------------------

# Convert to List to Dict
 (Condition both lenth should be match)
def list_string(l1,l2):
    return dict(zip(l1,l2))
    
dd = [1,2,3,4]
dd2 = [44,55,33,22]
find = list_string(dd,dd2)
print(find)

-------------------------------------------------------------
# Find missing number from array
def find_missing_no(no):
    no_len = len(no) +1
    
    excepted = 0
    for i in range(1,no_len +1):
        excepted ^=i
    
    actual = 0
    for d in no:
        actual ^=d

    return excepted ^ actual
    

no = [1,2,4,5,6]
res = find_missing_no(no)
print(res)

---------------------------------------------------------------
# Find array sum with target value in array

def find_target_sum(arr,target_sum):
    seen = set()
    pairs = []
    
    for n in arr:
        sum = target_sum - n
        if sum in seen:
            #seen.add(n)
            pairs.append((min(n,sum),max(n,sum)))
        else :
            seen.add(n)
    return pairs


dd = [1,2,4,3,5]
res = find_target_sum(dd,7)
print(res)

--------------------------------------------------------------------
# @property decorator with getter,setter and deleter example
class Person:
    def __init__(self, name):
        self._name = name  # Protected attribute (convention with underscore)

    @property
    def name(self):
        print("Getting name")
        return self._name

    @name.setter
    def name(self, value):
        print("Setting name")
        if not isinstance(value, str) or not value.strip():
            raise ValueError("Name must be a non-empty string")
        self._name = value.strip()

    @name.deleter
    def name(self):
        print("Deleting name")
        self._name = None

  Example usage
person = Person("Alice")
print(person.name)  # Getting name, prints: Alice
person.name = "Bob"  # Setting name
print(person.name)  # Getting name, prints: Bob
del person.name  # Deleting name
print(person.name)  # Getting name, prints: None

  Invalid input
try:
    person.name = ""  # Raises ValueError
except ValueError as e:
    print(e)  # Name must be a non-empty string

---------------------------------------------------------
# Factorial program
def factorial(n):
    if n < 0:
        return "Factorial is not defined for negative numbers"
    elif n == 0 or n == 1:
        return 1
    else:
        result = 1
        for i in range(2, n + 1):
            result *= i
        return result  
print(factorial(5))  # Output: 120

---------------------------------------------------------

# python function check if a year is a leap year
def is_leap_year(year):
    if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
        return True
    else:
        return False
print(is_leap_year(2020))  # Output: True
print(is_leap_year(1900))  # Output: False
print(is_leap_year(2000))  # Output: True

--------------------------------------------------------
# Binary searching
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = (left + right) // 2
        
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
            
    return -1


arr = [2, 3, 4, 10, 40, 50, 60, 70]
target = 10
result = binary_search(arr, target)
if result != -1:
    print(f"Element {target} is present at index {result}")
else:
    print(f"Element {target} is not present in array")


