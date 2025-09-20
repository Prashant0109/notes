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
