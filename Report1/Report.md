# Basic Information:

- Title: Neural Subgraph Counting with Wasserstein Estimator (Wasserstein Estimator下的神经子图计数)
- Authors: Hanchen Wang, Rong Hu, Ying Zhang, Lu Qin, Wei Wang, Wenjie Zhang
- Affiliation: University of Technology Sydney (悉尼科技大学)
- Keywords: Subgraph Counting, Graph Neural Network
- URLs: https://dl.acm.org/doi/10.1145/3514221.3526163, GitHub: None

# Summary:

- a. Research background of this article:
  - 本文介绍了图分析中的子图计数问题是一个基础的、被广泛应用于生物信息学、计算机视觉和社交网络分析等领域的研究问题。
- b. Past methods, their problems, and motivation:
  - 由于子图计数问题是 NP 完全问题，近似方法一直受到广泛研究，但这些方法不能处理大而复杂的查询和数据图。之前的机器学习方法要么仅支持小数据图，要么不能有效地利用数据图信息，这限制了它们的可扩展性、预测准确性和鲁棒性。
- c. Research methodology proposed in this paper:
  - 本文提出了一种新的近似子图计数算法 NeurSC，它由一个自适应提取模块和一个估计器组成，可以高效地从查询和数据图中提取和组合信息。NeurSC 的估计精度通过 Wasserstein 判别器得到改进，通过更新网络参数和查询和数据图之间的顶点对应关系，最小化了查询和数据图之间的 Wasserstein 距离。
- d. Task and performance achieved by the methods in this paper:
  - 在七个大型真实标记图上的实验结果表明，NeurSC 在预测精度和鲁棒性方面优于其他方法。

# Background:

- a. Subject and characteristics:
  - 本研究的主题是图分析中的子图计数问题，这是一个基础的、被广泛应用于生物信息学、计算机视觉和社交网络分析等领域的研究问题。
- b. Historical development:
  - 子图计数问题是 NP 完全问题，近似方法一直受到广泛研究。之前的机器学习方法要么仅支持小数据图，要么不能有效地利用数据图信息，这限制了它们的可扩展性、预测准确性和鲁棒性。
- c. Past methods:
  - 以前的机器学习方法仅支持小数据图，不能处理大而复杂的查询和数据图，也不能有效地利用数据图信息。
- d. Past research shortcomings:
  - 过去的研究方法未能充分利用数据图信息和支持大型数据图。
- e. Current issues to address:
  - 本文旨在解决现有机器学习子图计数方法在可扩展性、预测准确性和鲁棒性方面的局限性。

# Methods:

- a. Theoretical basis of the study:
  - 本研究基于图神经网络和 Wasserstein 判别器提出了一种新的近似子图计数算法 NeurSC。
- b. Technical route of the article (step by step):
  - 首先，NeurSC 的模块会自适应从查询图和数据图中提取子结构，以减少不利数据顶点的影响和提高模型的效率和可扩展性。然后，估计器将有效地组合查询和数据图的信息。最后，通过以 Wasserstein 判别器为基础的对抗训练提高了估计精度和质量。
  - NeurSC 的算法框架主要包括以下步骤：
    - 从查询图和数据图中提取信息并构建子图。
    - 利用 Wasserstein 判别器进行对抗训练并提高图的表示和估计精度。
    - 将子图集成到估计器中，计算估计值。

# Conclusion:

- a. Significance of the work:
  - 本文提出了一种新的近似子图计数算法 NeurSC，提高了子图计数问题的估计精度和可扩展性。
- b. Innovation, performance, and workload:
  - 本文的创新之处在于提出了一种适用于查询和数据图的子图计数算法，并将 NeurSC 与其他技术进行了比较，表明 NeurSC 模型在预测精度和鲁棒性方面都表现出色。
- c. Research conclusions (list points):
  - 本文提出了一种新的近似子图计数算法 NeurSC，它通过自适应提取模块和估计器从查询和数据图中提取和组合信息，并通过 Wasserstein 判别器来提高估计精度。
  - 在七个大型真实标记图上的实验结果表明，NeurSC 在预测精度和鲁棒性方面优于其他方法。
  - 未来研究方向还可以包括开发更加高效、可扩展的子图计数算法和扩展图神经网络以处理更大、更复杂的图像。