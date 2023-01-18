---
layout: default
title: VLT/SPHERE
parent: Telescopes Tips
grand_parent: To my students
nav_order: 8
---

### 1. Data archive

The VLT/SPHERE data can be fetched from the [SPHERE raw data query form](http://archive.eso.org/wdb/wdb/eso/sphere/form). For example, if we want to download the data taken with the project 096.C-0248, we can enter `096.C-0248` in the **Program ID** section and then click **Search**. You can then mark the observations you want to download by checking the boxes on the left of those rows, and then click **Request marked datasets**.
{: .fs-2 }

### 2. Pipeline installation

We can perform pipeline data reduction using the [https://irdap.readthedocs.io/en/latest/](IRDAP) python module. You can simply install it with pip wheel, which is instructed [https://irdap.readthedocs.io/en/latest/installation.html](here).
{: .fs-2 }

To make sure you installation is successful, you can follow the [https://irdap.readthedocs.io/en/latest/example.html](instruction) to run the demo data reduction. It calibrates the data taken with the project `096.C-0248`. You don't need to download the data. But you can try to download the same data from the archive following the instruction in Section 1, and then follow the instruction in Section 3 to see if you can get the same images as what are given by the demo.
{: .fs-2 }

### 3. Running pipeline

It is pretty simply to run the IRDAP pipeline. Please follow the instruction [here](https://irdap.readthedocs.io/en/latest/instructions.html).
{: .fs-2 }
