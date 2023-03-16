# HadoopFlumeExample
This example shows my efficiency with Hadoop and Apache Flume 
## Purpose
I created this example to learn about Apache Flume
## Achievement
I learned a lot about 
- Hadoop
- Linux
- Apache Flume
- Big Data
## Finished Work
For this project I wrote flume scripts which organized and saved data in hdfs using the date column and a flag comlumn.
### Data
The represented energy reading from a meter taken every 10 seconds. The column headings were dataID, meterID, date, time, energy cumalativeEnergyConsumption, and flag. All data were meant to be organized into folders following hierarchy energyData/year/month, and anything flagged showed be further organized into energyData/year/month/day.

![image](https://user-images.githubusercontent.com/59895799/225549050-485b30af-0837-4d8f-8195-556953db1466.png)

### Design
I used three agents. The first uses multiplexing to separate the flagged data and saves it to the HDFS and sends the non-flagged data to the second agent. Then the second agent replicates the non-flagged data and sends it to the third agent where there are two sources which read the data. The third one uses multiplexing to set their final directory paths and saves the final data in HDFS. This is better demonstrated in the diagram below:

![image](https://user-images.githubusercontent.com/59895799/225549251-5681f35c-18b7-4b6a-83b9-dc163fb7741f.png)

## Results
I was able to seperate and organize data perfectly.

Non-flagged Data
![image](https://user-images.githubusercontent.com/59895799/225549514-20ff3459-1ce0-4509-8a7c-d70e53f06222.png)

All the flagged data was stored in energyDataFlagged/year/month/date

![image](https://user-images.githubusercontent.com/59895799/225549624-b0951e0a-582f-4094-b692-2e751d54b712.png)
