# EBS
* it is storage volumes/disks that you can attach to your EC2 instances. When a new instance is attached, it naturally has one EBS volume attached. That's where your Linux system installed. You could add more volumes, e.g., one for your app, one for your data etc. 

## EBS Volume Types
### IOPS vs Throughput 
* IOPS (# of read/write **operations** per second): Important metric for quick transactions, low latency apps, transactional workloads. It can be used to measure storage performance.
* Throughput (measure # of **bits** read or written per sec): important metric for large datasets, large I/O sizes, complex queries. The ability to deal with large datasets. 
### SSD vs HDD
* SSD (solid-state driver) vs HDD (hard-disk drive): see this [website](https://www.enterprisestorageforum.com/hardware/ssd-vs-hdd/) for image comparison
固态盘(SSD) 通常使用基于闪存的存储器来存储数据，因此没有活动部件。 它们具有比机械硬盘更快的读/写速度、更短的访问时间（更少的延迟）以及更高的每GB 存储成本。 机械硬盘(HDD) 使用旋转的磁性介质来存储数据，可通过执行器臂（非常类似于电唱机）上的读/写头访问数据。
* SSD: faster, shorter lifespan, more expensive, non-mechnical (flash), less fragile, best for stroing operating systems, gaming apps, and frequently used files
* HDD: slower, longer lifespan, cheaper, mechanical (moving parts), fragile, best for storing extra data like movies, photos and documents

### Boot Volume
The boot volume is essentially the working storage being used by the instance to utilize operating system code and other files and applications.

### EBS Volume Types
* General Purpose SSD (GP2): 3 IOPS per GiBs, up to max of 16000 IOPS per volume
* Provisioned IOPS SSD (io1): 50 IOPS per GiB. Up to 64000 IOPS per volume. 
    * Suitable for I/O intensive apps, large DBs, and latency-sensitive workloads. 
    * Choose it if focus more on IOPS.
* Throughput Optimized HDD (st1): 
    * suitable for storing big data, data warehouses, ETL and log processing.
    * Choose it if focus more on throughputs.

## Create an EBS and attach to an instance DEMO
* step 1: start the instance
* step 2: go to EC2 Volumes, "Create Volume". 
* step 3: Under "Actions", select "Attach Volume"