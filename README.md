# CS5296_Project
This is project repo of group 2 of CS5296 Cloud Computing.

The project is developed on AWS EMR 6.4.0.

Setting enviroment:

Create Cluster on EMR:
  Release label:emr-6.4.0
  Hadoop distribution:Amazon 3.2.1
  Applications:Spark 3.1.2, JupyterHub 1.4.1, JupyterEnterpriseGateway 2.1.0, Hive 3.1.2, TensorFlow 2.4.1, Livy 0.7.1
  
  -MASTER
    m5.xlarge
    4 vCore, 16 GiB memory, EBS only storage
    EBS Storage:32 GiB
    On-demand

  -CORE
    2 instances
    m5.xlarge
    4 vCore, 16 GiB memory, EBS only storage
    EBS Storage:32 GiB

  ![860038496f03eab351729696339d018](https://user-images.githubusercontent.com/19788285/164482875-0457eabe-3345-4725-90c9-056256b0fb64.png)
  ![d5de1992adfe87287a5fe9b8cb56c9d](https://user-images.githubusercontent.com/19788285/164483001-c351cbe5-c18e-4ac6-a337-6680a2f4c22f.png)

  Add configuation and bootstap actions, original file saved in /configuration
  ![e92f33c6f8136b07eb636b78ebbde5c](https://user-images.githubusercontent.com/19788285/164483025-e98d8854-f8ec-466b-a985-11f391b9143e.png)
  ![a3eaae2de494466521dd189b9bf1731](https://user-images.githubusercontent.com/19788285/164483058-1f532063-5d54-4ca3-be68-edba2d18358b.png)

Others setting by default.


