# Machine-Learning-Theory
# 🧠 Why Learning **Theory** Matters

> *“There is nothing so practical as a good theory.”* — Kurt Lewin  

- **Predictive guarantees** – 理论告诉我们算法 *什么时候*、*为什么* 能泛化，避免仅凭经验调参。  
- **性能上界 / 下界** – 通过复杂度分析与信息论极限，判断一条思路是否已经“撞墙”，从而指引创新方向。  
- **可解释与鲁棒性** – 数学框架（泛化误差分解、稳定性、PAC-Bayes 等）帮助诊断模型脆弱点。  
- **跨领域迁移** – 概率论、优化、统计… 在深度学习与强化学习中形成统一语言，加速新算法设计。  

本仓库聚焦 **Machine Learning Theory** 全链条的核心学科资料，搭建起“从基础到前沿”的自学路线。

---

## 📂 Topics Covered

| 路径 (目录) | 内容概述 |
|-------------|-----------|
| **probability/** | 概率论与随机过程：大数定律、集中不等式、马尔可夫链。<br>教材：*Probability and Measure – Billingsley*, 练习笔记。 |
| **statistics/** | 统计决策与推断：渐近理论、假设检验、信息几何。<br>讲义：*Wasserman – All of Statistics*。 |
| **optimization/** | 凸优化与非凸景观：梯度法、内点法、自共轭函数、鞍点逃逸。<br>书籍：*Boyd & Vandenberghe*, *Nesterov*，个人推导笔记。 |
| **machine_learning/** | 统计学习理论：VC 维、Rademacher 复杂度、稳定性、核方法、PAC-Bayes。 |
| **reinforcement_learning/** | RL 理论：MDP 样本复杂度、后悔界、策略梯度收敛分析、函数逼近。<br>草稿书：*Agarwal - RL: Theory and Algorithms*。 |
| **deep_learning_theory/** | 宽网络 NTK，隐式偏置，梯度流动力学，表示能力与深度化。Workshop 论文阅读笔记。 |

> 每个子目录下包含  
> • 📚 **books/** – 官方 PDF/合法电子稿  
> • 📝 **notes/** – Markdown/Jupyter 笔记  
> • 🔗 **links.md** – 高质量外部资源索引  

---

## 🚀 Getting Started

```bash
git clone https://github.com/<MIStatlE>/<repo>.git
cd <repo>
open notes/optimization/first_order_methods.md   # macOS 示例


