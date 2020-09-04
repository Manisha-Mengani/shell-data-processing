# shell-data-processing
### CURL
- CURL stands for cilent URL
- Command used to extract the text from the url
- ```curl "url" ```  
(here in place of url lets take https://en.wikipedia.org/wiki/Harry_Potter)

### To copy the text from url into a file
-  ```curl "https://en.wikipedia.org/wiki/Harry_Potter"  -O "data.txt" ``` 
(data.txt is the file name for which we need to copy the content)

### Commands to process the retrive data from the url
- ``` tr ' ' '\12' < data.txt ```
* This command will transform complete content into individual words with each word separated into single line
  
 - ``` tr ' ' '\12' < data.txt | sort ```
 * The output of the above command is pipped to sort it in an order
 
 - ``` tr ' ' '\12' < data.txt | sort | uniq -c ```
 * The output of the above command is pipped to unique occurances of the words
 
 - ``` tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr ```
 *  The output of the above command is pipped to sort the words in a reverse order with a numerical flag

 - ``` tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr > result.txt ```
 *  The output of the above command will copy all the results into result.txt file.
 
 
 
 ### Up Arrow in bash
 * Up Arrow in bash will help to retrive the previous commands in the existing bash window
 
 ### Getting help
 - ``` sort --help ```
 * To get the help with the sort flags that were used in sorting
 * "-n" - To sort the with numeric values
 * "-r" to sort data in reverse order
 * Only one dash is used for single letter flag
 * Two dashes when the flag is more than one letter
 
 ### Bonus points:
 * Using only your intellect and script commands, which file holds the positive comments?
   File A hold positive
 * Which file holds negative comments?
   File B hold negetive
 * How did you process the data? How confident are you?
   Just had a look into the file and performed operations to retrive the content of the both the files using commands below commands
   * ```tr ' ' '\12' < A.txt ```
   * ```tr ' ' '\12' < A.txt | sort```
   * ```tr ' ' '\12' < A.txt | sort | uniq -c ```
   * ``` tr ' ' '\12' < A.txt | sort | uniq -c | sort -nr > resultA.txt```
   
 * I used below commands to differentiate the content holiding by 
  * ``` $ cat A.txt | grep -i 'bad' -c ``` 
  * ``` $ cat B.txt | grep -i 'bad' -c ``` 
  * ``` $ cat B.txt | grep -i 'good' -c ``` 
  * ``` $ cat B.txt | grep -i 'good' -c ``` 

  * ![Manisha Mengani](CAPTURE.jpeg)
 
