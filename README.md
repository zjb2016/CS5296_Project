# CS5296_Project
This is project repo of group 2 of CS5296 Cloud Computing.

The project is developed on AWS EMR 6.4.0.

## Setting enviroment:

*Create Cluster on EMR*
  - Release label:emr-6.4.0 (python3.7)
  - Hadoop distribution:Amazon 3.2.1
  - Applications:Spark 3.1.2, JupyterHub 1.4.1, JupyterEnterpriseGateway 2.1.0, Hive 3.1.2, TensorFlow 2.4.1, Livy 0.7.1
  
  
*MASTER*
- m5.xlarge
- 4 vCore, 16 GiB memory, EBS only storage
- EBS Storage:32 GiB
- On-demand
  

*CORE*
- 2 instances
- m5.xlarge
- 4 vCore, 16 GiB memory, EBS only storage
- EBS Storage:32 GiB
- On-demand

![860038496f03eab351729696339d018](https://user-images.githubusercontent.com/19788285/164482875-0457eabe-3345-4725-90c9-056256b0fb64.png)
![d5de1992adfe87287a5fe9b8cb56c9d](https://user-images.githubusercontent.com/19788285/164483001-c351cbe5-c18e-4ac6-a337-6680a2f4c22f.png)

Add configuation and bootstap actions, original file saved in /configuration

![e92f33c6f8136b07eb636b78ebbde5c](https://user-images.githubusercontent.com/19788285/164483025-e98d8854-f8ec-466b-a985-11f391b9143e.png)
![a3eaae2de494466521dd189b9bf1731](https://user-images.githubusercontent.com/19788285/164483058-1f532063-5d54-4ca3-be68-edba2d18358b.png)

Others setting by default.

## Project Structure

This project is aimed at sentiment analysis on a text dataset, we trying to use ml lib provided by spark to do binary classification.

- **clf-without-preprocess.ipynb** is a naive experiment with ml lib.
- **clf-with-sparknlp.ipynb** is based on previous experiment, upgrading with sparknlp preprocess pipeline.
- **tensorflow.ipynb** is an unfinished attempt, the code with added preprocess procedure broke on emr(time out , still not figure out),also we trying to use Elephas to do the distributed computing with keras, it's hard to handle the package dependency on EMR, so I just post a naive version.


- **/data** is the data set we use , containing 25000 records both test and train file.
-  **/configuration** source scripts of setting sparknlp enviroment on EMR.

## References
- https://spark.apache.org/docs/latest/ml-guide.html
- http://nlp.johnsnowlabs.com/
