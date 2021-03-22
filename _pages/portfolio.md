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
## Correlation between Covid-19 and Economic (2020 - 2021)
* ***DBMS:*** MySQL.
* ***Languages:*** Python, HTML/CSS/Javascript, Shell script.
* ***Technologies:*** ETL, Apache Airflow, Apache Spark, Docker, Flask, Restful API
* ***Github:*** [sb-capstone](https://github.com/trdtnguyen/sb-capstone1)
This project provides ready-to-analyze datasets for Covid-19 and other related aspects in our daily life such as stock index, unemployment rate, job opennings, bussiness activities. We implement a full stack solution includes: (1) the front-end dashboard with Flask + jQuery, (2) ETL pipeline with Apache Spark + Python and Apache Airflow for scheduling ETL tasks and (3) MySQL as the back-end DBMS. 
<img src='/images/portfolio_imgs/project_covid_flowchart.jpg' width="700">


## Revisiting write-ahead logging with NVDIMM (2019)

* ***DBMS:*** MySQL.
* ***Languages:*** C/C++, Shell script.
* ***Technologies:*** PMDK from pmem.io, TPC-C, Linkbench.
* ***Public paper(s):*** [conf. paper](https://www.researchgate.net/profile/Trong_Dat_Nguyen/publication/336550336_Revisiting_write-ahead_logging_with_NVDIMM/links/5da524bfa6fdcc8fc3528a09/Revisiting-write-ahead-logging-with-NVDIMM.pdf)


<img src='/images/portfolio_imgs/project_WAL.jpg' width="700">

## PB-NVM: A High Performance Partitioned Buffer on NVDIMM (2018 - 2019)

* ***DBMS:*** MySQL, MongoDB.
* ***Languages:*** C/C++, Python, Shell script.
* ***Technologies:*** PMDK from pmem.io, TPC-C, YCSB, Linkbench.
* ***Public paper(s):*** [SCIE paper](https://www.sciencedirect.com/science/article/pii/S1383762118303102?via%3Dihub#b1)
* ***Githubs:*** [[MySQL 5.7](https://github.com/trdtnguyen/mysql-pmem)], [[MongoDB](https://github.com/trdtnguyen/mongo-pmem)]

<img src='/images/portfolio_imgs/project_PBNVM.jpg' width="700">

## MongoDB Journaling evaluation with NVDIMM (2017)

* ***DBMS:*** MongoDB.
* ***Languages:*** C/C++, Shell script.
* ***Technologies:*** NVDIMM, YCSB.
* ***Public paper(s):*** [[conf. paper](https://www.researchgate.net/profile/Trong_Dat_Nguyen/publication/329144714_MongoDB_Journaling_Evaluation_with_NVDIMM_Devices/links/5bf7dc46458515a69e360ef5/MongoDB-Journaling-Evaluation-with-NVDIMM-Devices.pdf)]

<img src='/images/portfolio_imgs/project_MongoDB_journaling.jpg' width="700">


## Dynamic Stream Mapping on MongoDB (2017)

* ***DBMS:*** MongoDB.
* ***Languages:*** C/C++, Shell script.
* ***Technologies:*** Multi-streamed SSD, YCSB, Linkbench.
* ***Public paper(s):*** [[SCIE paper](http://jise.iis.sinica.edu.tw/JISESearch/pages/View/PaperView.jsf?keyId=167_2231)], [[Conf. paper](https://link.springer.com/chapter/10.1007/978-981-10-6520-0_1)]
* ***Github:*** [[mongo-mssd](https://github.com/trdtnguyen/mongo-mssd)]

<img src='/images/portfolio_imgs/project_DSM.jpg' width="700">

## Optimize MongoDB with TRIM command (2016)

* ***DBMS:*** MongoDB.
* ***Languages:*** C/C++, Shell script.
* ***Technologies:*** TRIM command, YCSB.
* ***Public paper(s):*** [[conf. paper](http://dl.acm.org/citation.cfm?id=3007844)]
* ***Github:*** [[mongo-trim](https://github.com/trdtnguyen/mongo-trim)]

Analyzed I/O characteristics of MongoDB using YCSB benchmark and _blktrace_. Described space management in WiredTiger. Optimized MongoDB using TRIM command, improved throughput up to 14.7%

<img src='/images/portfolio_imgs/project_TRIM.jpg'  width="700">

## Stock Prices Matching (2013)

* ***OS:*** Androi.
* ***Languages:*** Java.
* ***Technologies:*** Androi Studio, Eclipse.
* ***Public paper(s):*** [[thesis paper](http://dcollection.knu.ac.kr/public_resource/pdf/000000057598_20200729013632.pdf)]
* ***Github:*** 
* ***Presentations:**** [[KDBC 2015](http://dbsociety.or.kr/kdbc2015/kdbc_conf.html)]

<img src='/images/portfolio_imgs/project_stockmatch.jpg'  width="700">
