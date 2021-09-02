# Summary of Big Data Technology Course Based on Hadoop

Table of Contents
================= 

- [Terminologies](#Terminologies) 
- [Characteristics](#Characteristics) 
- [Techniques](#Techniques)
- [Technology](#Technology)


## Terminologies 
- Name Node
- Date Node: Store the blocks
- Block: Are the chunks where the file is divided 
- Replica
- Rack: 
- Cluster:
- Yarn: is a cluster managmnet

## Characteristics
- 4 V’s of Big Data
- Principles pf Big Data
- 
## Techniques
##  Technology
- The core methods
- 1)setup () – To configure parameters like the input size, distributed cache, heap size.
   -  Method Definition- public void setup (context)

2)reduce () - often called as the Heart of the reducer. This is called once per key with the associated reduce task.
- Method Definition -public void reduce (Key,Value,context)

3)cleanup () – Executed only once at the end of reduce task for clearing all the temporary files.
