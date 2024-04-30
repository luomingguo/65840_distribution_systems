# 65840_distribution_systems
MIT 6.5840 Distribution Systems Spring 2024 实验课程


## 实验1 实现分布式系统MapReduce
你的任务是实现分布式的MapReudce，包括master(or coordinator)和worker两个部分。将会有一个coordinator进程，一个或多个工作进程并行执行。在真实的系统中，workers将会在很多不同的机器中运行，但是当前只是运行在一台机器上。worker和coordiator将通过RPC进行通信，每个worker将从coordinator获取任务，读取任务的输入（可能一个或多个文件），执行任务，并将任务的输出写入到一个或多个文件，并再向coordinator获取新任务。coordinator的任务是探察无法执行完任务的worker，coordinator的主逻辑在main/mrcoordinator.go，worker的主逻辑在main/mrworker.go（但不要更改这些文件）; 把实现放在 mr/coordinator.go, mr/worker, mr/rpc.go.
