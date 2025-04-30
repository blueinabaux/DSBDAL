# Apache-Hadoop-Setup-Wordcount

## Let's setup the Hadoop nodes first
- Move to the **sbin or bin folder**
```bash
cd hadoop-3.4.1/sbin
```
OR
```bash
cd hadoop-3.4.1/bin
```
- Run the following commands
```bash
./start-dfs.sh
```
```bash
./start-yarn.sh
```
- Verify if the nodes are running
```bash
jps
```
### Debug Step
- If only **4** are running and **namenode** is missing or if you receive error like connection refused
```bash
hdfs namenode -format
```
- Restart again
```bash
./start-dfs.sh
```
```bash
./start-yarn.sh
```
## Scouting the files 
- Navigate to
```bash
hadoop-3.4.1 -> share -> hadoop -> mapreduce -> mapreduce-examples.jar -> org -> apache -> hadoop -> examples
```
- Extract these files
```bash
WordCount.class
WordCount$IntSumReducer.class
WordCount$TokenizerMapper.class
```
## Coding Part
- Follow instructions of [Yash Shinde](github.com/yash-73)
- Let's assume your **Wordcount.java** file has been created in **Desktop**
- Create a file named **input.txt** in the same directory with some content
- Run the following commands
```bash
 javac -classpath $(hadoop classpath)-d . WordCount.java
```
```bash
 jar cf wc.jar WordCount*.class
```
```bash
hdfs dfs -put input.txt /user/input/
```
```bash
hadoop jar wc.jar WordCount /user/input output
```
```bash
 hdfs dfs -cat output/part-r-00000
```
### Debug
- If input folder already exists make new one by appending more characters. **Do make changes in the commands**
- If it doesnt exist make one
```bash
hdfs dfs -mkdir /user/input
```
- If output folder already exists make new one by appending more characters. **Do make changes in the commands**
