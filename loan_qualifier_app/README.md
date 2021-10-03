# Loan Qualifier Application

This is a python command-line interface application that allows users to see qualifying loans from lenders quickly and easily. The application works by taking in a `daily_rate_sheet` of loan criteria from various loan providers, asking the user a number of questions to evaluate their loan eligibility, and then returning to them a list of qualifying loans.

An application developer at fintech lending startup, was tasked with adding a new high priority feature that can prompt the user to save the qualifying loans as a new CSV file.  This project is an excellent way for the developer to demonstrate his skills in his new fintech career.

The main contribution or user story for the project is as follows:

Role: Biz operation

Goal: Create an enhancement in the software that will prompt the user to save the qualifying loan as a new CSV file.

Reason: To demonstrate the new software engineers’ skills in fintech career

---

## Technologies
The programming language used for this project is Python 3.9. In addition, the following libraries were imported and used in the coding:
1. Fire, 2. Questionary, 3. pathlib, 4. csv library 
Windows 10operating system used in executing the python coding.  
git bash and VS code which has a built in CLI and libraries are used for the project.

This project leverages python 3.9 with the following packages:

* [fire](https://github.com/google/python-fire) - For the command line interface, help page, and entrypoint.

* [questionary](https://github.com/tmbo/questionary) - For interactive user prompts and dialogs

For project visibilty and information sharing a repository was created in GitHub for tthis project named Challenge2_Repo.

---

## Installation Guide
Before running the application first install the following dependencies.
```python
  pip install fire
  pip install questionary
```
How To Install Python 3 on Windows 10
Step 1: Select Version of Python to Install, Step 2: Download Python Executable Installer, Step 3: Run Executable Installer, Step 4: Verify Python Was Installed On Windows.
Step 5: Verify Pip Was Installed, Step 6: Add Python Path to Environment Variables (Optional)

Python Fire is a library for automatically generating command line interfaces (CLIs) from python object. This can be installed in one of the following ways:
To install Python Fire from pypi, run:
pip install fire
Alternatively, to install Python Fire from source, clone the source and run:
python setup.py install

pip questionary installation
Use the package manager pip to install Questionary:
$ pip install questionary

---

## Usage
An sample block codes are shown below:
The easiest way to use Fire is to take any Python program, and then simply call fire.Fire() at the end of the program. This will expose the full contents of the program to the command line. An sample block code of fire usage is shown below:

  def run():
      """The main function for running the script."""
      # Load the latest Bank data
      bank_data = load_bank_data()

      # Get the applicant's information
      credit_score, debt, income, loan_amount, home_value = get_applicant_info()

      # Find qualifying loans
      qualifying_loans = find_qualifying_loans(bank_data, credit_score, debt, income, loan_amount, home_value)

      # Save qualifying loans
      save_qualifying_loans(qualifying_loans)

  if __name__ == "__main__":
        fire.Fire(run)

An sample of questionary usage block code are shown below:

Screenshots:
<img src="C:\Users\egeor\OneDrive\Desktop\Fintech\Challenge2_Repo\loan_qualifier_app\Images\Questionary_for_Applicants_bank_info.png">

Code blocks:
import questionary

def save_qualifying_loans(qualifying_loans):
    # using questionary, the user is asked to enter the file path where the file will be saved.
    ans_path = questionary.path("What file path do you want to save qualifying loans?").ask()

    ans_savefile = questionary.confirm("Do you want to save this file?").ask()
    if ans_savefile == True: 
         
    # if the answer by the user is yes, then the user will be promped to enter the file path and csv file to save the result.
        save_csv(qualifying_loans)
        
---
## Contributors
I wish to acknowledge the following contributors to the success of this project:
  Camden Kirkland - Lead instrucor Rice University Fintech Bootcamp
  Jonathan Randolph - TA  Rice University Fintech Bootcamp
  Kenneth Igben - TA  Rice University Fintech Bootcamp
  Caleb MacBride - TA  Rice University Fintech Bootcamp
My contact email is egeorge2013khs@gamil.com 

My LinkedIn profile: www.linkedin.com/in/emmanuel-george-mba-pmp-pcqi

References:
https://github.com/google/python-fire
https://www.google.com/search?q=how+to+install+python+on+windows+10&rlz=1C1JZAP_enUS900US901&oq=how+to+install+python&aqs=chrome.2.69i57j0i20i263i512j0i512l8.20367j0j15&sourceid=chrome&ie=UTF-8
https://pypi.org/project/questionary/

---

## License

MIT
