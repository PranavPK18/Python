Overview

This repository contains solutions to several Python exercises focused on file handling, validation, user interaction, and AWS S3 integration.

Exercise 1 - Validation Exception

File: ex1.py (or implement as part of your project)

Description:

Validates mileage values from input.txt.

Raises a custom ValidationException if any mileage is not a valid integer.

Stops validation at the first invalid mileage and prints an error message.

Usage:
def ex1():
    try:
        validate_file("input.txt")
    except ValidationException as ve:
        print(ve)

ex1()

Exercise 2 - Total Gym Visits

File: ex2.py

Description:

Reads multiple CSV files (week-1.csv, week-2.csv, week-3.csv) containing gym visit data.

Calculates and prints the total number of gym visits across all weeks.

Usage:
def ex2():
    total = find_total_visits()
    print(f"Total visits: {total}.")

ex2()

Exercise 3 - Word Counter I/O

File: ex3.py

Description:

Reads words from an input file (words.txt).

Separates words into two categories: small words (less than 3 characters) and large words (3 or more characters).

Writes the separated words into small-words.txt and large-words.txt.

Prints the lists of small and large words.

Returns the total number of unique words.

Usage:
def ex3():
    total_words = count_words("words.txt")
    print(f"\nTotal words: {total_words}.")

ex3()

Exercise 4 - Calculator Log and S3 Upload

File: ex4.py

Description:

Repeatedly prompts the user to enter two numbers, calculates their sum, and logs the calculation.

When the user enters 'q', stops input and uploads the log file to an Amazon S3 bucket.

Requires AWS credentials and an existing S3 bucket.

Usage:
def ex4():
    calculate()

ex4()

Notes:

Update the student_id and bucket_name variables in the code before running.

Requires the boto3 Python package and AWS credentials configured.

Exercise 5 - Car List Builder

File: ex5.py

Description:

Reads mileage data from input.txt and car model data from car-ids.txt.

Filters out entries with invalid mileage (non-integer).

Combines the valid data into a list of dictionaries with keys id, miles, and model.

Prints the final list.

Usage:
def ex5():
    car_list = build_car_list()
    from pprint import pprint
    pprint(car_list)

ex5()

Setup & Requirements

Python 3.x

For Exercise 4, install AWS SDK for Python:

pip install boto3


Configure AWS credentials with:

aws configure


Prepare input files as described in each exercise.

Files Needed for Testing

input.txt (for Ex1, Ex5)

car-ids.txt (for Ex5)

week-1.csv, week-2.csv, week-3.csv (for Ex2)

words.txt (for Ex3)

Contact

For questions or help, feel free to reach out
