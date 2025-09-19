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
