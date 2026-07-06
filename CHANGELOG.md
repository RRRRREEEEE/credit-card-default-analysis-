# 变更日志

---

## 2026-07-05（阶段二+四推进）

### 阶段二：建模分析 ✅
- 训练/测试集划分（7:3，分层抽样，random_state=42）
- 逻辑回归模型：AUC=0.703，召回率=63.4%，最优阈值=0.50（天然校准）
- 随机森林模型：AUC=0.690，召回率=27%（默认）→ 调阈值至0.35后召回率=59.7%
- ROC曲线对比 + 特征重要性Top15 + 模型对比表
- 风险-价值四象限矩阵：LR概率 → 风险评分，年收入+贷款金额Z-score → 价值评分
- 3张新图：fig6_roc_curve.png, fig7_feature_importance.png, fig8_quadrant.png
- 结论：逻辑回归以更高AUC和更好可解释性胜出

### 阶段三：Tableau ⏭️
- 决定跳过：课程附件1未要求Tableau，matplotlib已产出8张图足够论文使用

### 阶段四：论文初稿 ✅
- 用 python-docx 生成完整论文：封面+目录+摘要+0~6章+参考文献+附录
- 含8张嵌入式图片
- 文件：`paper/贷款违约预测课程论文.docx`
- 个人信息留占位符，需自行填写

### 明天待办
- 打开论文替换个人信息占位符
- 检查图片显示、调整目录页码
- 生成评分表

### 完成
- **阶段一全部完成**：数据预处理 + 特征工程 + 可视化 + 导出
- 数据切换：UCI 信用卡数据 → 天池贷款违约预测数据
- 缺失值处理：employmentLength（未知）、n0~n14（中位数）、dti/pubRecBankruptcies/revolUtil（中位数）
- 异常值处理：dti 999%→中位数、annualIncome 99分位截断
- 特征工程：install_income_ratio、fico_mean、income_debt_ratio、credit_age
- 编码方案：grade/subGrade/regionCode/title → LabelEncoder，purpose → OneHot（13列）
- 标准化：56个特征 StandardScaler
- 5张可视化：违约率饼图、等级违约柱状图、箱线图、热力图、逾期vs违约柱状图
- 导出：cleaned_data.csv + model_ready_data.csv
- 创建任务追踪表、列名对照表.xlsx

### 当前状态
- **阶段**：阶段一 ✅ 完成 → 阶段二待开始
- **进度**：20%
- **下一步**：阶段二 — 逻辑回归 + 随机森林 + 特征重要性 + 四象限矩阵

### 关键变更
- 中文字体：SimHei → Microsoft YaHei（Windows 11 兼容性更好）
- 箱线图：pandas boxplot → seaborn boxplot
- purpose 编码：LabelEncoder → OneHot（参考天池社区方案）

### 遇到的问题
- VS Code 文件缓存：外部修改 notebook 后需关标签页再打开
- matplotlib 中文方框：换 Microsoft YaHei + 重启内核解决
- seaborn set_style 覆盖字体设置：plt.rcParams 放在 sns.set 之后
- dti 存在 999% 占位符错误值 → 中位数替换
- annualIncome 极端值 → 99分位截断

---

## 2026-07-04（准备阶段）

### 完成
- 项目计划书 v2.0 定稿
- 人机合作协定确立
- 甲方指令簿创建
- 关键决策记录创建
- 项目目录结构初始化

### 当前状态
- **阶段**：准备阶段 ✅ 完成
- **进度**：5%
- **下一步**：开始阶段一（下载数据集）

### 遇到的问题
- 无

---
