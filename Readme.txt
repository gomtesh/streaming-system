Design a streaming system using PySpark to perform different data aggregation analyses using SQL queries for any given data

Initially we had taken a Bank data of fraudulent transaction detection through credit cards which has around 63 Lakhs rows and 11 column and size is around 500 Mb. and divided them according to time stamps into various of .csv files which were around 800 in number using the GROUP BY function of SQL on Step Column. i.e. Maps a unit of time in the real world. In this case 1 step is 1 hour of time.
Group by function help us to identify steps and its count which means number of rows or number of transitions on that particular step.
We initially had 11 columns  out of which 2 are found to be redundant which were removed during the data cleaning process to avoid crowding.
In these particular files,  records of data which only carried one transaction in a time stamp were further removed to further remove redundancy.
After this step we had around 63 lakh rows and 9 columns.
After that our main objective that was to design a streaming system using pyspark and perform aggregation analytics of SQL.
In this structured streaming, we have  used a function called as “maxFilesPerTrigger” and set it value to 1 but its value is variable and since we were getting best results keeping  the value equal to 1 .
We have used various kinds of streaming windows on self-made data set ans check the difference in results.	



Pre-requisite
	1.	Install Jupiter notebook or use code in google colab
	2.	!pip install pyspark
	3.	!pip install pandas
	4.	Download csv file from https://www.kaggle.com/code/llabhishekll/fraud-transaction-detection/data
	5.	Run .ipynb block by block
