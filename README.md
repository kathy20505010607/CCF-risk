# 企业非法集资风险预测

#### 环境配置
Anaconda3-2018.12-Windows-x86_64
python 3.7.1
pandas 1.1.4
numpy 1.19.4
missingo 0.4.2
seaborn 0.9.0
tqdm 4.28.1
xgboost 1.2.1
lightgbm 3.1.0
catboost 0.24.3
sklearn 0.20.1


#### 目录结构


├── train
│   ├── annual_report_info.csv
│   ├── base_info.csv
│   ├── change_info.csv
│   ├── entprise_info.csv
│   ├── news_info.csv
│   ├── other_info.csv
│   ├── tax_info.csv
│   ├── entprise_evaluate.csv
│   └── entprise_submit.csv
├── CCF企业风险 
    ├── importance.csv  
    ├── result.csv 
    └── CCF企业风险.ipynb 


#### 训练和测试

读取entprise_info.csv中的数据，将之前处理过的数据表中的数据与entprise_info.csv中的数据结合形成训练集，
读取entprise_evaluate.csv中的数据，将之前处理过的数据表中的数据与entprise_evaluate.csv中的数据结合形成测试集，
填充数据集中的空值，选择重要特征存入列表，运行K折交叉验证和catboost算法进行训练和测试，并且得出特征的重要性用以分析。得出结果后，将id及对应
的score写入结果表格。