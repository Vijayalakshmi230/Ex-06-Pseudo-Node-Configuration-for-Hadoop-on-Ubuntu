 Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu

## AIM

To implement Pseudo Node configuration for Hadoop on ubuntu

## Pre-requisites

a) jdk

Single-Node Configuration

1.	Create a dedicated user account for hadoop

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/b62fd35f-f243-4e8d-833f-1726e1cfb626)


2.	Install java1.8 in folder /usr/local

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/6492d282-691a-4e8c-a7bb-44a17def6b69)

 
3.	Install Hadoop

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/615ca447-696a-4c03-a7f3-148ddaf4e32f)


4.	Set the hadoop environment variables: Include the following lines in the
$HOME/.bashrc file

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/28ab0520-d16f-4c19-afdc-23ee967e5152)

 
5.	Set hadoop environment variables: Include the following lines /etc/profile file

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/f9bb071f-2256-441f-bbf7-6cfc3c48fc6e)


6.	Run the.bashrc & profile files from the $ prompt for updating the changes

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/561c82f6-eef2-417d-8ed8-b95fe0bb77e5)


![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/c3701a0f-c573-46bc-8328-8a09f612ad94)



![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/cc83f65f-56fd-41e2-81fa-378d875f5874)



$ bin/hadoop version	

7.	Configuration of the hadoop files: hadoop-env.sh, core-site.xml, mapred-site.xml, hdfs- site.xml and yarn-site.xml

path ::	/usr/local/hadoop-2.5.1/etc/hadoop

a)	hadoop-env.sh
Include the following lines in hadoop-env.sh file

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/ac401db9-fe85-4bc3-8942-7bd480cf364f)



b)	core-site.xml
Configure the directory for Hadoop to store its data files, the network ports it listens to, etc. Setup will use Hadoop’s Distributed File System (HDFS-single local machine)

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/ecd0ab7e-88c0-4f36-a08f-b2f8da6c1832)


 
Include the following lines in core-site.xml file between <configuration> and
</configuration> tags

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/107a99a2-ec67-42df-9ce0-f9367fe7ef73)


c)	mapred-site.xml

 ![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/9c68d52b-b2c5-449e-ac6c-dc4d5e248e96)


Include the following lines in mapred-site.xml file

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/e367ad47-e4b0-45c4-b78e-98684f413a54)

 

d)	hdfs-site.xml
Include the following lines in hdfs-site.xml file

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/64f4a2e0-4325-4cce-8a0c-42196aebf316)



e)	yarn-site.xml
Include the following lines in yarn-site.xml file

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/2f49ffb6-494a-4814-a2c8-302220d63cb1)



8.	Format the Hadoop File system implemented on top of the local file system using


![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/8df44792-851e-40f6-9cc9-589b27fdaed6)


9.	Start Hadoop using


![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/6d245faa-3c5b-49c8-875b-d62db3ff1d5c)


Explore Hadoop using http://localhost:50070/ from the browser	
 
10.	The commonly used HDFS Commands are as follows:

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/146e0b5f-75ec-4279-bf5f-740c7c9459bb)


11.	Create a directory ‘/input’ in HDFS

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/7e9a12c5-03f8-4a6e-9d80-53b0b4fadd76)


12.	Copy the input files into the distributed file system


![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/11f82d45-b416-4bb0-ba1c-a319b71eccff)



13.	Run some of the examples provided

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/28218114-c1e4-42aa-8398-a5a39c6375e9)


14.	Examine the output files

![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/bc2c32f1-209a-41ee-84c8-a3fef2f12df8)


Copy the output files from the distributed file system to the local file system and examine them:


![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/6658c945-b2e0-481f-89fb-38ee1d66c2db)

 
or
View the output files on the distributed file system


![image](https://github.com/Vijayalakshmi230/Ex-06-Pseudo-Node-Configuration-for-Hadoop-on-Ubuntu/assets/127175503/6b0ff6c8-37b2-4513-a526-1a5f2a613b18)




## Result:
Thus, the implementation of Pseudo Node configuration for Hadoop on ubuntu is successfully executed.
