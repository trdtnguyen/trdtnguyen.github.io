---
title: "DSM: A Low-Overhead, High-Performance, Dynamic Stream Mapping Approach for MongoDB"
excerpt: "Short description of portfolio item number 1<br/><img src='/images/portfolio_imgs/mssd/fig1_mssd.jpg'>"
collection: portfolio
---

In this project, we exploits Multi-Streamed SSD to optimize WiredTiger storage engine in MongoDB. Compared to the original WiredTiger, optimized one imporves the throughput by up to 65% in Linkbench.

For detail, view our [[paper](http://jise.iis.sinica.edu.tw/JISESearch/pages/View/PaperView.jsf?keyId=167_2231)].

## Multi-streamed SSD

***Erasing overhead.*** Out-of-place updates in NAND flash SSD require a data block (i.e., sector) must be erased before new data are writing on. Erasing a block with all invalid or valid data is fast. The Flash Translation Layer (FTL) just adjusts the mapping table (map logical block address to physical block address). However, with partial invalid blocks, that are blocks have some valid data pages, FTL must copy valid pages to new empty block before erasing the old one. That lead to copying overhead. How to minimize partial invalid blocks?. Multi-streamed SSD was born to answer that question.

***Multi-streamed SSD basic.*** Multi-streamed SSD allows applications from *user space* or *kernel space* assigning a stream along with a *write* or *pwrite* system call. As the results, all writes with the same stream ID alocated in the same NAND block. If the stream assigning in application is done properly, all pages in the same block will be invalid at the same time. Thus, minize the number of partial invalid blocks.

## Stream mapping strategies
Finding the properly stream mapping strategy is nontrivial. It depends on storage engines, file structures, and the applications (i.e., workloads).

