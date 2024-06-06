# 基于集成学习的2024欧洲杯预测
## 项目说明
    本项目是基于Kaggle开源的Baseline进行调整及优化，并对baseline进行逐行讲解。

    本项目所使用的数据集为国际足联世界排名1992-2024以及1872年至2024年欧洲杯之前的国际足球比赛数据。

    在本项目中，我们将问题变为分类问题，即我们最后模型的目标是预测主队的胜率和客场的平局/胜率。
    
    为了去除客场球队的优势，在项目中预测了客场和主场球队的变化结果(因为世界杯没有主场优势,仅在德国队比赛时考虑主场因素)，并使用两个预测的平均值作为概率。


## 数据集说明
    1872年至2024年国际足球成绩

    该数据集包括从 1872 年的第一场正式比赛到 2024 年的欧洲杯之前的国际足球比赛结果。
    比赛范围从FIFA世界杯到FIFI野生杯到常规友谊赛。
    这些比赛严格来说是男子的正式国际比赛，数据不包括奥运会或至少有一支球队是国家B队，U-23或联赛选择球队的比赛。
    
### results.csv包括以下列：
    date- 比赛日期
    home_team- 主队名称
    away_team- 客队名称
    home_score- 全职主队得分，包括加时赛，不包括点球大战
    away_score- 全场客队得分，包括加时赛，不包括点球大战
    tournament- 比赛名称
    city- 比赛所在的城市/城镇/行政单位的名称
    country- 比赛所在国的名称
    neutral- TRUE/FALSE 列，指示比赛是否在中立场地进行
    shootouts.csv包括以下列：

    date- 比赛日期
    home_team- 主队名称
    away_team- 客队名称
    winner- 点球大战获胜者
### 国际足联世界排名1992-2022

    country_full— 国家全名
    country_abrv— 国家缩写
    rank — 当前国家/地区排名
    total_points— 当前总分
    previous_points— 上次评分的总分
    rank_change — 排名变化
    confederation— 国际足联联合会
    rank_date— 评级计算日期

## 特征工程
    提取影响比赛结果的关键特征，作为模型的特征选择
## 我们的工作
    我们比较了五种不同的足球比赛结果预测建模方法：
#### 泊松回归
#### SVM
#### GBDT
#### 随机森林 
#### XGboost
    并选择了召回率较高的模型作为我们的预测模型，用于预测从小组赛到淘汰赛阶段的获胜者，最终预测德国队获得 2024 年欧洲杯冠军。
## 结果
### 小组赛预测结果
![image](https://github.com/Juvenilecris/2024_Euro_Cup_prediction/blob/main/imgs/%E5%B0%8F%E7%BB%84%E8%B5%9B.png)
### 淘汰赛预测结果
![image](https://github.com/Juvenilecris/2024_Euro_Cup_prediction/blob/main/imgs/%E5%B0%8F%E7%BB%84%E8%B5%9B.png)
