# Distributed Clustering
 
Implementation of Kmeans and Distance Based Outlier Detection with Hadoop MapReduce.

## Execution

### Kmeans

The program can be run in the terminal as such:

```bibtex
./kmeans.sh [file] [output] [centroids]
```

Where [file] is file with the training set located in hdfs, [output] is the hdfs direction where outputs are stored, and [centroids] is the initial centroids file hdfs.

An example of the command with values filled in:

```bibtex
./kmeans.sh /user/hadoop/data/points.csv /user/hadoop/output /user/hadoop/data/centroids.txt
```

### Distance Based Outlier Detection 

The program can be run in the terminal as such:

```bibtex
./outlier.sh [file] [output] [R] [k]
```

Where [file] is file with the two dimensional data points located in hdfs, [output] is the hdfs direction where outputs are stored, [R] is the radius around which neighbors are found and [k] is the minimum number of neighbors that does not make a point an outlier within a distance R.

An example of the command with values filled in:

```bibtex
./outlier.sh /user/hadoop/data/points.csv /user/hadoop/output 5 3 
```
