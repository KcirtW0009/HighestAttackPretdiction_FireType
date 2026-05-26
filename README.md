# 🔥 火系宝可梦最高攻击种族值预测

## 项目简介

本项目基于宝可梦官方API数据，通过**单因子线性回归模型**预测火系宝可梦的最高一攻种族值。项目从PokeAPI获取火系宝可梦的种族值数据，分析总种族值与最高攻击/特攻之间的关系，并构建预测模型。

## 📊 技术栈

- **数据获取**: PokeAPI GraphQL接口 (https://beta.pokeapi.co/graphql/v1beta)
- **数据处理**: Pandas, NumPy
- **数据可视化**: Matplotlib, Seaborn
- **机器学习**: Scikit-learn (LinearRegression)
- **开发环境**: Jupyter Notebook (Python 3.11.4)

## 🎯 功能特性

1. **数据采集**: 从PokeAPI获取所有火系宝可梦的完整种族值数据
2. **数据分析**: 提取HP、攻击、防御、特攻、特防、速度等关键属性
3. **特征工程**: 计算每个宝可梦的"最高一攻种族值"（攻击与特攻的较大值）
4. **可视化展示**: 绘制散点图和回归线，直观展示变量关系
5. **模型训练**: 使用60%测试集的线性回归模型
6. **预测功能**: 输入任意总种族值，预测对应的最高一攻种族值
7. **对比验证**: 自动匹配最接近的真实宝可梦数据进行验证

## 📁 项目结构

```
HighestAttackPretdiction_FireType/
├── HighestAttackPretdiction_FireType.ipynb  # 主程序（Jupyter Notebook）
├── README.md                                # 项目说明文档
├── LICENSE                                  # 开源许可证
└── .gitignore                               # Git忽略配置
```

## 🚀 快速开始

### 环境要求

```bash
pip install requests pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 运行步骤

1. 克隆本项目：
```bash
git clone https://github.com/KcirtW0009/HighestAttackPretdiction_FireType.git
```

2. 启动Jupyter Notebook：
```bash
jupyter notebook HighestAttackPretdiction_FireType.ipynb
```

3. 按顺序运行所有单元格

### 自定义预测

在Notebook中找到以下代码块，修改`Who`变量的值即可自定义预测：

```python
Who = 530  # 在这里输入你想要预测的宝可梦的总种族值
```

## 📈 模型性能

- **算法**: 单因子线性回归 (Ordinary Least Squares)
- **评估指标**: MSE, RMSE, R² Score
- **数据划分**: 训练集40% / 测试集60%
- **随机种子**: 42 (保证结果可复现)

## 💡 使用示例

输入总种族值 `530`，模型将：
1. 预测该总种族值对应的最高一攻种族值
2. 查找数据库中最接近该总种族值的真实火系宝可梦
3. 对比预测值与实际值的差异

## 📝 开发者信息

- **作者**: KcirtW0009
- **邮箱**: KcirtW0009@outlook.com
- **GitHub**: [KcirtW0009](https://github.com/KcirtW0009)

## 📄 许可证

本项目采用 MIT 许可证 - 详见 [LICENSE](LICENSE) 文件

## ⚠️ 注意事项

- 数据来源于PokeAPI，可能随游戏版本更新而变化
- 模型仅适用于火系宝可梦的数据范围
- 预测结果仅供参考，实际数值以游戏内数据为准

---

**最后更新**: 2026-05-26
