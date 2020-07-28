---
layout: archive
title: "Portfolio"
permalink: /portfolio/
author_profile: false
---
<!-- Use this code for blog-style layout
{% include base_path %}
{% for post in site.portfolio %}
  {% include archive-single.html %}
{% endfor %}
-->

## PB-NVM: A High Performance Partitioned Buffer on NVDIMM

* ***DBMS:*** MySQL, MongoDB.
* ***Languages:*** C/C++, Python, Shell script.
* ***Technologies:*** PMDK from pmem.io, TPC-C, YCSB, Linkbench.
* ***Public paper(s):*** [SCIE paper](https://www.sciencedirect.com/science/article/pii/S1383762118303102?via%3Dihub#b1)
* ***Githubs:*** [[MySQL 5.7](https://github.com/trdtnguyen/mysql-pmem)] | [[MongoDB](https://github.com/trdtnguyen/mongo-pmem)]

<img src='/images/portfolio_imgs/project-PBNVM.jpg' width="700">

## DSM: A Low-Overhead, High-Performance, Dynamic Stream Mapping Approach for MongoDB 

* ***DBMS:*** MongoDB.
* ***Languages:*** C/C++, Shell script.
* ***Technologies:*** Multi-streamed SSD, YCSB, Linkbench.
* ***Public paper(s):*** [[SCIE paper](http://jise.iis.sinica.edu.tw/JISESearch/pages/View/PaperView.jsf?keyId=167_2231)] | [[Conf. paper](https://link.springer.com/chapter/10.1007/978-981-10-6520-0_1)]
* ***Github:*** [[mongo-mssd](https://github.com/trdtnguyen/mongo-mssd)]

<img src='/images/portfolio_imgs/project_DSM.jpg' width="700">

## Optimize MongoDB with TRIM command

* ***DBMS:*** MongoDB.
* ***Languages:*** C/C++, Shell script.
* ***Technologies:*** TRIM command, YCSB.
* ***Public paper(s):*** [[conf. paper](http://dl.acm.org/citation.cfm?id=3007844)]
* ***Github:*** [[mongo-trim](https://github.com/trdtnguyen/mongo-trim)]

Analyzed I/O characteristics of MongoDB using YCSB benchmark and _blktrace_. Described space management in WiredTiger. Optimized MongoDB using TRIM command, improved throughput up to 14.7%

<img src='/images/portfolio_imgs/project_TRIM.jpg'  width="700">
