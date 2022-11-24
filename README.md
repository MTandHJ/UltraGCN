


## run

```
conda create --name=UltraGCN python=3.7.9
conda activate UltraGCN
pip install -r requirements.txt
```

The dataset should consist of train/test.txt, in which each row represents a user.



### Gowalla

```bash
CUDA_VISIBLE_DEVICES=3 python main.py --config_file gowalla_config.ini
```

### Yelp2018


```bash
CUDA_VISIBLE_DEVICES=3 python main.py --config_file yelp2018_config.ini
```

### Books

```bash
CUDA_VISIBLE_DEVICES=3 python main.py --config_file amazon_config.ini
```

### ML-1M

```bash
CUDA_VISIBLE_DEVICES=3 python main.py --config_file ml-1m_config.ini
```

### CDs

```bash
CUDA_VISIBLE_DEVICES=3 python main.py --config_file amazoncds_config.ini
```

### Electronics

```bash
CUDA_VISIBLE_DEVICES=3 python main.py --config_file electronics_config.ini
```

## remove

```
conda activate base
conda remove -n UltraGCN --all
```



## Reproduction
See _benchmarks_ folder to reproduce the results.
For example, we show the detailed reproduce steps for the results of UltraGCN on the AmazoonBooks dataset in _UltraGCN_amazonbooks_x0.md_ file.



## Results
|   Model  | AmazonBooks | AmazonBooks        |  Yelp2018 | Yelp2018        |  Gowalla  |   Gowalla      |
|:--------:|:-----------:|:-------:|:---------:|:-------:|:---------:|:-------:|
|          |  Recall@20  | nDCG@20 | Recall@20 | nDCG@20 | Recall@20 | nDCG@20 |
|   NGCF   |    0.0344   |  0.0263 |   0.0579  |  0.0477 |   0.1570  |  0.1327 |
| LightGCN |    0.0411   |  0.0315 |   0.0649  |  0.0530 |   0.1830  |  0.1554 |
| **UltraGCN** |    **0.0681**   |  **0.0556** |   **0.0683**  | **0.0561**  |   **0.1862**  |  **0.1580** |
