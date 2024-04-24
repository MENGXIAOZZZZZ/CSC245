# CSC245
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab1/assets/166454688/5ac2927c-cf94-4794-8b0c-8d6b421788fe)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab1/assets/166454688/66f9d3a3-fd11-40ed-af54-326cd322978f)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab1/assets/166454688/1899bf37-757c-44ca-abb6-b31db8f514e9)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab1/assets/166454688/85eeea27-40eb-4153-8018-d147e379d5d0)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab1/assets/166454688/7f5d5c60-4107-49dd-9820-3592706aad46)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab1/assets/166454688/064960d1-c3db-4e32-8770-fd85dc62e7dc)
![image](https://github.com/MENGXIAOZZZZZ/CSC245-lab1/assets/166454688/1e80b317-0268-4f65-b4a1-1fd80413dc64)



import numpy as np
# 1.Create a rank 2 (2D) array
my_array = np.array([[11, 12, 13, 14], [15, 16, 17, 18]])
print(my_array)

# 1. Create an array with 4 rows and 3 columns of zeros.
array_zeros = np.zeros((4, 3))
print(array_zeros)

# 2.Create an array of ones that has 3 rows and 4 columns.
array_ones = np.ones((3, 4))
print(array_ones)

# 3.Create an array containing integers 4 to 13 inclusive.
array_integers = np.arange(4, 14)
print(array_integers)

# 4.Create an array containing
array_floats = np.arange(0, 6, 1.5)
print(array_floats)

# 5.Create a 2 by 2 array containing '4' in each position.
array_fours = np.full((2, 2), 4)
print(array_fours)

# 6.Create 2 matrices   i. Identity matrix of size 4  
identity_matrix = np.eye(4)
print(identity_matrix)

# ii. Diagonal matrix with [10,12] as the diagonals 
diagonal_matrix = np.diag((10, 12))
print(diagonal_matrix)

# 7. Create a 3 by 3 array with random floats in [0, 10].
array_random_floats = np.random.uniform(0, 10, (3, 3))
print(array_random_floats)

# 8. Create a 3 by 3 array with random integers in [10, 20].
array_random_integers = np.random.randint(10, 21, (3, 3))
print(array_random_integers)

# 1. Use this array for the following practice: myArray = np.array([[11,12,13], [14,15,16], [17,18,19]])   a. Get a subarray of the first row and first 2 columns.  
myArray = np.array([[11, 12, 13], [14, 15, 16], [17, 18, 19]])
subarray_a = myArray[0, :2]
print(subarray_a)

# b. Change all elements in 1st and second row to 0.
myArray[:2] = 0
print(myArray)


# 2. Create an array that contains [0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20] and reverse the order.
reversed_array = np.arange(21)[::-1]
print(reversed_array)
# reshaping
myArray = np.array([[11, 12, 13], [14, 15, 16]])
reshaped_array = myArray.reshape(3, 2)
print(reshaped_array)

# MATH
myArray = np.arange(10)
# 1.Find the square of every number in array
squared_array = np.square(myArray)
print(squared_array)
# 2.Find the square root of every number in array
sqrt_array = np.sqrt(myArray)
print(sqrt_array)
# 3.Multiply the square of each number in array with its respective square root
result_array = squared_array + sqrt_array
print(result_array)


# ADDING ELEMENTS
myArray = np.array([[11, 12, 13], [14, 15, 16], [17, 18, 19]])
# 1
new_row = np.array([[20, 21, 22]])
myArray = np.vstack((myArray, new_row))
print(myArray)
# 2
myArray = np.array([[11, 12, 13], [14, 15, 16], [17, 18, 19]])
new_column = np.array([[30], [40], [50]])
myArray = np.hstack((myArray, new_column))
print(myArray)


# INSERTING ELEMENTS
# 1.Add 1 column of 1 to this array: myArray = np.zeros((2, 2))
myArray = np.zeros((2, 2))
new_column = np.ones((2, 1))
myArray = np.hstack((myArray, new_column))
print(myArray)
# 2.Add 2 rows of 2 to the answer from part 1
myArray = np.full((2, 3), myArray.shape[1], 2)
new_rows = np.full((2, myArray.shape[1]), 2)
myArray = np.vstack((myArray, new_rows))
print(myArray)
# 3.Remove the last column
myArray = np.delete(myArray, -1, axis=1)
print(myArray)
# 4.Remove the last row
myArray = np.delete(myArray, -1, axis=0)
print(myArray)


# DELETING ELEMENTS
myArray = np.matrix([[1, 2, 3], [4, 5, 6], [7, 8, 9]])
myArray = np.delete(myArray, 1, axis=1)
print(myArray)


# TEST EXERCISE Replace all odd numbers in the given array with -1
exercise_1 = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])
exercise_1[exercise_1 % 2 == 1] = -1
print(exercise_1)

# Convert a 1-D array into a 2-D array with 3 rows
exercise_2 = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8])
exercise_2 = exercise_2.reshape((3, -1))
print(exercise_2)

# Add 202 to all the values in given array
exercise_3 = np.arange(4).reshape(-2, -1) + 202
print(exercise_3)


# Generate a 1-D array of 10 random integers between 30 and 40 (inclusive)
random_array = np.random.randint(30, 41, size=10)
print(random_array)


# Find the positions of: elements in x where its value is more than its corresponding element in y, and  elements in x where its value is equals to its corresponding element in y.
x = np.array([21, 64, 80, 22, 74, 85, 31, 71, 90, 89])
y = np.array([21, 7, 3, 45, 2, 10, 75, 55, 4, 37])
positions_more = np.where(x > y)
positions_equal = np.where(x == y)
print(positions_more, positions_equal)


# Extract the first four columns of this 2-D array
exercise_6 = np.arange(100).reshape((5, -1))
first_four_columns = exercise_6[:, :4]
print(first_four_columns)


