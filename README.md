# ECE2112_PA2
EXPERIMENT 2: NUMERICAL PYTHON (NUMPY)

# REPRODUCIBLE NORMALIZATION PROBLEM
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
<img width="819" height="175" alt="image" src="https://github.com/user-attachments/assets/e96821d4-3f11-49e6-9c16-43b66a140f7b" />



