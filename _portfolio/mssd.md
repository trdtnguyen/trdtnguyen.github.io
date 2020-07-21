---
title: "DSM: A Low-Overhead, High-Performance, Dynamic Stream Mapping Approach for MongoDB"
excerpt: "Short description of portfolio item number 1<br/><img src='/images/portfolio_imgs/mssd/fig1_mssd.jpg'>"
collection: portfolio
---

In this project, we exploits Multi-Streamed SSD to optimize WiredTiger storage engine in MongoDB. Compared to the original WiredTiger, optimized one imporves the throughput by up to 65% in Linkbench.

For detail, view our [[paper](http://jise.iis.sinica.edu.tw/JISESearch/pages/View/PaperView.jsf?keyId=167_2231)].

## Multi-streamed SSD

Out-of-place updates in NAND flash SSD require a data block (i.e., sector) must be erased before new data are writing on. If there are some valid data pages on the block, they must be copied to new empty block before the old block is ereased. That lead to copying overhead. If the erasing block has all invalid pages, then there is no cost for copying back pages. That is the key point why multi-streamed SSD was born for.



<img src='/images/portfolio_imgs/mssd/fig1_mssd.jpg'>

