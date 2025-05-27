A Docker container (from ‘Dockerfile’) was launched using the following command: 

docker run -p 8888:8888
-v /home/ubuntu/.aws:/home/jovyan/.aws
-v /home/ubuntu/Katie_Mowry_DE300:/home/jovyan/work
my_jupyter

Required libraries: numpy, pyspark.sql, math 

1.	tf-idf definition
The data file is loaded and converted to an RDD. Three MapReduce functions are implemented: map_phase, shuffle_and_sort, and reduce_phase. These functions are run to calculate tf-idf measures for each document. The scores are saved in a new column called tfidf_score in a Spark DataFrame. The first 5 rows of the Spark DataFrame are printed. Finally, the full tf-idf measures for the first 5 documents are printed. 

2.	SVM Objective Function 
The data files are loaded, and values are extracted using RDDs. Similar to the first problem, three MapReduce functions are implemented: map_phase_svm, shuffle_and_sort_svm, and reduce_phase_svm. The loss_SVM function is written to run these functions and calculate the SVM loss. Lambda was set to 0.01 for this question. The final SVM loss is printed using the provided weights and bias.
