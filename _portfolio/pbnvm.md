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

Most writes occured in DBMSs come from Buffer Management. Buffer management allocates a buffer pool in DRAM to enable CPUs quickly access to data pages without fetching them from storage device. When the buffer pool becomes full, DBMS evict dirty pages to storage devices to keep them durable. That process is mainly considered as a bottleneck due to:
1. Storage devices (e.g, hard disk) have slow IOs.
2. DBMSs must ensure atomicity and durability for individual evicted pages from buffer pool to storage device. That put on more overhead of the system.

One may solve the first problem easily by using fast storage device such as NVMe SSD instead of hard disks. However, the second problem is nontrivial due to:
* ***High lock contention.*** Centralized buffer pool causes high lock contention between query threads (threads update data on buffer pool) and eviction thread (thread flush dirty pages from buffer pool to storage devices).
* ***Redundant IOs.*** To ensure dirty pages are written "in-whole" to storage devices, InnoDB writes dirty pages first on douwlbe-write buffer (DWB) then writes the same copies on database tables (system tablespace, user tablespace).
* ***Long flushing time*** To ensure data durability, DBMS uses synchronized write that takes long flushing time. In other words, eviction thread hold the buffer pool's lock until it ensures all written data are durable in the storage device. During that period, query threads which access to the buffer pool must waiting for the lock.

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
