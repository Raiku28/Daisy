# Daisy

Hadoop


Hadoop is an open source distributed processing framework that manages data processing and storage for big data applications in scalable clusters of computer servers. It's at the center of an ecosystem of big data technologies that are primarily used to support advanced analytics initiatives, including predictive analytics, data mining and machine learning. 

Hadoop's ability to process and store different types of data makes it a particularly good fit for big data environments. They typically involve not only large amounts of data, but also a mix of structured transaction data and semistructured and unstructured information, such as internet clickstream records, web server and mobile application logs, social media posts, customer emails and sensor data from the internet of things (IoT).

Install Hadoop
Step 1: Click here to download the Java 8 Package. Save this file in your home directory.

Step 2: Extract the Java Tar File.
Command: tar -xvf jdk-8u101-linux-i586.tar.gz

Step 3: Download the Hadoop 2.7.3 Package.
Command: wget https://archive.apache.org/dist/hadoop/core/hadoop-2.7.3/hadoop-2.7.3.tar.gz


Step 4: Extract the Hadoop tar File.
Command: tar -xvf hadoop-2.7.3.tar.gz

Step 5: Add the Hadoop and Java paths in the bash file (.bashrc).

Step 6: Edit the Hadoop Configuration files.
Command: cd hadoop-2.7.3/etc/hadoop/

Step 7: Open core-site.xml and edit the property mentioned below inside configuration tag:
core-site.xml informs Hadoop daemon where NameNode runs in the cluster. It contains configuration settings of Hadoop core such as I/O settings that are common to HDFS & MapReduce.

Command: vi core-site.xml

Step 8: Edit hdfs-site.xml and edit the property mentioned below inside configuration tag:
hdfs-site.xml contains configuration settings of HDFS daemons (i.e. NameNode, DataNode, Secondary NameNode). It also includes the replication factor and block size of HDFS.

Command: vi hdfs-site.xml

Step 9: Edit the mapred-site.xml file and edit the property mentioned below inside configuration tag:
mapred-site.xml contains configuration settings of MapReduce application like number of JVM that can run in parallel, the size of the mapper and the reducer process,  CPU cores available for a process, etc.

In some cases, mapred-site.xml file is not available. So, we have to create the mapred-site.xml file using mapred-site.xml template.

Command: cp mapred-site.xml.template mapred-site.xml

Step 10: Edit yarn-site.xml and edit the property mentioned below inside configuration tag:
yarn-site.xml contains configuration settings of ResourceManager and NodeManager like application memory management size, the operation needed on program & algorithm, etc.

Command: vi yarn-site.xml

Step 11: Edit hadoop-env.sh and add the Java Path as mentioned below:
hadoop-env.sh contains the environment variables that are used in the script to run Hadoop like Java home path, etc.

Command: vi hadoop–env.sh

Step 12: Go to Hadoop home directory and format the NameNode.
Command: cd

Command: cd hadoop-2.7.3



Step 13: Once the NameNode is formatted, go to hadoop-2.7.3/sbin directory and start all the daemons.
Command: cd hadoop-2.7.3/sbin

Step 14: To check that all the Hadoop services are up and running, run the below command.
Command: jps

![image](https://user-images.githubusercontent.com/77367704/104584181-22e1a700-569d-11eb-8ed2-db7948e11e11.png)

Advantages:
Advanced data analysis can be done in-house – Hadoop makes it practical to work with large data sets and customize the outcome without having to outsource the task to specialist service providers. Keeping operations in-house helps organizations be more agile, while also avoiding the ongoing operational expense of outsourcing.
Organizations can fully leverage their data – One alternative to not using Hadoop is simply not to use all the data and inputs that are available to support business activity. With Hadoop organizations can take full advantage of all their data – structured and unstructured, real-time and historical. Leveraging adds more value to the data itself and improves the return on investment (ROI) for the legacy systems used to collect, process, and store the data, including ERP and CRM systems, social media programs, sensors, industrial automation systems, etc.
Run a commodity vs. custom architecture – Some of the tasks that Hadoop is being used for today were formerly run by MPCC and other specialty, expensive computer systems. Hadoop commonly runs on commodity hardware. Because it is the de facto big data standard, it is supported by a large and competitive solution provider community, which protects customers from vendor lock-in.
