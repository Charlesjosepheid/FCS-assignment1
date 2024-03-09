#############
# Problem 1 #
#############

# Given a non-negative int n, return the count of the occurrences of 7 as a digit, so for example 717 returns 2.
# Hint: note that mod (%) by 10 yields the rightmost digit (126 % 10 is 6), while divide (/) by 10 removes the rightmost digit (126 / 10 is 12).

def count_7_recursive(n):
  print(n)
  if n == 0:
      return 0
  else:
      if n % 10 == 7:
          return 1 + count_7_recursive(n // 10)
      else:
          return count_7_recursive(n // 10)

n = int(input("Enter a non-negative integer: "))

print("Occurrences of digit 7 in", n, ":", count_7_recursive(n))

#############
# Problem 2 #
#############

# Given a set of characters and a positive integer k, print all possible strings of length k that can be formed from the given set.
# Example: Input: set[] = {'a','b'}, k = 3

# Output:
# aaa
# aab
# aba
# abb
# baa
# bab
# bba
# bbb

# def generate_strings(set_chars, k, prefix=""):
#   if k == 0:
#       print(prefix)
#       return
#   for char in set_chars:
#       new_prefix = prefix + char
#       generate_strings(set_chars, k - 1, new_prefix)

# set_chars = ['a', 'b']  
# k = 3  
# generate_strings(set_chars, k)

#############
# Problem 3 #
#############

# Write a function to compute the factorial of a number. The factorial of the number is defined as the product of all positive integers less than or equal to that number.
# Example: Factorial(3)=3*2*1=6

# def factorial(n):
#   if n == 0:
#       return 1
#   else:
#       return n * factorial(n - 1)

# n = int(input("Enter a non-negative integer: "))

# if n < 0:
#   print("Factorial is not defined for negative integers.")
# else:
#   print("Factorial of", n, "is", factorial(n))

#############
# Problem 4 #
#############

# You are given a list jumps of positive and negative integers which signify forward ornegative jumps.
# Starting at index 0, you jump to index 0+jump[0]. In general, if you are at index k, you would jump to index k+jump[k] Let's say jumps[0] was +2. Index becomes 2. Assuming jumps[2] was -1, index would become 1.
# Write the function list_jumps(jumps) where jumps is the aforementioned list. The function should return the string 'cycle' if the index will never leave the boundaries of the input list otherwise it must return 'out-of-bounds'. The starting index is always 0.

# def list_jumps(jumps):
#   def jump_helper(current_index, visited):
#       if current_index in visited:
#           return "cycle"

#       if current_index < 0 or current_index >= len(jumps):
#           return "out-of-bounds"

#       visited.add(current_index)
#       next_index = current_index + jumps[current_index]
#       return jump_helper(next_index, visited)

#   return jump_helper(0, set())

# jumps = list(map(int, input("Enter the list of jumps (separated by space): ").split()))

# print(list_jumps(jumps))  
