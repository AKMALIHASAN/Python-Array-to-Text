+++
title = "How to write array to text file in Python"
date = 2021-11-23
lastmod = 2021-11-24
draft = false
weight = 100
keywords = ["python write array to text file"]
description = "In this article, we will see how to create text file from array using different pre-defined functions in Python."
tags = ["Python", "Python Array"]
author = "A K M Ali Hasan"
postlink = 
inarticle = true
+++

# Python-Array-to-Text-File

 If we want to have a list of values with us, we can go with list or if we want to make it constant we can go with tuple; on the other hand in array we can we can have all the values of same datatype. We can have int, float, string together in one list but we can’t have int, float, string together in Array. Hence in array if all the values are Integer array then it calls int array if all the values are floating point then it calls float array, similar for string array.

## Now how to create a text file from array

### In order to do this we need to go with 3 main steps
i)	Open file  <br />
ii)	Process file  <br />
iii)	Close file  <br />


### First we are going define our main function

`def main():` <br />

And now I am going to open up my file by naming the variable name _“outputfile”_ because we need to output the data to file.

`Outputfile = open (‘file.txt’, ‘w’)`


Here I am going to user write mode. With write mode we can override any data that might exist; if the file doesn’t exist we are going to create that file.  We want the inputs each be on their own line. Therefore we concatenate the inputs with a new line character by using “\n”.

Then we can take 3 inputs 

`name = input("Please enter a name: ")` <br />
`address = input("Please enter a address: ")` <br />
`zipcode = input("Please enter a zip: ")` <br />

Then specify output file by _outputfile.write()_

`outputfile.write(name + '\n')` <br /> 
outputfile.write(address + '\n')` <br />
outputfile.write(zipcode + '\n')` <br />


These are going to write information to our file.

Finally we are going to close our file by 
`outfile.close()`

Then we are going to call our function  `main() `

After saving the code in order to compile and run it open cmd in the path of the file and run it as following 


![ffff](https://user-images.githubusercontent.com/55964681/142964069-764593fc-9a2a-4cc2-93d4-680211a1442f.png)


![i](https://user-images.githubusercontent.com/55964681/142966319-111e6a0d-90ac-4545-a8bd-24b29183b5a6.png)


After input the information we can notice no output here, because for the output we write a text file named _“info.txt”_

![g](https://user-images.githubusercontent.com/55964681/142966148-eb06e3d3-a7cd-4af6-8305-6bcff685b778.png)



## _Code_:

```python
def main() :
  
  # open the output file for writing. This will delete any existing data
  outputfile = open('info.txt', 'w')
  
  
  # get three inputs
  name = input("Please enter name: ")
  address = input("Please enter address: ")
  zipcode = input("Please enter zipcode: ")



  # save the information into the file
  outputfile.write(name + '\n')
  outputfile.write(address + '\n')
  outputfile.write(zipcode + '\n')

  # close the file
  outputfile.close()

#call the main function
main()
```

Now if I want to add more persons information we need to use append function "a” instead of write "w”.  

`Outputfile = open (‘file.txt’, ‘a’)`

By using append function we can enter multiple person’s information. If we try write function “w” for multiple person’s information input it will override not append the information. 



## _Code_: (Appending data)

```python
def main() :
  
  # open the output file for writing and appending. This will append with any existing data
  outputfile = open('info.txt', 'a')
  
  
  # get three inputs
  name = input("Please enter name: ")
  address = input("Please enter address: ")
  zipcode = input("Please enter zipcode: ")



  # save the information into the file
  outputfile.write(name + '\n')
  outputfile.write(address + '\n')
  outputfile.write(zipcode + '\n')

  # close the file
  outputfile.close()

#call the main function
main()
```

![l](https://user-images.githubusercontent.com/55964681/142966576-cd2ac871-9448-4013-bedc-27f155b0a462.png)

