## ICE - 1 details are given below

#### Table of Contents

1. Overview of task
2. Code explanation
3. Output

### 1. Overview of task
For the given task urllib module is used to analyse the webpage to see what the page is about, the raw data is converted into token then finds the most frequent tokens later plotted into graph. ICE-1.ipynb contains code which is ready for execution.

### 2. Code explanation

##### step 1: import required libraries
Firstly, imported required python modules as given below. Following modules are required to run program successfully and to read accurate results.

![imported packages](https://github.com/chay2021/ICE-1/blob/main/importedpackages.png)

##### step 2: Choose page from internet
Once required modules imported, I choose SpaceX wiki page to extract keywords. To feed spaceX wiki page to python, used `urlopen` function as given below

![fetch Data URL](https://github.com/chay2021/ICE-1/blob/main/fetchDataUrl.png)

##### step 3: Read and parse data
Once page is given to `urlopen` function, next phase is read the page and process it by parsing the data. As given below, `read()` is the function from response which helps to read context from page. Once response is read, `BeautifulSoup` parse the data. 

![Parse Data](https://github.com/chay2021/ICE-1/blob/main/parseData.png)

In the above screenshot, there is another function `get_text(strip=True)` included to covert parse data into Text fields.

##### step 4: tokenize and clean the data

we split text into words using `split()` function. In general, we can notice several prepositions and grammatical words. Tried to avoid these keywords using python modules `stopwords` which is imported from `nltk.corpus`

![Tokenization of data](https://github.com/chay2021/ICE-1/blob/main/tokenizeData.png)

Above screenshot explains how tokenziation is done and how stopwords used to remove general english words from `clean_tokens`

##### step 5: Finding frequency of words

Determined frequency of words using `FreqDist()` function which is imported from nltk. There are few keywords repeated very less number of times. So, deleted those keywords using Dict for loop as given below and condition set to less than 5.

![Frequency of Words](https://github.com/chay2021/ICE-1/blob/main/FrequencyOfWords.png)

### 3. Output

for understanding purpose, printed all words with Frequency using ":" separator. 

![print Data](https://github.com/chay2021/ICE-1/blob/main/printData.png)

Finally, visualized the data in a graph. X axis indicates the keywords which are parsed from wiki page and Y-Axis indicates Frequency/Count of the words.

![data visualization](https://github.com/chay2021/ICE-1/blob/main/Graph.png)