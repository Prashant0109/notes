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


# Convert to List to Dict
# Condition both lenth should be match
def list_string(l1,l2):
    return dict(zip(l1,l2))
    
dd = [1,2,3,4]
dd2 = [44,55,33,22]
find = list_string(dd,dd2)
print(find)

