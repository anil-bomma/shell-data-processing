# shell-data-processing

## to retrieve text from url
* use the following command `[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12` to request content from an HTTPS.

* The curl command used to get data from the URL and store in a file is ```curl "https://en.wikipedia.org/wiki/Big_data" -o data.txt```

## to process text data
* ```tr ' ' '\12' < data.txt``` translate command is used to change arg1 to arg2, here empty space is changed to new line
pipe ( | )  Passes the output (stdout) of a previous command to the input (stdin) of the next one, or to the shell. This is a method of chaining commands together.
* ```tr ' ' '\12' < data.txt | sort``` adding to above point we have used pipe command to apply sort filter, here data is sorted in ascending order
* ```tr ' ' '\12' < data.txt | sort | uniq -c``` apply uniq and display count on the sorted output
* ```tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr```apply numerical comparison with reverse data(descending).
* ```tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr > result.txt``` adding to above command here the output will be saved in new file result.txt. 

### up arrow in bash
* Up arrow in bash shell is used to view previously executed command. 

### bash shell commands
1. "sort" sort the end result data in ascending order.
1. "-n" - sort the data by comparing with numerical value. 
1. "-r" - reverse the result data. 
1. "-" is used for a single letter flag. 
1. we will be using "--" when command is word and "-" if command is letter.
1. "<" to read input from file.
1. ">" write output to the file.
1. ">>" append the output to the given file.
1. usefull link: https://tldp.org/LDP/abs/html/special-chars.html#PIPEREF

