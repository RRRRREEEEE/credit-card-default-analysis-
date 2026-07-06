# 贷款违约预测与客户风险分层分析

基于机器学习的贷款违约预测模型构建与客户价值评估，高级商务数据分析课程项目。

## 数据下载

数据集来自阿里云天池平台：

🔗 **https://tianchi.aliyun.com/dataset/173753**

下载后将 `train.csv` 放入 `data/` 文件夹即可运行 notebook。

## 项目结构

```
├── loan_default_analysis.ipynb   # 主分析 notebook（可从头运行）
├── generate_paper.py             # 论文自动生成脚本
├── notebooks/                    # notebook 备份
├── figures/                      # 图表输出（notebook 运行后生成）
├── CHANGELOG.md                  # 变更日志
├── DECISIONS.md                  # 分析决策记录
└── README.md
```

## 技术栈

Python · pandas · numpy · matplotlib · seaborn · scikit-learn

## 运行方式

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter notebook loan_default_analysis.ipynb
# Kernel → Restart & Run All
```

## 论文摘要

本研究基于天池金融风控贷款违约预测数据集，分层抽样30,000条真实贷款记录，采用逻辑回归和随机森林构建违约预测模型。逻辑回归模型以 AUC 0.703、召回率 62.9% 的综合表现优于随机森林。在此基础上构建风险-价值四象限矩阵，将客户划分为明星/潜力/挽留/拒绝四类，为差异化策略提供数据支持。

## 许可证

本项目仅用于学习与课程展示。
