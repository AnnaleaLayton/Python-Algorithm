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

<img width="468" alt="image" src="https://github.com/AnnaleaLayton/Python-Algorithm/assets/133062663/94d4d1b7-771e-42f2-90d4-90b0cdae8935">


When using an .open() function that includes the argument "r" for “read,” I can call the .read() function in the body of the with statement. The .read() method converts the file into a string and allows me to read it. I applied the .read() method to the file variable identified in the with statement. Then, I assigned the string output of this method to the variable ip_addresses.


In summary, this code reads the contents of the "allow_list.txt" file into a string format that allows me to later use the string to organize and extract data in my Python program.

<h1>Convert the string into a list</h1>

In order to remove individual IP addresses from the allow list, I needed it to be in list format. Therefore, I next used the .split() method to convert the ip_addresses string into a list:

 <img width="390" alt="image" src="https://github.com/AnnaleaLayton/Python-Algorithm/assets/133062663/2ee6d776-b6d2-4b3f-9d03-30c389d493ec">


The .split() function is called by appending it to a string variable. It works by converting the contents of a string to a list. The purpose of splitting ip_addresses into a list is to make it easier to remove IP addresses from the allow list. By default, the .split() function splits the text by whitespace into list elements. In this algorithm, the .split() function takes the data stored in the variable ip_addresses, which is a string of IP addresses that are each separated by a whitespace, and it converts this string into a list of IP addresses. To store this list, I reassigned it back to the variable ip_addresses. 



