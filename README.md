# ransomware_demo

Please make sure the following packages and the latest python is installed on your machine:


cryptography
os
pathlib
tkinter
jupyter (for nbconvert)
pyinstaller


Contained in this project should be 3 items:

-a cyberproj directory
-the project report in PDF format
-and this README.txt

Inside the cyberproj directory there should exist

- files directory
- Ransom.ipynb
- Ransom.py
- private_key.pem

The Ransom.py is a python Script converted from Ransom.ipynb using the following command:

jupyter nbconvert --to script Ransom.ipynb

To convert the Ransom.py to a standalone executable, use following command

pyinstaller --windowed Ransom.py

If you wish to produce a standalone executable use the following command:

pyinstaller --windowed --onefile Ransom.py

Please note that on most machines this will trigger your antivirus software.

Output should be located in the created dist directory

If you're having trouble creating the executable, the Ransom.py file can be executed as a script using python, or the Ransom.ipynb can be executed through Jupyter. NOTE THAT THIS CAN BE DONE IF AND ONLY IF THE NECESSARY PACKAGES ARE INSTALLED



Please note that the executable should be built by the user on their machine, as uploading executables is usually not permitted on any web platform, including Moodle


The Ransom.ipynb is the original commented source code

The 'files' directory is the starting point for the encryption process

you can view the test files and directory structure inside the files folder. You may add additional files for testing if you wish to do so. 

The private_key.pem file is the private key used to decrypt files after encryption. Should the file be missing, a warning will be issued when trying to decrypt your files. Should a wrong private key be used, the decrypted files will be unintelligible, as the decryption algorithm has no way of knowing whether the key was correct or not.
