---
title: "PB-NVM: A High Performance Partitioned Buffer on NVDIMM"
excerpt: "PB-NVM architecture<br/><img src='/images/portfolio_imgs/PB-NVM/PB-arch.jpg'>"
collection: portfolio
---

In this project, we propose and implement PB-NVM, a partition NVM-based buffer to reduce lock contention and high overhead of the centralized buffer in InnoDB. Compared to the original InnoDB, our approach improves the throughput by up to 2.47 times while reducing the flushing time per transaction by up to 7 times.

## Atomic Write in Disk-based DBMS

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
