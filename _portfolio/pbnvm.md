---
title: "PB-NVM: A High Performance Partitioned Buffer on NVDIMM"
excerpt: "PB-NVM architecture<br/><img src='/images/portfolio_imgs/PB-NVM/PB-arch.jpg'>"
collection: portfolio
---

In this project, we propose and implement PB-NVM, a partition NVM-based buffer to reduce lock contention and high overhead of the centralized buffer in InnoDB. Compared to the original InnoDB, our approach improves the throughput by up to 2.47 times while reducing the flushing time per transaction by up to 7 times.

## What're Prolems
Dabase Management Systems (DBMSs) work on two-tier architecture that CPUs access on working data kept on DRAM and write updates on files located on durable storages. Below figure show DBMS's compoents regard to two-tier architecture.
<div>
<img src='/images/portfolio_imgs/PB-NVM/PB-2tier.jpg'>
</div>

Buffer pool is an important component of Dabase Management Systems (DBMSs). However, buffer pool is mainly considered as a bottleneck due to:
1. Block devices have slow IOs
2. DBMSs must ensure atomicity and durability for individual evicted pages.

While the first is hardware problem, the second one is software problem. 

## PB-NVM Architecture

<div>
<img src='/images/portfolio_imgs/PB-NVM/PB-arch.jpg'>
</div>

## Experiment

<div>
<img src='/images/portfolio_imgs/PB-NVM/PB-TPCC-throughput.jpg'>
</div>

<div>
<img src='/images/portfolio_imgs/PB-NVM/PB-Linkbench-throughput.jpg'>
</div>

## Key Take-aways
