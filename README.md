<h1> Project Description </h1>
  At my organization, access to restricted content is controlled with an allow list of IP addresses. The "allow_list.txt" file identifies these IP addresses. A separate remove list identifies IP addresses that should no longer have access to this content. I created an algorithm to automate updating the "allow_list.txt" file and remove these IP addresses that should no longer have access.

<h1> Open the file that contains the allow list!</h1>
For the first part of the algorithm, I opened the "allow_list.txt" file. First, I assigned this file name as a string to the import_file variable:
<img width="270" alt="image" src="https://github.com/AnnaleaLayton/Python-Algorithm/assets/133062663/290ae109-4e0f-4921-8117-a37a3483472f">

Then, I used a with statement to open the file:

<img width="406" alt="image" src="https://github.com/AnnaleaLayton/Python-Algorithm/assets/133062663/ca1b51e3-52df-4886-a612-f63acafa62a7">

In my algorithm, the with statement is used with the .open() function in read mode to open the allow list file for the purpose of reading it. The purpose of opening the file is to allow me to access the IP addresses stored in the allow list file. The with keyword will help manage the resources by closing the file after exiting the with statement. In the code with open(import_file, "r") as file:, the open() function has two parameters. The first identifies the file to import, and then the second indicates what I want to do with the file. In this case, "r" indicates that I want to read it. The code also uses the as keyword to assign a variable named file; file stores the output of the .open() function while I work within the with statement.


<h1> Read the file contents!</h1>
In order to read the file contents, I used the .read() method to convert it into the string.
