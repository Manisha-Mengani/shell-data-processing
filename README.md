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
 
 - ``` sort --help ```
 * To get theb help with the sort flags
 
