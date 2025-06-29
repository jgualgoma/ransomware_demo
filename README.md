# ransomware_demo

Please make sure the following packages and the latest python is installed on your machine:


cryptography  
os  
pathlib  
tkinter  
jupyter (for nbconvert)  
pyinstaller  




Inside this directory there should exist

- Ransom.ipynb  
- private_key.pem  



To create a Ransom.py python from Ransom.ipynb using the following command:

jupyter nbconvert --to script Ransom.ipynb

To convert the Ransom.py to a standalone executable, use following command

pyinstaller --windowed Ransom.py

If you wish to produce a standalone executable use the following command:

pyinstaller --windowed --onefile Ransom.py

Please note that on most machines this will trigger your antivirus software.

Output should be located in the created dist directory

The Ransom.ipynb is the original commented source code

The 'files' directory is the starting point for the encryption process. Please create a files directory in the same directory as the executable

The private_key.pem file is the private key used to decrypt files after encryption. Should the file be missing, a warning will be issued when trying to decrypt your files. Should a wrong private key be used, the decrypted files will be unintelligible, as the decryption algorithm has no way of knowing whether the key was correct or not.
