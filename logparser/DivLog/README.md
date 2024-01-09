# DivLog

### Abstract

DivLog is an online LLM-based log parsing framework via in-context learning. It supports various LLMs as engines through API for high-quality parsing results.

Read more information about DivLog from the following papers:

+ Junjielong Xu, Ruichun Yang, Yintong Huo, Chengyu Zhang, and Pinjia He. [DivLog: Log Parsing with Prompt Enhanced In-Context Learning](https://doi.org/10.1145/3597503.3639155). *In 2024 IEEE/ACM 46th International Conference on Software Engineering (ICSE’24)*


### Running

Install the required enviornment:
```
pip install -r requirements.txt
```

Run the following scripts to start the demo by replacing "sk-xxx" to your own OpenAI API Key:

```
python demo.py -key sk-xxx
```

Run the following scripts to execute the benchmark by replacing "sk-xxx" to your own OpenAI API Key:

```
python benchmark.py -key sk-xxx
```

Re-generate embeddings by replacing "sk-xxx" to your own OpenAI API Key:

```
python embedding.py -key sk-xxx
```

If you wish to re-run all the results (which may cost much time and api budget), please delete the `results` repository:

```
rm -r results
```

### Benchmark

Running the benchmark script on Loghub_2k datasets, you could obtain the following results.

|      Dataset | Parsing Accuracy | Precision Template Accuracy | Recall Template Accuracy | Grouping Accuracy |
|:------------:|:-----------------|:----------------------------|:-------------------------|:------------------|
|     HealthApp| 0.9955           | 0.947368                    | 0.960000                 | 0.8700            |
|       OpenSSH| 0.9450           | 0.961538                    | 0.925926                 | 0.7530            |
|   Thunderbird| 0.9850           | 0.934211                    | 0.953020                 | 0.9630            |
|     Proxifier| 1.0000           | 1.000000                    | 1.000000                 | 1.0000            |
|        Apache| 1.0000           | 1.000000                    | 1.000000                 | 1.0000            |
|           HPC| 0.9970           | 0.914894                    | 0.934783                 | 0.9270            |
|     Zookeeper| 0.9980           | 0.886792                    | 0.940000                 | 0.7360            |
|     OpenStack| 0.9995           | 0.953488                    | 0.953488                 | 0.9785            |
|          HDFS| 0.9990           | 0.866667                    | 0.928571                 | 0.8880            |
|         Spark| 0.9995           | 0.972222                    | 0.972222                 | 1.0000            |
|          BGL | 0.9870           | 0.917355                    | 0.925000                 | 0.9720            |
|      Windows | 0.9980           | 0.918367                    | 0.900000                 | 0.9980            |
|        Linux | 0.9970           | 0.957627                    | 0.957627                 | 0.9940            |
|      Android | 0.9425           | 0.830409                    | 0.855422                 | 0.9300            |
|          Mac | 0.8625           | 0.675595                    | 0.665689                 | 0.8455            |
|       Hadoop | 0.9960           | 0.982609                    | 0.991228                 | 0.9940            |


### Citation

:telescope: If you use our logparser tools or benchmarking results in your publication, please kindly cite the following papers.

+ [**ICSE'19**] Jieming Zhu, Shilin He, Jinyang Liu, Pinjia He, Qi Xie, Zibin Zheng, Michael R. Lyu. [Tools and Benchmarks for Automated Log Parsing](https://arxiv.org/pdf/1811.03509.pdf). *International Conference on Software Engineering (ICSE)*, 2019.
+ [**DSN'16**] Pinjia He, Jieming Zhu, Shilin He, Jian Li, Michael R. Lyu. [An Evaluation Study on Log Parsing and Its Use in Log Mining](https://jiemingzhu.github.io/pub/pjhe_dsn2016.pdf). *IEEE/IFIP International Conference on Dependable Systems and Networks (DSN)*, 2016.