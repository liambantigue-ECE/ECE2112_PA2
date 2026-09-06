# ECE2112_PA2
EXPERIMENT 2: NUMERICAL PYTHON (NUMPY)

# A. REPRODUCIBLE NORMALIZATION PROBLEM
The problem instructs us to "Create a reproducible random 5×5 integer ndarray named X." When I first read the problem I was reminded of our Z-score topic in our statistic class back in SHS. Basically, the problem uses a reproducible X as the population, a population mean (mu), a population standard deviation (s), a normalized value like "Z-score" stored as X_normalized, and lastly it must be a 5x5 ndarray.

The "reproducible random 5x5 integer ndarray" is provided for us using the statements:<br>
<img width="526" height="60" alt="image" src="https://github.com/user-attachments/assets/74ee16ea-fa8b-409d-9516-09aadadb8d0a" /><br>
- The first line makes sure the random values are reproducible while the second line sets the boundary of values from 10 until 100 not including 101, lastly it is in the form of a 5x5 array.

We then focus on getting the mu and s using numpy functions such as np.mean() and np.std():<br>
<img width="184" height="47" alt="image" src="https://github.com/user-attachments/assets/b1757a84-e4b2-4f4a-a30f-5eda4b989d78" /><br>
- We use the value of X as the parameter since they are POPULATION mean and standard deviation respectively.

To normalize the array values we use the formula X minus mu divided by s, we store the operation in "X_normalized" as instructed.<br>
<img width="387" height="66" alt="image" src="https://github.com/user-attachments/assets/7af8834f-d478-41f6-b11a-231d63c21153" />

The problem also instructs us to get the floating-point rounded mean and standard deviation of the normalized value and they must equal to 0 and 1 respectively, so once again we us the numpy functions np.mean(), np.std(), and np.round() storing them in Mean_normalized and Std_normalized:<br>
<img width="560" height="55" alt="image" src="https://github.com/user-attachments/assets/92f8ace7-c1bb-40ac-b1d4-b748984c8e5c" /><br>

Lastly, we print the required values and store the normalized array with filename "X_normalized.npy" using the function np.save(). I used an f-string inside the print to add labels and make it organized.<br>
<img width="819" height="175" alt="image" src="https://github.com/user-attachments/assets/e96821d4-3f11-49e6-9c16-43b66a140f7b" /><br>
**OUTPUT**:<br>
<img width="746" height="451" alt="image" src="https://github.com/user-attachments/assets/cc2d512c-e74f-4497-a4a4-ce6a3b4ca693" />

# B. CUBES DIVISIBLE BY 4 PROBLEM
The problem instructs us to "create the first 100 positive integers, cube every element, and reshape the result into a
10 × 10 ndarray named C." 

  To start, I debated on whether using np.arange() or np.linspace() because on the latter it INCLUDED 100 and i can't be bothered to use 101 for the former because I find it weird and cofusing however, I also found out that np.linspace() outputs FLOAT values but the problem requires INTEGERS so i went ahead and used np.arange(1, 101) which means from 1 to 100 with step of 1 (no step value specified defaults to a step value of 1). I also used the operator of double asterisks to turn the values into cube ** 3. Lastly, I reshaped the ndarray to 10x10 by using the function .reshape(10,10).<br>
<img width="555" height="36" alt="image" src="https://github.com/user-attachments/assets/68d5c77d-2781-4ad6-9471-77f42761f995" /><br>

 Next is to "Use a Boolean condition on C to obtain every cubed value divisible by 4. Store the selected values in
div by 4." <br>
We use the module operator % to determine if the value divided by 4 is evenly divided or not. If it is evenly divided it must be equal to 0 so next we use the equal to operator ==. Together. it is arrange like this: C % 4 == 0. To include the Boolean condition we use the array we want to extract the values that are TRUE from the brackets containing the condition, together it should look like C[ C % 4 == 0]. We then store it to div_by_4.<br>
<img width="290" height="39" alt="image" src="https://github.com/user-attachments/assets/3c0c9a18-af44-46e4-9af9-b6bfde0c03ed" /><br>

Lastly, we print the required checks such as shape of C, array div_by_4, number of selected elements, and finally save! <br>
<img width="703" height="161" alt="image" src="https://github.com/user-attachments/assets/1673b4b7-4bb0-43fe-b446-93995be16e09" /><br>
**note**: notice that in showing the number of selected elements I used a the function len() inside the brackets of the f-string instead of determining it outside the print statement.<br>
**OUTPUT**:<br>
<img width="861" height="306" alt="image" src="https://github.com/user-attachments/assets/256051e5-e016-43a0-a675-6d7d5ec837f2" />

# C. ABOVE-MEAN SQUARES PROBLEM
The problem instructs us to "Create a 6 × 6 ndarray named S containing the squares of the first 36 positive integers in increasing
row-major order."<br>

Same as problem B, we use the same syntax but squared instead of cubed.<br>
<img width="495" height="45" alt="image" src="https://github.com/user-attachments/assets/a4a84dbb-a738-4afb-9c46-38b5ce224af6" /><br>

Next is to "Compute the mean of all elements of S and store it in S_mean."<br>
Remember in problem A. we used the function np.mean(), we use the same function in finding the mean of all elements.<br>
<img width="231" height="36" alt="image" src="https://github.com/user-attachments/assets/ab2391c9-b30d-46c6-8125-023a04c8bf84" /><br>

Next requires a Boolean condition same as problem B. We use the same syntax but we change the condition to the requirement which is to "select only the elements strictly greater than S mean. Store these values in above_mean." It will be S > S_mean.<br>
<img width="311" height="31" alt="image" src="https://github.com/user-attachments/assets/ae7eecf6-53f7-4d07-a980-adff2923c16a" />

Lastly, we print the required checks such S, S mean, above mean, and the number of selected elements, and finally save! <br>
<img width="715" height="183" alt="image" src="https://github.com/user-attachments/assets/9bdd8c95-04e8-4dd6-a47b-59212ffd3b5a" /><br>

**OUTPUT**:<br>
<img width="834" height="401" alt="image" src="https://github.com/user-attachments/assets/7b5fa06c-c9f7-427b-9150-28f63b680865" />
