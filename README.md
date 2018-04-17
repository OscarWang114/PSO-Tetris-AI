# PSO-Tetris-AI

This is a Term Project for CS3243 - Introduction to Artificial Intelligence at the National University of Singapore.

## Getting Started

These instructions will get you a copy of the project up and training the AI on your local machine. More details will be added in the future.

## Training the AI

Create a `tetris_log` folder in your home directory for the AI to log its training progress/result as a `.csv` file.

```bash
mkdir ~/tetris_log
```

Clone the project and compile.
```bash
git clone https://github.com/OscarWang114/PSO-Tetris-AI.git
cd PSO-Tetris-AI/src
java *.java jswarm_pso/*.java
```
Start training the Tetris AI. Note that you need to supply three arguments in the command for PSO. x1: Number of particles x2: Number of iterations x3: Number of threads
```bash
java PSO x1 x2 x3
```
For example: `java PSO 30 100 3` uses 30 particles and 100 iterations to train the data. The 30 particles are distributed among 3 threads, so each thread gets 10 particles and processes them sequentially. However, the 3 threads are executed **in parallel**, which can theoretically reduce the computational time by a factor of 1/3 compared to `java PSO 30 100 1`.

## Automated Training on Sunfire using Cron

We used the Sunfire Server provided by the National University of Singapore and Cron to automate the training phase. A guide on using Sunfire and Cron written by [OscarWang114](https://github.com/OscarWang114) can be found [here](https://hackmd.io/s/SJPWTzqsf).

## Built With

* [Java](https://www.oracle.com/java/index.html) - The language used
* [Cron](https://en.wikipedia.org/wiki/Cron) - The job scheduler used for training

## Authors

* **Oscar Wang** - *Java Coding (heurstics, PSO training, multithreading) and Cron Job executions* - [OscarWang114](https://github.com/OscarWang114)
* **Vivian Nguyen** - *Java Coding (heurstics) and Report Writing* -
[vivianmnguyen](https://github.com/vivianmnguyen)
* **Raphael Massart** - *Report Writing* -
[RaphaelMassart](https://github.com/RaphaelMassart)
* **Aishwarya George** - *Report Writing* -
[ash-g777](https://github.com/ash-g777)
* **Meriem Hrittane** - *PSO Studying and Researching*-
[mhrittane](https://github.com/mhrittane)


## Acknowledgments

* [JSwarm-PSO library](http://jswarm-pso.sourceforge.net/) and its author [Pablo Cingolani](http://www.mcb.mcgill.ca/~pcingola/) (pcingola@users.sourceforge.ne).
