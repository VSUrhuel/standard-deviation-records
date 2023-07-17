
# Standard Deviation on Record

## Introduction:

Until this point, the programs you've created would only deal with processing information sent by the source code or the keyboard input. Yet, a program may also acquire its information from a file on a disk. For this exercise, the source of your information comes from a text file that is accessed sequentially.

Note that when reading a string data, the `getline()` function would be used, and it has the newline as the default delimiter. For example:

```cpp
string str;
getline(inRec, str, '\t'); // Reading a string with a tab delimiter
```

The standard deviation is acquired by the positive square root of the variance. The variance computed for intended for sample data is designated by s2.

𝑠^2 = ∑(𝑥 − 𝜇)^2 / (𝑛 − 1)

Where:
- 𝑥 - element in a population
- 𝜇 – mean (average)
- 𝑛 – size of the population

The standard deviation is the most commonly used measure of spread (dispersion). It indicates how compactly the values of a data set are clustered all around the mean.

## Learning Outcomes:

- Read data from a sequential file and place it in a structure.
- Compute the standard deviation of the record and write the result to another sequential file.

## Problem Background:

1. Create a text file named "StudentScore.txt" on the notepad with the following content:
   ```
   John 99
   Caleb 79
   Timothy 82
   Ruth 85
   Hannah 78
   Peter 92
   Joshua 88
   ```
   Note: The delimiter between the student name and the score is a tab stop (`\t`), while the delimiter between the score and the student name is a new line (`\n`). Be sure that there is no stray character at the end of your record.

2. On your C++ source code, define a structure as follows:

   ```cpp
   struct student
   {
      string studentName;
      double score;
   };
   ```

3. Implement the functions below:

   ```cpp
   /* Get the data from the text file and store it in the array of student 
   structure. Read a single record first, then use a looping structure controlled 
   by an ifStreamObj.eof() function to read all of the content of the text file.
   */
   void readFromRecord(student studScoreRec[]);

   /* Compute the average score on the studScoreRec[] array with size s.
   */
   double recAverage(student studScoreRec[], int s);

   /* Compute the standard deviation of the record.
   */
   double recSTDev(student studScoreRec[], int s);

   /* Write to a sequential text file named "scoreDescStat.txt" with the
   average and standard deviation as content.
   */
   void writeResultToFile(double ave, double stDev);
   ```

4. Call all the functions created in the `main` function.

## Contributing

If you would like to contribute to this project, you can follow these steps:

1. Fork the repository on GitHub.
2. Clone the forked repository to your local machine.
3. Create a new branch for your changes.
4. Make your modifications or add new features.
5. Test your changes to ensure they work correctly.
6. Commit your changes and push them to your forked repository.
7. Submit a pull request to the original repository, describing your changes in detail.

Please make sure to adhere to the existing coding style and conventions used in the project. Also, ensure that your changes are well-documented and accompanied by appropriate test cases.

We appreciate any contributions, including bug fixes, new features, and improvements to the existing codebase.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute the code as permitted by the license.

## Contact

If you have any questions or suggestions regarding this project, you can contact the project maintainers at [email@example.com](mailto:email@example.com).

Thank you for your interest in this standard deviation on record project!
