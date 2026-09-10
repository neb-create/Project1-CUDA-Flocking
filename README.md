**University of Pennsylvania, CIS 5650: GPU Programming and Architecture,
Project 1 - Flocking**

* Nico Kong
   [LinkedIn](https://www.linkedin.com/in/nicola-kong/), [Email]: nebfinn@gmail.com
* Tested on: Windows 11, AMD Ryzen AI 9 HX 370 @ 2.0GHz 32GB, GTX 4060 8GB (Personal Laptop)

Result:

Results are captured with Scattered Uniform Grid, 50000 Boids and 128 Block Size.

![screenshot](images/result.png)
![gif](images/result.gif)

## Performance Analysis

### Framerate change with increasing # of boids

Block Size: 128

**With Visualization**

| # Boids | Naive (fps) | Scattered Uniform Grid (fps) | Coherent Uniform Grid (fps) |
|---|---|---|---|
| 5,000    | 492.5 | 1160.8 | 1210.1 |
| 25,000   | 49.1 | 1024.4 | 1189.2 |
| 50,000   | 12.5 | 458.1 | 1194.8 |
| 100,000  | 3.9 | 268.3 | 1013.0 |
| 250,000  | 0.7 | 127.2 | 243.3 |
| 500,000  | 0.2 | 37.8 | 101.4 |

**Without Visualization**

| # Boids | Naive (fps) | Scattered Uniform Grid (fps) | Coherent Uniform Grid (fps) |
|---|---|---|---|
| 5,000    | 609.2 | 1878.9 | 2014.2 |
| 25,000   | 58.9 | 1132.5 | 1905.4 |
| 50,000   | 16.3 | 812.0 | 1630.3 |
| 100,000  | 4.5 | 416.2 | 1317.9 |
| 250,000  | 0.7 | 143.4 | 450.7 |
| 500,000  | 0.2 | 45.7 | 285.8 |

![boid count vs framerate graph](images/graph_boidcount.png)

### Framerate change with increasing block size

Method: WithVisualization, Coherent Uniform Grid, 100000 Boids

| Block Size | Framerate (fps) |
|---|---|
| 32   | 880.5 |
| 64   | 914.0 |
| 128  | 1013.0 |
| 256  | 596.2 |
| 512  | 564.3 |
| 1024 | 918.7 |

![block size vs framerate graph](images/graph_blocksize.png)

### Discussion Questions

**For each implementation, how does changing the number of boids affect performance? Why do you think this is?**


**For each implementation, how does changing the block count and block size affect performance? Why do you think this is?**


**For the coherent uniform grid: did you experience any performance improvements with the more coherent uniform grid? Was this the outcome you expected? Why or why not?**


**Did changing cell width and checking 27 vs 8 neighboring cells affect performance? Why or why not?**



