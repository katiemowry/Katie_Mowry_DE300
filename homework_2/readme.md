PART I 
The DATA ENG Homework 2 Part I.ipynb file can be run directly, with all necessary csv files accessible. After importing all necessary libraries (duckdb, seaborn, matplotlib.pyplot, and textwrap), the data is loaded into a duckdb database, and this is verified by printing the tables within the database.

Question 1: An SQL query is used to create a summary of drug types and their total usage by ethnicity. Then, Python grouping is applied to print the top-used drug types for each ethnicity. A bar graph showing these results is also displayed. Finally, the resulting table is printed and exported for Part II.  

Question 2: An SQL query is used to create a summary of the procedures performed on patients of different age groups. Then, Python grouping is applied to print the top three procedures, along with the name of the procedures, for each age group. Finally, the resulting table is printed and exported for Part II.  

Question 3: An SQL query is used to display the patient, ethnicity, gender, and ICU length of stay. Then, Python is used to calculate the mean, standard deviation, and median for gender and ethnicity. Boxplots are generated for both gender and ethnicity to visualize the distributions. Finally, the resulting table is printed and exported for Part II.  

PART II
The DATA ENG Homework 2 Part II.ipynb file is run on the EC2 instance within the local port. A Docker container (from ‘Dockerfile’) was launched using the following command: 
docker run -p 8888:8888 \
  -v /home/ubuntu/.aws:/home/jovyan/.aws \
  -v /home/ubuntu/Katie_Mowry_DE300:/home/jovyan/work \
  my_jupyter

After launching the Docker container, a boto3 session is created and connected to Cassandra. A new keyspace is created, verified, and connected. Cassandra tables are created and the corresponding data is inserted from the exported csv files from Part I. Python queries are used to reproduce the analysis from Part I, and all printed results match the output from Part I.
