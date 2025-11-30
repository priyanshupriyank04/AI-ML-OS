# AI-ML-OS
🧠 AI-Driven CPU Scheduler

A hybrid Operating Systems + Machine Learning project

📌 Overview

This project implements a complete CPU scheduling simulator that models how an operating system selects which process runs on the CPU at any moment. It includes traditional CPU scheduling algorithms such as FCFS, SJF, and SRTF, and introduces machine-learning-based schedulers that learn process behavior and predict CPU burst lengths.

The goal is to explore how ML can improve scheduling decisions compared to classic OS scheduling policies.

🚀 Key Features
1. Full CPU Scheduling Simulation

Models CPU burst execution

Simulates I/O blocking and waiting queues

Handles arrival times, multiple CPU–I/O cycles, and priorities

Tracks waiting time, turnaround time, response time, and context switches

2. Classical Scheduling Algorithms

FCFS (First-Come, First-Served)

SJF (Shortest Job First)

SRTF (Shortest Remaining Time First)

These serve as baseline scheduling strategies.

3. Machine-Learning-Based Scheduling

Two ML-based schedulers are implemented:

ML-RF (Random Forest)

ML-XGB (XGBoost)

Both models predict the next CPU burst length using historical features and process statistics. The scheduler selects the process with the shortest predicted burst—similar to a learned version of SJF.

4. Automatic Dataset Generation

The simulator generates its own ML training dataset during execution.
Each time a CPU burst completes, it logs:

previous burst lengths

process type (CPU-bound / IO-bound)

priority

arrival time

total CPU consumed

total wait time

the actual next CPU burst (ML target label)

This creates a fully supervised learning dataset without external input.

5. Benchmarking Framework

All schedulers—classical and ML—are tested on identical workloads.
Benchmarked metrics include:

average waiting time

average turnaround time

average response time

context switches

This allows direct comparison between traditional schedulers and ML-driven approaches.

🎯 Project Objectives

Demonstrate how machine learning can support CPU scheduling

Compare classical vs ML schedulers on realistic workloads

Show that ML can approximate burst predictions and improve scheduling over FCFS

Build a complete end-to-end ML × OS simulation framework

📈 Summary of Results

SJF and SRTF perform best, as expected, since they assume perfect future knowledge.

ML-based schedulers outperform FCFS, demonstrating the value of learned predictions.

ML-RF and ML-XGB approximate SJF behavior without knowing the future, validating the feasibility of AI-assisted schedulers.

📝 Project Status

This project currently includes:

Synthetic process generator

Full scheduling simulator

Dataset logging system

Random Forest and XGBoost predictors

End-to-end benchmarking suite

🧩 Future Enhancements

Potential future work includes:

Neural network–based burst prediction

Reinforcement learning scheduler

More advanced feature engineering

Metrics like CPU utilization and throughput

Visualization dashboards
