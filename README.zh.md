# 生物学中的人工智能智能体 (AI Agents)

本代码库是以下论文的配套资源：

> **[Artificial Intelligence agents for biological research: a survey](https://academic.oup.com/bib/article/27/1/bbag075/8499367)**
> 
> Cong Qi*, Wenbo Wang*, Siqi Jiang, Qin Liu, Xun Song, Hanzhang Fang, Zhi Wei  
> Briefings in Bioinformatics 27, no. 1 (2026).

该代码库组织了代表性的**生物学 AI 智能体系统**
根据论文中提出的**五维分类法**。
它被设计为**一个活跃的、持续更新的参考资源**
供计算机科学和生物学研究人员使用。

---

![agent workflow](images/agent_workflow.png)


![taxonomy](images/taxonomy_r1_sj.png)

![mapping](images/mapping.png)

---

## 📑 目录

- [概览：五维分类法](#概览五维分类法)
- [1. 生物学任务领域](#1-生物学任务领域)
  - [临床决策支持](#clinical-decision-support)
  - [知识发现和假设生成](#knowledge-discovery-and-hypothesis-generation)
  - [分子和药物设计](#molecular-and-drug-design)
  - [多组学分析](#multi-omics-analysis)
  - [探索性应用](#exploratory-applications)
- [2. 系统架构](#2-系统架构)
  - [单智能体系统](#single-agent-systems)
  - [多智能体系统](#multi-agent-systems)
  - [神经符号整合](#neuro-symbolic-integration)
- [3. 评估策略](#3-评估策略)
- [4. 交互模式](#4-交互模式)
- [5. 资源整合](#resource-integration)
  - [知识增强智能体](#knowledge-augmented-agents)
  - [工具增强智能体](#tool-augmented-agents)
- [基准测试](#benchmark)
- [维护与更新](#维护与更新)
- [引用](#引用)

---

## 概览：五维分类法

我们从五个维度组织现有的生物学 AI 智能体研究：

1. **生物学任务领域**  
2. **系统架构**  
3. **交互模式**  
4. **评估策略**  
5. **资源整合**

每个部分都列出了代表性系统以及简明的参考
原始出版物的信息和直接链接。

以下是总体的 **分类表**。
要查看详细的子类别，请单击表中的 **领域** 标题。

---

## 1. 生物学任务领域

此维度按人工智能智能体解决的生物学问题对其进行分类。

### 临床决策支持

- **[Leveraging Large Language Models for Decision Support in Personalized Oncology](https://jamanetwork.com/journals/jamanetworkopen/fullarticle/2812097#google_vignette)** (*2023*) `JAMA Network Open`
  > 本研究通过将四种大型语言模型在精准肿瘤学中的治疗建议与人类专家的建议进行比较，评估了它们作为助手的表现。虽然模型产生了更多的候选治疗方案，但由于支持证据有限，它们与专家决定的总体一致性较低，尽管出现了一些临床上有用和独特的建议。研究结果表明，LLM 可能会支持想法生成和文献筛选，但不能取代专家判断。


- **[SensitiveCancerGPT: Leveraging Generative Large Language Model on Structured Omics Data to Optimize Drug Sensitivity Prediction](https://pmc.ncbi.nlm.nih.gov/articles/PMC11888479/)** (*2025*) `bioRxiv`
  > 本工作探讨了使用生成式大型语言模型从结构化药物基因组学数据进行药物敏感性预测。通过特定领域的提示工程和微调，GPT 在多个数据集上实现了强大的性能和泛化能力，在多种设置中超越了既定的基准。结果表明，生成式 LLM 可以作为支持精准肿瘤学研究的有效计算工具。

- **[CART-GPT: A T Cell-Informed AI Linguistic Framework for Interpreting Neurotoxicity and Therapeutic Outcomes in CAR-T Therapy](https://pmc.ncbi.nlm.nih.gov/articles/PMC12363796//)** (*2025*) `bioRxiv`
  > 本文介绍了 CART-GPT，这是一个基于 Transformer 的模型，在超过一百万个 CAR-T 单细胞 RNA-seq 概况上进行训练，以预测 CAR-T 治疗中针对患者的治疗反应和神经毒性风险。该模型在实现强大预测性能的同时，还提供了可解释的见解，表明治疗结果是由协调的 T 细胞状态子集驱动的，而不是单一的细胞类型。通过将单细胞预测与患者水平的结果联系起来，并发布大型注释图谱，该研究证明了基础模型对精准 CAR-T 治疗计划的价值。



- **[Exploring the Potential of AI-powered Applications for Clinical Decision-making in Gynecologic Oncology](https://obgyn.onlinelibrary.wiley.com/doi/abs/10.1002/ijgo.70251)** (*2025*) `International Journal of Gynecology & Obstetrics`
  > 本研究通过将其建议与妇科和乳腺癌病例的多学科肿瘤委员会决定进行比较，评估了 GPT-4 自动提供治疗建议的能力。GPT-4 生成了连贯且临床上合理的建议，但仍然存在准确性和完整性方面的限制，特别是在手术和全身治疗的选择上。迭代提示显着提高与专家决定的符合性，表明 GPT-4 可以作为临床决策的支持工具，而不是替代医生。



- **[Chatbot for the Return of Positive Genetic Screening Results for Hereditary Cancer Syndromes: A Prompt Engineering Project](https://cancer.jmir.org/2025/1/e65848)** (*2025*) `JMIR Cancer`
  > 本研究设计并评估了由 GPT-4 提供支持的聊天机器人，以支持大型公共卫生计划中全人群阳性基因组筛查结果的反馈。专家评估表明，聊天机器人提供清晰、用户友好且符合上下文的沟通，在语气、可用性和边界管理方面表现良好，尽管计划特有的准确性需要提高。研究结果证明了基于 LLM 的聊天机器人在增强遗传咨询服务和改善基因组医疗保健可及性方面的可行性。


- **[Evaluating the Use of Generative Artificial Intelligence to Support Genetic Counseling for Rare Diseases](https://www.mdpi.com/2075-4418/15/6/672)** (*2025*) `Diagnostics`
  > 本研究评估了四个生成式 AI 模型回答罕见病和遗传咨询问题的能力，重点是准确性和安全性。虽然所有模型通常都提供了可靠和专业的信息，但性能各不相同，ChatGPT 得分最高，而 Perplexity 显示出最多低质量的回答。结果突出了生成式 AI 在支持患者及其家属方面的潜在价值，同时强调需要专家监督以减少不准确和歧义。




- **[Innovations in Medicine: Exploring ChatGPT’s Impact on Rare Disorder Management](https://www.mdpi.com/2073-4425/15/4/421)** (*2024*) `Genes`
  > 这篇综述检查了 AI，特别是 ChatGPT，在推进罕见病和遗传病的研发、教育和临床实践中的作用。它强调了 AI 在改善个性化患者护理方面的潜力，同时批判性地讨论了当前的局限性和风险。该研究概述了未来开发可以更好地支持医疗保健专业人员和患者进行罕见病管理的 AI 工具的方向。



- **[Importance of Prior Patient Interactions With the Healthcare System to Engaging With Pretest Cancer Genetic Services via Digital Health Tools Among Unaffected Primary Care Patients: Findings From the BRIDGE Trial](https://onlinelibrary.wiley.com/doi/full/10.1111/1475-6773.14652)** (*2025*) `Health Services Research`
  > 这项随机试验调查了未受影响的初级保健患者通过数字健康工具开启关于癌症遗传服务的患者门户消息，以及启动检测前遗传护理的相关因素。患者的参与度在很大程度上受先前与医疗保健系统互动的影响，如频繁的门户使用和初级保健就诊，而社会人口统计学和临床特征并未显示出显著影响。研究结果表明，改善医疗保健和数字工具的可及性可能是提高癌症遗传服务使用率的关键。



- **[Improving Automated Deep Phenotyping Through Large Language Models Using Retrieval Augmented Generation](https://link.springer.com/article/10.1186/s13073-025-01521-w)** (*2025*) `Genome Medicine`
  > 本研究介绍 RAG-HPO，这是一种检索增强生成方法，利用大型语言模型改进了从临床文本中自动提取人类表型本体术语的过程。通过将 LLM 与经过策划的表型数据库相结合，RAG-HPO 在准确率、召回率和 F1 分数上显着优于现有的基于规则的工具，同时最大限度地减少了幻觉。结果表明，检索引导的 LLM 能够为罕见疾病诊断和临床基因组学研究提供准确可靠的表型提取。




- **[GeneGPT: Augmenting Large Language Models with Domain Tools for Improved Access to Biomedical Information](https://academic.oup.com/bioinformatics/article/40/2/btae075/7606338)** (*2024*) `Bioinformatics`
  > 本工作提出了 GeneGPT，一个通过直接调用 NCBI Web API 使大型语言模型能够回答基因组学问题的框架。通过在上下文中学习生成并执行 API 调用并结合增强解码，GeneGPT 显着减少了幻觉并在 GeneTuring 基准测试上达到了最先进的性能。结果表明，工具增强的 LLM 可以在基因组学任务中可靠地进行复杂的多跳推理。



- **[Assessing the Utility of Large Language Models for Phenotype-Driven Gene Prioritization in Rare Genetic Disorder Diagnosis](https://www.cell.com/ajhg/fulltext/S0002-9297(24)00296-9)** (*2024*) `The American Journal of Human Genetics`
  > 本研究评估了多个大型语言模型在跨不同提示、输入类型和任务设置下罕见疾病诊断中由表型驱动的基因优先排序。尽管 GPT-4 表现最好，但其准确性仍大大低于传统基因优先排序工具，并且从检索增强或少样本学习中获得的益处有限。研究结果强调了 LLM 在临床基因组工作流程中的潜力以及当前的局限性，包括对充分研究的基因的偏见。



- **[A Comparative Evaluation of ChatGPT 3.5 and ChatGPT 4 in Responses to Selected Genetics Questions](https://pubmed.ncbi.nlm.nih.gov/38872284/)** (*2024*) `Journal of the American Medical Informatics Association`
  > 本研究使用遗传咨询师和临床医生的专家审查，评估了 GPT-4 与 GPT-3.5 相比提供关于 BRCA1、HFE 和 MLH1 的遗传信息的能力。GPT-4 在准确性上有显著提高并且整体相关性较好，但仍然存在持续的错误和可用性限制。研究结果突出了 GPT-4 在遗传学教育中的前景，同时强调在临床使用中需要持续完善和伦理监督。



- **[Biomni: A General-Purpose Biomedical AI Agent](https://pmc.ncbi.nlm.nih.gov/articles/PMC12157518/)** (*2025*) `bioRxiv`
  > 本文介绍 Biomni，一种通用的生物医学 AI 智能体，旨在自主执行跨不同生物医学领域的复杂研究任务。通过将大型语言模型推理与检索增强计划和基于代码的执行相结合，Biomni 展示了在基因优先级排序、药物重新定位和罕见疾病诊断等任务上强大的泛化能力，而无需针对特定任务进行调整。结果表明，AI 智能体系统可以显着提高生物医学研究效率，并支持人类科学家处理复杂的发现工作流程。




- **[BioLab: End-to-End Autonomous Life Sciences Research with Multi-Agents System Integrating Biological Foundation Models](https://www.biorxiv.org/content/10.1101/2025.09.03.674085v1.abstract)** (*2025*) `bioRxiv`
  > 本文展示了 BioLab，这是一个多智能体系统，它集成了特定领域的基础模型和计算工具，以实现端到端生物学研究的自动化。BioLab 在生物医学推理基准测试中优于领先的大型语言模型，并自主执行复杂的流水线，包括带有实验验证的从头抗体设计。结果表明，原生 AI 多智能体框架能够紧密耦合计算和实验，以推动可扩展的科学发现。



- **[SleepBert: An Intelligent Clinical Encyclopaedia for Sleep Disorders Using Large Language Models](https://pmc.ncbi.nlm.nih.gov/articles/PMC12083639/)** (*2025*) `Research Square`
  > 本文介绍了 SleepBert，一种检索增强模型，将多导睡眠图结构化特征与非结构化的临床叙述相结合，以进行全面的睡眠障碍分析。通过微调 ClinicalBERT 并合并实时医学文献检索，SleepBert 实现了明显高于现有基线的诊断准确率。该系统支持可扩展且基于证据的复杂睡眠数据解释，以辅助临床决策和研究。



- **[Approximating facial expression effects on diagnostic accuracy via generative AI in medical genetics](https://academic.oup.com/bioinformatics/article/40/Supplement_1/i110/7700869)** (*2024*) `Bioinformatics`
  > 本研究探讨面部表情如何影响人工智能和人类利用面部图像诊断遗传综合征。深度学习模型和临床医生在个体微笑时，更有可能正确识别威廉姆斯综合征和安吉曼综合征，这揭示了与刻板表情相关的偏见，而在其他综合征中没有观察到这种影响。结果强调面部表情是一个重要的混杂因素，在人工智能驱动的基因组和临床诊断中应考虑和减轻这种因素。



- **[Can Large Language Models Democratize Access to Dual-use Biotechnology?](https://arxiv.org/abs/2306.03809)** (*2023*) `Arxiv`
  > 该研究表明，通过提供可操作的技术指导、材料采购和程序细节，大型语言模型聊天机器人能够快速指导非专家获取和开发具有引发大流行病潜力的病原体。研究结果凸显了当前 LLM 部署中的严重军民两用风险，表明这些模型可能会降低造成生物学危害的门槛。作者强调需要强有力的保护措施，包括第三方模型评估、数据集管理和全面的 DNA 合成筛选。




- **[Artificial Intelligence in Clinical Genetics](https://www.nature.com/articles/s41431-024-01782-w)** (*2025*) `European Journal of Human Genetics`
  > 本综述回顾了人工智能在临床遗传学领域的过去、现在和新兴应用，涵盖了诊断、患者管理、治疗和临床支持。它概述了主要 AI 类别，包括机器学习、深度学习和生成式 AI，并讨论了它们在遗传学实践中不断发展的作用。作者认为 AI 可能会极大地改变临床遗传学，并强调需要主动准备以平衡益处和风险。




- **[Advancing Healthcare: The Role and Impact of AI and Foundation Models](https://pmc.ncbi.nlm.nih.gov/articles/PMC11236664/)** (*2024*) `American Journal of Translational Research`
  > 本文回顾探讨了医疗保健领域基础人工智能模型的演变，强调了它们在影像、基因组学和决策支持等领域的诊断、医学干预和精准医学中日益增长的影响力。它讨论了生成式和传统人工智能模型的变革潜力，以及医疗保健系统中缓慢采用、伦理、偏见和治理的挑战。作者主张建立透明、公平和负责任的人工智能框架，包括通用医疗人工智能概念，以实现可扩展和负责任的医疗创新。



- **[Intuitive Human–Artificial Intelligence Theranostic Complementarity](https://www.liebertpub.com/doi/full/10.1089/cbr.2025.0021)** (*2025*) `Cancer Biotherapy & Radiopharmaceuticals`
  > 本文认为，虽然深度学习在放射学和核医学的放射组学和基于图像的分析中表现出色，但生成式人工智能在临床决策中的应用由于缺乏理解、判断力和同理心而受到根本的限制。作者强调人工智能应补充而非替代核医学医师，其直觉、责任感和以患者为中心的推理仍至关重要。提议一种协同的“人类-AI”方法以支持个性化并充满同理心的针对肿瘤的治疗诊断护理。



### 知识发现和假设生成

<!-- 
- **[Assessing the Performance of Generative Artificial Intelligence in Retrieving Information against Manually Curated Genetic and Genomic Data](https://academic.oup.com/database/article/doi/10.1093/database/baaf011/8019548)** (*2025*) `Database`
  > 论文提出 Foam - Agent，一种从自然语言自动化 CFD 工作流的多智能体框架。它具有独特的检索、文件生成和纠错系统，降低了专业知识的门槛。


- **[Characterization and Automated Classification of Sentences in the Biomedical Literature: A Case Study for Biocuration of Gene Expression and Protein Kinase Activity](https://pmc.ncbi.nlm.nih.gov/articles/PMC11741306)** (*2025*) `bioRxiv`
  > 论文提出 Foam - Agent，一种从自然语言自动化 CFD 工作流的多智能体框架。它具有独特的检索、文件生成和纠错系统，降低了专业知识的门槛。



- **[Generative Artificial Intelligence GPT-4 Accelerates Knowledge Mining and Machine Learning for Synthetic Biology](https://pubs.acs.org/doi/full/10.1021/acssynbio.3c00310)** (*2023*) `ACS synthetic biology`
  > 论文提出 Foam - Agent，一种从自然语言自动化 CFD 工作流的多智能体框架。它具有独特的检索、文件生成和纠错系统，降低了专业知识的门槛。


- **[Network for Knowledge Organization (NEKO): An AI Knowledge Mining Workflow for Synthetic Biology Research](https://www.sciencedirect.com/science/article/pii/S1096717624001484)** (*2025*) `Metabolic Engineering`
  > 论文提出 Foam - Agent，一种从自然语言自动化 CFD 工作流的多智能体框架。它具有独特的检索、文件生成和纠错系统，降低了专业知识的门槛。 -->


- **[Leveraging Generative AI to Assist Biocuration of Medical Actions for Rare Disease](https://academic.oup.com/bioinformaticsadvances/article/5/1/vbaf141/8160944)** (*2025*) `Bioinformatics Advances`
  > 本文介绍 AutoMAxO，一个半自动化框架，它使用大型语言模型来扩展罕见病医疗行动的生物管理。通过从文献中提取候选治疗方法，并在人工审查之前将它们与 MAxO、HPO 和 MONDO 本体论对齐，AutoMAxO 大大减少了手动管理负担。应用于 37 种罕见遗传病，该方法识别出数百种新的治疗注释，证明了 LLM 辅助管理在转化研究中的实用性。




- **[FAVOR-GPT: A Generative Natural Language Interface to Whole Genome Variant Functional Annotations](https://academic.oup.com/bioinformaticsadvances/article/4/1/vbae143/7789482)** (*2024*) `Bioinformatics Advances`
  > 本工作介绍了 FAVOR-GPT，这是一种检索增强生成接口，它将大型语言模型与 FAVOR 数据库集成，以支持解释全基因组变异注释。通过将复杂的功能注释转化为用户友好的摘要，FAVOR-GPT 提高了没有专门知识的研究人员的可访问性和可用性。结果表明，基于 RAG 的 LLM 接口可以有效增强基因组数据解释，同时保持高注释准确性。



- **[GP-GPT: Large Language Model for Gene-phenotype Mapping](https://arxiv.org/abs/2409.09825)** (*2024*) `arXiv`
  > 本工作介绍了 GP-GPT，这是一种专门的大型语言模型，在用于遗传-表型知识表示和关系分析的大规模基因组学、蛋白质组学和医学遗传学数据上进行微调。GP-GPT 在基因组学信息检索和关系确定任务上优于通用 LLM，展示了强大的特定领域理解力。结果表明，量身定制的 LLM 可以更有效地支持基因-表型研究和生物医学知识发现。




- **[SpatialAgent: An Autonomous AI Agent for Spatial Biology](https://www.biorxiv.org/content/10.1101/2025.04.03.646459v1.abstract)** (*2025*) `bioRxiv`
  > 本文介绍 SpatialAgent，这是一个完全自主的 AI 智能体，旨在通过将大型语言模型与自适应推理和动态工具使用相结合来支持端到端空间生物学研究。在大型人类和小鼠空间数据集上进行评估时，SpatialAgent 在关键任务上优于现有计算方法并达到或超过人类的表现。该研究展示了空间生物学中可扩展且协作的 AI 驱动发现的新范例。




- **[PCMR: A Comprehensive Precancerous Molecular Resource](https://www.nature.com/articles/s41597-025-04899-9)** (*2025*) `Scientific Data`
  > 本研究介绍了癌前分子资源 (PCMR)，这是一个大型综合数据库，汇编了各种癌症类型和组织的癌前病变的多组学分子特征。通过将差异分析与基于 ChatGPT 的文本挖掘相结合，PCMR 系统地识别了癌前病变与基因的关联，并验证了它们的生物学和临床相关性。该资源为研究早期致癌作用以及推进癌前病变研究和干预提供了全面的基础。



- **[Uncertainty-Aware Adaptation of Large Language Models for Protein-Protein Interaction Analysis](https://arxiv.org/abs/2502.06173)** (*2025*) `arXiv`
  > 本研究引入了一种不确定性感知的框架，使用微调的大型语言模型进行蛋白质-蛋白质相互作用预测。通过集成 LoRA 集合和用于不确定性量化的贝叶斯 LoRA，该方法提高了基于 LLM 的 PPI 分析在多种疾病环境下的可靠性和可重复性。研究结果强调了置信度感知建模对于 LLM 在精准医学和计算生物学中值得信赖应用的重要性。



- **[CRISPR-GPT for agentic automation of gene-editing experiments](https://www.nature.com/articles/s41551-025-01463-z)** (*2025*) `Nature Biomedical Engineering`
  > 这项工作介绍了 CRISPR-GPT，这是一个基于 LLM 的智能体系统，旨在支持端到端的 CRISPR 基因编辑实验设计和数据分析。通过整合领域知识、检索、外部工具和微调模型，CRISPR-GPT 协助实验规划、向导 RNA 设计、协议起草和结果解释。实验验证证明了它作为跨不同 CRISPR 模式的基因组工程 AI 副驾驶的有效性。




- **[MRAgent: An LLM-based Automated Agent for Causal Knowledge Discovery in Disease via Mendelian Randomization](https://academic.oup.com/bib/article/26/2/bbaf140/8107848)** (*2025*) `Briefings in Bioinformatics`
  > 本文介绍 MRAgent，这是一种基于 LLM 的自动化智能体，它通过自主地从文献中识别暴露-结果对并使用 GWAS 数据进行因果推断来促进大规模孟德尔随机化分析。通过减少对先验专家知识的依赖，MRAgent 简化了疾病研究中的因果发现，并通过自动和人工评估展示了端到端的工作流程。结果突出了由 LLM 驱动的智能体在复杂生物医学研究中推进因果分析的潜力。




- **[Evaluating GPT and BERT Models for Protein-Protein Interaction Identification in Biomedical Text](https://academic.oup.com/bioinformaticsadvances/article/4/1/vbae133/7755482)** (*2024*) `Bioinformatics Advances`
  > 本研究评估了基于 Transformer 的语言模型从生物医学文本中提取蛋白质-蛋白质相互作用的能力。双向编码器模型，尤其是 BioBERT，取得了最强的整体表现，而 GPT-4 尽管没有专门在生物医学语料库上接受训练，但表现出相当的精度和召回率。结果表明，大型语言模型可以有效支持从生物医学文献中自动挖掘 PPI。




- **[Generative Artificial Intelligence GPT-4 Accelerates Knowledge Mining and Machine Learning for Synthetic Biology](https://pubs.acs.org/doi/full/10.1021/acssynbio.3c00310)** (*2023*) `ACS synthetic biology`
  > 这项工作展示了基于 GPT-4 的提示工程如何简化从合成生物学文献中提取知识。通过对 176 篇关于产油酵母的出版物进行挖掘，作者将非结构化文本转换为结构化数据集，使机器学习模型能够准确预测发酵性能。结果表明，生成式 AI 可以显著减少手动管理工作，支持生物制造中的预测建模，并实现向研究较少的微生物系统的迁移学习。




- **[AI-driven Toolset for IPF and Aging Research Associates Lung Fibrosis with Accelerated Aging](https://www.biorxiv.org/content/10.1101/2025.01.09.632065v1.abstract)** (*2025*) `bioRxiv`
  > 本研究应用 AI 通过将路径感知的蛋白质组衰老时钟与特定领域语言模型 ipf-P3GPT 相结合，揭示特发性肺纤维化潜在的与衰老相关的机制。衰老时钟表现出很强的预测性能，并将加速衰老与严重的 COVID-19 联系起来，而分子分析表明 IPF 反映了失调的衰老途径，而不仅仅是衰老加速。这些结果强调了衰老生物学和 IPF 之间的新联系，并证明了 AI 引导策略研究年龄相关疾病的价值。




- **[Intuitive Human–Artificial Intelligence Theranostic Complementarity](https://www.liebertpub.com/doi/full/10.1089/cbr.2025.0021)** (*2025*) `Cancer Biotherapy & Radiopharmaceuticals`
  > 深度学习有潜力通过提供比人类更快、更可靠的图像分析来改变放射学和核医学，但生成式 AI 在临床决策中的作用仍然存在争议。AI 缺乏理解、判断和同理心，因此其输出必须由负责患者护理的核医学医生解释和应用。以互补的方式使用，AI 可以通过整合放射组学、基因组学和临床数据来支持精准诊疗，同时使医生能够专注于知情、以患者为中心的治疗决策。


### 分子和药物设计

- **[CancerGPT for few shot drug pair synergy prediction using large pretrained language models](https://www.nature.com/articles/s41746-024-01024-9)** (*2024*) `npj Digital Medicine`
  > 大型语言模型显示出强大的少样本学习能力，但它们泛化到复杂生物学问题的能力仍未得到充分探索。本研究提出了一种基于少样本 LLM 的方法，通过利用来自文本而非结构化数据的先验知识，预测罕见癌症组织中的药物对协同作用。跨七种罕见组织的实验表明，紧凑的 CancerGPT 模型在极少甚至没有样本的情况下实现了高准确度，其表现与经过微调的大得多的 GPT-3 模型相当。



- **[AutoPM3: Enhancing Variant Interpretation via LLM-driven PM3 Evidence Extraction from Scientific Literature](https://academic.oup.com/bioinformatics/advance-article-abstract/doi/10.1093/bioinformatics/btaf382/8178584)** (*2025*) `Bioinformatics`
  > 本文介绍 AutoPM3，这是一种自动化框架，可从生物医学文献中提取 ACMG/AMP PM3 变异证据以支持罕见病诊断。使用开源 LLM 结合基于 Text2SQL 的变异提取器和检索增强生成模块，AutoPM3 有效处理文本和表格。在最新策划的 PM3-Bench 数据集上评估，该方法实现了高准确率和召回率，优于依赖大型模型的方法。结果表明，开源 LLM 可以为基于文献的变异解释提供快速、经济高效且可扩展的解决方案。




- **[Generative Design of Functional Metal Complexes Utilizing the Internal Knowledge of Large Language Models](https://arxiv.org/abs/2410.18136)** (*2024*) `arXiv`
  > 设计过渡金属配合物涉及搜索巨大的化学空间，这限制了传统遗传算法的有效性。这项工作介绍了一种基于 LLM 驱动的进化优化框架，利用预训练的化学知识来指导单目标和多目标优化，而无需监督微调。所提出的方法有效地识别出性能最佳的配合物，支持灵活的自然语言驱动的优化，并展现出在化学和材料设计方面的强大潜力。




- **[Automatic Biomarker Discovery and Enrichment with BRAD](https://academic.oup.com/bioinformatics/article-abstract/41/5/btaf159/8125018)** (*2025*) `Bioinformatics`
  > 将大型语言模型与生物医学研究工具整合在透明度、可重复性和数据来源方面提出了挑战。本工作介绍 BRAD，这是一种基于智能体的系统，它将 LLM 与外部工具和数据库结合起来以自动化研究工作流，同时保持透明和可靠的协议。应用于生物标志物发现和其他任务，BRAD 实现了超过传统生物信息学工具的语境化解释和自动化。




- **[Can large language models democratize access to dual-use biotechnology?](https://arxiv.org/abs/2306.03809)** (*2023*) `arXiv`
  > 大型语言模型通过提供跨学科的可访问专业知识正在加速和民主化研究，但它们也面临着降低具有严重生物安全影响的军民两用技术门槛的风险。一项教育实验表明，通过最少的提示，聊天机器人就可以指导非专家完成与大流行病级病原体相关的关键步骤，这表明此类能力可能会被广泛获取。这些发现强调迫切需要保护措施，如第三方模型评估、训练数据的仔细管理以及全面的 DNA 合成筛选，以减轻滥用风险。



### 多组学分析


- **[Conversational AI agent for precision oncology: AI-HOPE-WNT integrates clinical and genomic data to investigate WNT pathway dysregulation in colorectal cancer](https://www.medrxiv.org/content/10.1101/2025.05.07.25327180.abstract)** (*2025*) `Frontiers in Artificial Intelligence`
  > AI-HOPE-WNT 是一款对话式 AI 智能体，旨在支持通过自然语言对整合的临床和基因组结直肠癌数据中 WNT 途径的失调进行分析。该系统准确地再现了关于 WNT 途径改变的已发表发现，同时揭示了与生存率、治疗反应、突变共现和特定人群风险相关的新关联。通过自动化复杂的生物信息学工作流程，AI-HOPE-WNT 降低了技术障碍，并为精准肿瘤学研究建立了一种针对特定通路的范例。




- **[BioDiscoveryAgent: An AI Agent for Designing Genetic Perturbation Experiments](https://arxiv.org/abs/2405.17631)** (*2024*) `arXiv`
  > BioDiscoveryAgent 是一种基于 LLM 的自主智能体，它通过推理生物学知识来设计和评估基因扰动实验，而不需要明确的优化目标或模型训练。在多个数据集上，它在识别相关基因和基因组合（包括具有挑战性的非必需扰动任务和未见数据）方面大大优于贝叶斯优化基线。通过整合文献检索、数据分析和自我批评，BioDiscoveryAgent 为闭环生物学实验设计提供了一种可解释且高效的范式。




- **[Exploring new drug treatment targets for immune related bone diseases using a multi omics joint analysis strategy](https://www.nature.com/articles/s41598-025-94053-7)** (*2025*) `Scientific Reports`
  > 这项研究应用了一个集成的多组学孟德尔随机化框架来识别免疫相关骨病的血浆蛋白因果靶点。通过结合 MR、SMR、贝叶斯共定位、LDSC 以及下游网络和药物分析，作者系统地揭示了类风湿性关节炎、多发性硬化症、银屑病关节炎和克罗恩病相关关节炎的疾病特异性治疗靶点。研究结果为这些疾病发病机制背后的关键蛋白质提供了强有力的遗传证据，并为免疫相关骨病中精准药物发现提供了坚实的基础。




- **[Multimodal cell maps as a foundation for structural and functional genomics](https://www.nature.com/articles/s41586-025-08878-3)** (*2025*) `Nature`
  > 本工作通过整合 5100 多种蛋白质的生物物理相互作用数据和免疫荧光成像，展示了全面的人类亚细胞结构图谱。使用自监督多模态学习和大型语言模型辅助的注释，该研究确定了数百种分子组装，揭示了新的蛋白质功能，解码了与癌症相关的改变，并为结构和功能细胞生物学研究提供了一个公共平台。



- **[PCMR: A Comprehensive Precancerous Molecular Resource](https://www.nature.com/articles/s41597-025-04899-9)** (*2025*) `Scientific Data`
  > 本研究介绍了 PCMR，这是一个全面、精心策划的资源，整合了来自 35 种癌症类型和 20 个组织的超过 25000 个癌前病变样本的多组学分子特征。通过将大规模组学数据与 ChatGPT 辅助文本挖掘相结合，PCMR 系统地绘制了癌前-基因关联，并验证了它们的生物学和临床相关性，为推进癌前病变研究和癌症早期干预提供了宝贵的基础。




- **[Using ChatGPT to predict the future of personalized medicine](https://www.nature.com/articles/s41397-023-00316-9)** (*2023*) `The Pharmacogenomics Journal`
  > 本研究探讨了 ChatGPT 在个性化医疗和药物基因组学未来的潜在作用，强调了向算法驱动、多组学信息的个体化治疗的转变。虽然 ChatGPT 预测它将在改善患者预后和改变临床决策方面产生巨大的好处，但它也承认了在广泛的临床应用之前必须解决的当前局限性。




- **[Generative Methods for Pediatric Genetics Education](https://pmc.ncbi.nlm.nih.gov/articles/PMC10543060/)** (*2023*) `medRxiv`
  > 本研究评估生成式 AI 创建的图像是否可以通过帮助儿科住院医师识别遗传综合征来支持医学教育。虽然 AI 生成图像的表现与真实图像相当，但它们被认为稍微不那么有帮助，真实图像仍然是首选的学习工具。研究结果表明，生成式 AI 图像可以作为一种有用的辅助工具，特别是在教授不太熟悉的遗传病时。




- **[Automated Bioinformatics Analysis via AutoBA](https://arxiv.org/abs/2309.03242)** (*2023*) `arXiv`
  > 这项工作介绍了 AutoBA，这是一个基于大型语言模型的自主智能体，可以在最少的用户输入下简化传统的组学数据分析。经专家生物信息学家的验证，AutoBA 展示了在不同数据模式下（包括 WGS、RNA-seq、单细胞、ChIP-seq 和空间转录组学）的强健性能和适应性，同时通过本地执行保护数据隐私。该系统动态设计分析工作流的能力突出了其作为预定义生物信息学管道灵活替代方案的潜力。




- **[PheNormGPT: a framework for extraction and normalization of key medical findings](https://academic.oup.com/database/article-abstract/doi/10.1093/database/baae103/7833209)** (*2024*) `Database`
  > This work introduces PheNormGPT, a large language model–based framework for extracting and normalizing phenotypic findings from unstructured clinical text to Human Phenotype Ontology concepts. Using fine-tuned GPT models and a novel adaptive few-shot selection strategy, PheNormGPT achieved state-of-the-art performance in the BioCreative VIII phenotype extraction challenge. The results demonstrate the effectiveness of LLM-driven approaches for accurate clinical phenotype normalization.



### 探索性应用


- **[Spatial transcriptomics AI agent charts hPSC-pancreas maturation in vivo](https://www.biorxiv.org/content/10.1101/2025.04.01.646731.abstract)** (*2025*) `bioRxiv`
  > 这项工作介绍了 STAgent，这是一种自主的多模态 AI 智能体，它将大型语言模型与专用计算工具相集成，以自动化复杂的空间转录组学分析。应用于人类干细胞衍生的胰腺组织，STAgent 迅速揭示了空间成熟模式、细胞间相互作用和潜在的生物学机制，同时结合相关文献对发现进行情境化。结果展示了一种新的智能范例，可显着减少空间生物学研究中的分析时间和专业知识障碍。




- **[SeqMate: A Novel Large Language Model Pipeline for Automating RNA Sequencing](https://arxiv.org/abs/2407.03381)** (*2024*) `arXiv`
  > 这项工作介绍了 SeqMate，这是一个由大型语言模型驱动的工具，可让非专业用户一键式进行 RNA-seq 和单细胞 RNA-seq 分析。通过自动化数据准备、下游分析和带有文献链接报告的结果解释，SeqMate 消除了命令行管道固有的技术障碍，并降低了生物数据分析的入门门槛。



- **[SteLLA: A Structured Grading System Using LLMs with RAG](https://ieeexplore.ieee.org/abstract/document/10825385/)** (*2024*) `IEEE Big Data`
  > 本工作引入了 SteLLA，这是一个结构化评分框架，它将检索增强生成与大型语言模型相结合，以提高自动简答题评分的可靠性。通过在讲师提供的参考答案和量规的基础上进行评估，SteLLA 实现了与人类评分者的高度一致性，同时产生详细的、逐点的评分和反馈。分析表明，LLM 可以准确地捕捉事实内容，但可能会过度推断含义，从而为教育评估的安全有效部署提供见解。



- **[Explaining Genetic Programming Trees using Large Language Models](https://arxiv.org/abs/2403.03397)** (*2024*) `arXiv`
  > 本研究引入了 GP4NLDR，这是一个可解释的 AI 框架，它将基于遗传编程的非线性降维与由大型语言模型驱动的聊天机器人相结合。通过将 XAI 仪表板与 LLM 生成的解释相结合，该系统提供了高维数据转换的直观、以用户为中心的解释。结果展示了 LLM 在增强遗传编程方法的可解释性和可用性方面的潜力。



- **[Enhancing phenotype recognition in clinical notes using large language models: PhenoBCBERT and PhenoGPT](https://www.cell.com/patterns/fulltext/S2666-3899(23)00288-X)** (*2023*) `Patterns`
  > 本研究开发了 PhenoBCBERT 和 PhenoGPT，这两种基于大型语言模型的方法通过扩展人类表型本体词汇来自动识别临床记录中的表型。这些模型通过识别更广泛和更细微的表型概念（包括以前未表征的术语），优于传统的基于规则的工具，并在临床文本和生物医学文献中表现出强大的性能。这些结果强调了调整通用 LLM 进行特定领域临床和遗传学研究的有效性。




- **[A Comprehensive Survey of Foundation Models in Medicine](https://ieeexplore.ieee.org/abstract/document/10847310)** (*2025*) `IEEE Reviews in Biomedical Engineering`
  > 本综述全面回顾了医学领域的基础模型 (FM)，涵盖了它们的演变、学习策略、旗舰模型、应用以及在医疗保健领域的挑战。它系统地探讨了 BERT 和 GPT 等模型如何转变临床 NLP、医学影像和组学研究，并提出了启用 FM 的医疗应用的详细分类。该调查还讨论了关键的局限性、未决的研究问题以及为支持在医疗保健中负责任和有效地部署 FM 所汲取的教训。



- **[Regulatory barriers to USChina collaboration for generative AI development in genomic research](https://www.cell.com/cell-genomics/fulltext/S2666-979X(24)00130-7)** (*2024*) `Cell Genomics`
  > 本文分析了中美监管框架如何在基因组研究的生成式 AI 开发中制造合作障碍，特别是在数据共享、安全和合规性方面。它强调了两国创新与监管之间的紧张关系，并认为不一致的法律要求阻碍了负责任的国际合作。作者建议更新和更新双边科技协议，以促进人类基因组数据透明、合乎道德和安全的共享。




## 2. 系统架构

### 单智能体系统


- **[VarChat: the generative AI assistant for the interpretation of human genomic variations](https://academic.oup.com/bioinformatics/article-abstract/40/4/btae183/7641533)** (*2024*) `Bioinformatics`
  > 这项工作介绍了 VarChat，这是一种基于生成式 AI 的工具，旨在应对在快速扩张的科学文献中不断增长的基因组变异解释挑战。VarChat 自动识别、综合和总结与变异相关的研究，生成简洁的、具有临床相关性的描述，将基因变异与蛋白质功能和健康结果联系起来，同时提供可追溯的参考。通过简化文献审查和解释，VarChat 有助于将零碎的基因组知识转化为研究人员和临床医生可操作的见解。




- **[MEGA-GPT: Artificial Intelligence Guidance and Building Analytical Protocols Using MEGA Software](https://academic.oup.com/mbe/article-abstract/42/6/msaf101/8157534)** (*2025*) `Molecular Biology and Evolution`
  > 本研究介绍了 MEGA-GPT，这是一个检索增强的、由人工智能驱动的助手，旨在通过自然语言查询帮助用户导航 MEGA 进化遗传学软件日益复杂的功能。通过整合 MEGA 文档和特定版本的资源，MEGA-GPT 提供循序渐进的指导，澄清分析设置，并推荐最佳工作流程，同时与标准 ChatGPT 相比显着减少了幻觉。该工具提高了新手和经验丰富用户的可用性，并展示了定制的基于 RAG 的助手如何增强复杂的科学软件。




- **[MedBioLM: Optimizing Medical and Biological QA with Fine-Tuned Large Language Models and Retrieval-Augmented Generation](https://arxiv.org/abs/2502.03004)** (*2025*) `arXiv`
  > 本工作提出了 **MedBioLM**，这是一种领域适应性生物医学问答模型，它将微调与检索增强生成相结合，以提高医学和生物学查询中的事实准确性、推理能力和上下文深度。在不同的生物医学 QA 基准上进行评估，MedBioLM 显示微调带来了大幅的准确率提升，并且通过 RAG 提高了事实一致性。结果证明了领域优化 LLM 在生物医学研究、教育和临床决策支持方面的潜力。




- **[Evolution of publicly available large language models for complex decision-making in breast cancer care](https://link.springer.com/article/10.1007/s00404-024-07565-4)** (*2024*) `Archives of Gynecology and Obstetrics`
  > 本研究将五种公开可用的大型语言模型（GPT-4、GPT-3.5 变体、Llama2 和 Bard）针对复杂乳腺癌病例的治疗建议与多学科肿瘤委员会的建议进行了比较。GPT-4 显示出最高的一致性，特别是对于浸润性乳腺癌和放射治疗决策，而所有模型在基因检测建议方面表现都很差。总体而言，研究结果表明当前的 LLM 尚不足以可靠地用于乳腺癌护理的安全临床使用，这突出表明需要改进提示策略、数据控制和进一步的临床验证。




- **[Survey and Improvement Strategies for Gene Prioritization with Large Language Models](https://academic.oup.com/bioinformaticsadvances/advance-article-abstract/doi/10.1093/bioadv/vbaf148/8172498)** (*2025*) `Bioinformatics Advances`
  > 本研究以大型语言模型作为罕见病诊断中基因优先级排序的基准，以解决有限数据和大型候选基因集带来的挑战。使用多智能体策略、基于人类表型本体论的病例分层以及分而治之的排名框架，GPT-4 在识别致病基因方面始终优于其他模型，同时减轻了位置和文献偏见。尽管仍然存在对充分研究的基因的偏见和输入顺序敏感性，但所提出的框架显着提高了罕见遗传病的诊断效率。




<!-- - **[Large Language Model Agent as a Mechanical Designer](https://arxiv.org/abs/2404.17525)** (*2024*) `arXiv`
  > 这项工作提出了一种自主的机械设计框架，该框架将预训练的大型语言模型与有限元法 (FEM) 分析相结合，以迭代生成、评估和改进结构设计，而无需特定领域的微调。使用 2D 桁架结构作为测试平台，LLM 有效地导航离散的、多目标的设计空间，并比 NSGA-II 以更少的 FEM 评估实现更快的收敛。结果表明，基于推理的、语言驱动的 LLM 可以作为自主结构设计和迭代细化的有效优化器。 -->



- **[Benchmarking Large Language Models for Predictive Modeling in Biomedical Research With a Focus on Reproductive Health](https://pmc.ncbi.nlm.nih.gov/articles/PMC12312170/)** (*2025*) `bioRxiv`
  > 本研究使用来自生殖健康领域的多个 DREAM 挑战的标准化组学数据集，评估了大型语言模型 (LLM) 在预测建模任务中自动生成 R 和 Python 代码的能力。几个 LLM 成功生成了可执行的分析管道，其中 OpenAI 的 o3-mini-high 表现最佳，并且获得了与顶尖 DREAM 挑战团队相当或超过的测试表现。结果表明，LLM 可以有效地自动化基于组学的预测建模的关键步骤，降低技术障碍并加速探索性生物医学研究。



- **[Comprehensive molecular analyses of an autoimmune-related gene predictive model and immune infiltrations using machine learning methods in intracranial aneurysma](https://www.frontiersin.org/journals/immunology/articles/10.3389/fimmu.2025.1531930/full)** (*2025*) `Frontiers in Immunology`
  > This study investigates the genetic links between autoimmune processes and intracranial aneurysm (IA) by integrating transcriptomic data, functional enrichment analyses, and multiple machine-learning approaches. Two key autoimmune-related diagnostic genes, ADIPOQ and IL21R, were identified and used to build a neural-network model with strong predictive performance (AUC = 0.944). The results highlight immune infiltration and gene–miRNA–drug regulatory networks as important contributors to IA pathogenesis, suggesting potential therapeutic targets.



### 多智能体系统

- **[CellAgent: An LLM-driven MultiAgent Framework for Automated Single-cell Data Analysis](https://arxiv.org/abs/2407.09811)** (*2024*) `bioRxiv`
  > 本文介绍了 CellAgent，这是一个由 LLM 驱动的多智能体框架，它通过协调计划者、执行者和评估者智能体进行分层决策和自我迭代优化，实现单细胞 RNA-seq 数据分析的全自动化。CellAgent 自主选择合适的工具和超参数，执行端到端的分析，并在没有人工干预的情况下评估结果。跨不同组织和细胞类型的基准测试表明，CellAgent 实现了稳健、高质量的性能，同时大大减少了分析师的工作量，推进了“科学智能体”的范例。




- **[Autonomous chemical research with large language models](https://www.nature.com/articles/s41586-023-06792-0)** (*2023*) `Nature`
  > 本文介绍了 Coscientist，这是一个由 GPT-4 驱动的人工智能系统，它通过将大型语言模型与文献检索、代码执行和实验自动化工具相集成，自主设计、规划和执行复杂的科学实验。在六个具有代表性的任务（包括钯催化反应优化）中，Coscientist 在半自主实验设计、执行和推理方面展示了强大的能力。这些结果突出了由 LLM 驱动的人工智能系统在加速科学发现方面的多功能性、有效性和可解释性。




- **[Steering veridical large language model analyses by correcting and enriching generated database queries: first steps toward ChatGPT bioinformatics](https://academic.oup.com/bib/article-abstract/26/1/bbaf045/8002976)** (*2024*) `Briefings in Bioinformatics`
  > 本文探讨了使用原版 ChatGPT 作为生物信息学助手的局限性，强调了科学领域中由知识不完整、数据检索不佳和幻觉引起的错误。为了解决这些问题，作者引入了 NagGPT，这是一个位于 LLM 和基因组学数据库之间的中间件，用于验证、纠正和调解 LLM 生成的查询，同时用权威、最新的数据引导响应。与生成和执行 Python 代码的定制 GPT 配对，该系统支持跨主要基因组学数据库的动态检索和分析。结果展示了提高事实准确性、减少幻觉以及提高未修改的 LLM 在生物信息学任务中的可靠性的实用方法。




- **[CRISPR-GPT for agentic automation of gene-editing experiments](https://www.nature.com/articles/s41551-025-01463-z)** (*2025*) `Nature Biomedical Engineering`
  > 这项工作介绍了 CRISPR-GPT，这是一个基于 LLM 的智能体系统，旨在支持端到端的 CRISPR 基因编辑实验设计和数据分析。通过整合领域知识、检索、外部工具和微调模型，CRISPR-GPT 协助实验规划、向导 RNA 设计、协议起草和结果解释。实验验证证明了它作为跨不同 CRISPR 模式的基因组工程 AI 副驾驶的有效性。




### 神经符号整合

- **[Tokensome: Towards a Genetic Vision-Language GPT for Explainable and Cognitive Karyotyping](https://arxiv.org/abs/2403.11073)** (*2024*) `arXiv`
  > 本文认为，现有的自动核型分析方法局限于将任务纯粹视为视觉对象识别，而忽略了临床使用所需的整体信息和可解释性。作者引入了 Tokensome，这是一种视觉语言模型，通过标记化表示染色体，以实现可解释的、认知驱动的核型分析。通过将分析从视觉感知提升到认知决策，Tokensome 通过知识图谱和 LLM 整合了领域知识和推理。这种方法提高了可解释性并增强了对染色体异常的检测。




- **[Leveraging Generative AI to Assist Biocuration of Medical Actions for Rare Disease](https://academic.oup.com/bioinformaticsadvances/article/5/1/vbaf141/8160944)** (*2025*) `Bioinformatics Advances`
  > 本文介绍了 AutoMAxO，这是一种基于 LLM 的半自动化工作流程，旨在扩大罕见病医疗行动本体 (MAxO) 的生物管理，以解决手动管理的局限性。该系统使用 LLM 从文献摘要中提取候选治疗和医疗行动注释，然后通过后处理和人在循环验证将它们与 MAxO、HPO 和 MONDO 本体术语对齐。应用于涵盖 37 种罕见遗传病的摘要，AutoMAxO 确定了 958 个并入 MAxO 数据集的新治疗注释。结果表明，LLM 辅助管理可以大幅提高临床本体开发的覆盖率和效率。




- **[Assessing large language model performance related to aging in genetic conditions](https://www.nature.com/articles/s41514-025-00226-z)** (*2025*) `npj Aging`
  > 本研究评估大型语言模型（Llama-2-70B-chat 和 GPT-3.5）是否能够为 282 种遗传病的儿科和成人表现生成合理的临床小插曲、医患对话和管理计划。临床医生评分显示，这两种模型通常都能产生适合年龄的描述，在疾病表现方面具有良好的正确性和完整性，包括新生儿发病的代谢紊乱。然而，两种模型在生成管理计划时表现都明显较差，正确性和完整性仅为中等。这些发现表明，虽然 LLM 可以捕捉与年龄相关的临床特征，但它们在临床决策和管理方面的可靠性仍然有限。




- **[Using ChatGPT to predict the future of personalized medicine](https://www.nature.com/articles/s41397-023-00316-9)** (*2023*) `The Pharmacogenomics Journal`
  > 这项研究探讨了 ChatGPT 在讨论个性化医学和药物基因组学的未来方面的作用，这些领域旨在根据个体遗传和分子图谱量身定制治疗方法。通过向 ChatGPT 询问这些领域，作者发现该模型将它们描绘成有前景的方法，具有通过算法驱动的个性化治疗改善患者预后的强大潜力。然而，这些回答也凸显了当前的局限性和挑战，必须在临床实践中充分实现这种由 AI 引导的个性化之前解决这些问题。



## 3. 评估策略

- **[Exploring new drug treatment targets for immune related bone diseases using a multi omics joint analysis strategy](https://www.nature.com/articles/s41598-025-94053-7)** (*2025*) `Scientific Reports`

  > 这项研究应用了一个联合多组学分析框架来识别免疫相关骨病的新治疗靶点。通过整合异构分子数据集，这项工作提供了有关疾病机制的系统级视角，并突出了用于药物发现的候选途径。



- **[Survey and Improvement Strategies for Gene Prioritization with Large Language Models](https://academic.oup.com/bioinformaticsadvances/advance-article-abstract/doi/10.1093/bioadv/vbaf148/8172498)** (*2025*) `Bioinformatics Advances`

  > 本文以大型语言模型作为罕见疾病诊断中致病基因优先级排序的基准。它引入了表型感知的多智能体和分而治之策略，以减轻偏见、可扩展性问题和输入敏感性，证明了比基线 LLM 方法更高的准确性。



- **[Genetic Analysis of Milk Citrate Predicted by Milk Mid-infrared Spectra of Holstein Cows in Early Lactation](https://www.sciencedirect.com/science/article/pii/S0022030223008263)** (*2023*) `Journal of Dairy Science`

  > 该研究使用大规模中红外光谱预测和单步 GWAS 调查了牛奶柠檬酸盐（奶牛能量负平衡的早期生物标志物）的遗传结构。结果显示出高遗传力并确定了与基因组选择相关的关键基因组区域和候选基因。



- **[GOLF: A Generative AI Framework for Pathogenicity Prediction of Myocilin OLF Variants](https://pmc.ncbi.nlm.nih.gov/articles/PMC12262641/)** (*2025*) `bioRxiv`

  > 这项工作介绍了 GOLF，这是一种生成式 AI 框架，用于预测和解释与青光眼相关的 MYOC OLF 结构域变异的致病性。通过将生成模型与稀疏自动编码器相结合，该框架实现了准确的分类，同时揭示了驱动预测的潜在生化特征。



- **[Genome-Wide Association Study of Lactation Traits in Chinese Holstein Cows in Southern China](https://www.mdpi.com/2076-2615/13/15/2545)** (*2023*) `Animals`

  > 这项全基因组关联研究确定了与在高温和高湿条件下饲养的中国荷斯坦奶牛泌乳性状相关的 SNP 和候选基因。研究结果提供了遗传见解，以支持适应具有挑战性的环境压力的育种计划。



- **[Hematological and Biochemical Characterization of Aging Farm Male Rat Strains in the National Center for Geriatrics and Gerontology](https://www.jstage.jst.go.jp/article/expanim/74/1/74_24-0028/_article/-char/ja/)** (*2024*) `Experimental Animals`

  > 该论文描述了三种常用雄性大鼠品系中与年龄相关的血液学和生化变化。它强调了与衰老和老年学研究相关的品系特异性生理差异，强调了实验设计中品系选择的重要性。



- **[Ten Quick Tips for Harnessing the Power of ChatGPT/GPT-4 in Computational Biology](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1011319)** (*2023*) `PLoS Computational Biology `

  > 本文提供了十条在计算生物学工作流中使用 ChatGPT 和 GPT-4 的实用指南，涵盖代码生成、数据分析、科学写作和提示工程。它讨论了生物信息学应用程序的生产力提高和伦理考虑。



- **[Large Language Models as Efficient Reward Function Searchers for Custom-Environment Multi-Objective Reinforcement Learning](https://arxiv.org/abs/2409.02428)** (*2024*) `Arxiv`

  > 本文提出了 ERFSL，这是一个利用大型语言模型为复杂的自定义环境多目标强化学习任务搜索和完善奖励函数的框架。通过将 LLM 驱动的语义推理与进化策略相结合，该方法实现了高效的零样本奖励设计。



- **[Influence of the Concentrate Inclusion Level in a Grass Silage–based Diet on Hepatic Transcriptomic Profiles in Holstein-Friesian Dairy Cows in Early Lactation](https://www.sciencedirect.com/science/article/pii/S0022030223003764)** (*2023*) `Journal of Dairy Science`

  > This study analyzes how different concentrate levels in early-lactation diets affect hepatic transcriptomic responses in dairy cows. Results reveal parity-specific metabolic and inflammatory responses, offering insights into nutritional strategies for mitigating negative energy balance.



- **[Benchmarking Large Language Models for Predictive Modeling in Biomedical Research With a Focus on Reproductive Health](https://pmc.ncbi.nlm.nih.gov/articles/PMC12312170/)** (*2025*) `bioRxiv`

  > The authors benchmark multiple large language models for automated code generation in biomedical predictive modeling using DREAM challenge datasets. The study demonstrates that top-performing LLMs can match or exceed expert-designed models, particularly in standardized omics analyses.



- **[Bridging the Early Science Gap with Artificial Intelligence: Evaluating Large Language Models as Tools for Early Childhood Science Education](https://dl.acm.org/doi/full/10.1145/3706599.3721261)** (*2025*) `CHI EA`

  > This paper evaluates the ability of leading large language models to generate preschool-appropriate science explanations. Through expert teacher assessments, it highlights both the promise and limitations of LLMs in supporting early childhood science education.



- **[Leveraging Large Language Models for Decision Support in Personalized Oncology](https://jamanetwork.com/journals/jamanetworkopen/article-abstract/2812097)** (*2023*) `JAMA Network Open`

  > The study explores the use of conversational large language models to assist clinical decision-making in precision oncology. It discusses the potential of LLMs to support interpretation of complex biomarkers and streamline access to prior biomedical knowledge.



- **[Evaluating the Use of Generative Artificial Intelligence to Support Genetic Counseling for Rare Diseases](https://www.mdpi.com/2075-4418/15/6/672)** (*2025*) `Diagnostics`

  > This work assesses the accuracy and safety of multiple generative AI models in answering rare disease–related questions relevant to genetic counseling. While overall performance is strong, the study highlights risks of misinformation and the need for expert oversight.



- **[Leveraging Generative AI to Accelerate Biocuration of Medical Actions for Rare Disease](https://pmc.ncbi.nlm.nih.gov/articles/PMC11370550/)** (*2024*) `medRxiv`

  > The paper presents AutoMAxO, a semi-automated LLM-based workflow for scaling biocuration of medical actions in rare diseases. By combining AI-driven extraction with ontology alignment and human validation, the approach significantly accelerates structured knowledge curation.



- **[Importance of Prior Patient Interactions With the Healthcare System to Engaging With Pretest Cancer Genetic Services via Digital Health Tools](https://onlinelibrary.wiley.com/doi/abs/10.1111/1475-6773.14652)** (*2025*) `Health Services Research`

  > This randomized trial examines how prior healthcare system engagement influences patient uptake of digital tools for cancer genetic services. Findings suggest that existing patient-system interactions are key predictors of engagement with genetic testing workflows.



- **[Comparison of the Performance of Five Generative Artificial Intelligence Models on a Medical Molecular Biology Examination](https://www.cureus.com/articles/358057-comparison-of-the-performance-of-five-generative-artificial-intelligence-models-on-a-medical-molecular-biology-examination.pdf)** (*2025*) `Cureus`

  > This study compares the performance of five Chinese generative AI models on a medical molecular biology exam. Results show that several models outperform undergraduate students, while underscoring the need for critical evaluation and domain-specific AI systems in education.

## 4. 交互模式

- **[ChIP-GPT: a managed large language model for robust data extraction from biomedical database records](https://academic.oup.com/bib/article/25/2/bbad535/7600389)** (*2024*) `Briefings in Bioinformatics`

  > ChIP-GPT 提出了一种经过微调的 LLM 系统，用于从生物医学数据库中进行可扩展且稳健的元数据提取。通过迭代地提示定制的 GPT 模型，该框架准确地从嘈杂或不完整的记录中提取 ChIP-seq 靶标和细胞系，从而能够对大规模数据库条目进行专家级的推理。

- **[OpenAI o1-Preview vs. ChatGPT in Healthcare: A New Frontier in Medical AI Reasoning](https://www.cureus.com/articles/301598-openai-o1-preview-vs-chatgpt-in-healthcare-a-new-frontier-in-medical-ai-reasoning.pdf)** (*2024*) `Cureus`

  > 本社论比较了 OpenAI o1-Preview 与 ChatGPT-4 在医疗保健应用中的作用，强调了推理能力的进步及其对临床决策支持的影响。这项工作讨论了下一代生成式 AI 模型在医学推理环境中的机遇和局限性。

- **[Leveraging large language models for data analysis automation](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0317084)** (*2023*) `bioRxiv`

  > 本文介绍了 *mergen*，这是一个基于 R 的系统，它使用 LLM 根据自然语言描述自动化数据分析工作流。该框架结合了提示工程、执行反馈和工作流自动化，使非专家能够执行复杂的生物数据分析，同时暴露了 LLM 生成代码的当前局限性。

- **[GeneGPT: augmenting large language models with domain tools for improved access to biomedical information](https://academic.oup.com/bioinformatics/article-abstract/40/2/btae075/7606338)** (*2024*) `Bioinformatics`

  > GeneGPT 使用 NCBI Web API 增强大型语言模型，以提高事实准确性并减少基因组学问答中的幻觉。通过结合上下文学习和增强解码来实现结构化的 API 调用，GeneGPT 在 GeneTuring 基准测试中实现了最先进的性能，并支持多跳生物医学推理。

- **[Assessing the Utility of Large Language Models for Phenotype-Driven Gene Prioritization in Rare Genetic Disorder Diagnosis](https://www.cell.com/ajhg/fulltext/S0002-9297(24)00296-9)** (*2024*) `arXiv`

  > 本研究评估了大型语言模型在罕见病诊断中由表型驱动的基因优先排序的有效性。通过跨模型、提示和输入格式的系统基准测试，结果表明当前的 LLM 落后于传统的生物信息学工具，同时揭示了与临床整合相关的偏见和局限性。

- **[Evaluating the Symbol Binding Ability of Large Language Models for Multiple-Choice Questions in Vietnamese General Education](https://doi.org/10.1145/3628797.3628837)** (*2023*) `ACM`

  > 本工作使用新构建的基于 LaTeX 的数据集评估了 LLM 在越南语多项选择题上的符号绑定能力。该研究评估了几个模型从零样本至少样本的表现，提供了在严格的输出约束下推理效率和多语言评估的见解。

- **[CancerGPT for few shot drug pair synergy prediction using large pretrained language models](https://www.nature.com/articles/s41746-024-01024-9)** (*2024*) `npj Digital Medicine`

  > CancerGPT 提出了一种基于少样本 LLM 的框架，用于在数据有限的罕见癌症中预测药物对协同作用。通过利用预训练语言模型提取生物医学先验，该方法实现了与大得多的模型相比具有竞争力的性能，证明了在数据稀缺情况下数据驱动的生物推理的可行性。

- **[Enhancing phenotype recognition in clinical notes using large language models: PhenoBCBERT and PhenoGPT](https://www.cell.com/patterns/fulltext/S2666-3899(23)00288-X)** (*2023*) `Patterns`

  > 本文介绍了 PhenoBCBERT 和 PhenoGPT，这是两种基于 LLM 的模型，用于临床文本中的自动化表型识别。通过将人类表型本体覆盖范围扩展到基于规则的方法之外，这些模型改进了对已知和新的表型概念的检测，支持下游遗传病分析。

- **[A comparative evaluation of ChatGPT 3.5 and ChatGPT 4 in responses to selected genetics questions](https://academic.oup.com/jamia/article/31/10/2271/7693164)** (*2024*) `JAMIA`

  > 本研究比较了 ChatGPT-3.5 和 GPT-4 在回答遗传学相关问题时的表现，重点关注准确性、局限性和伦理考虑。分析突出了 GPT-4 的改进，同时强调了在医学遗传学环境中部署生成模型的风险和限制。

- **[Improving drug repositioning with negative data labeling using large language models](https://link.springer.com/article/10.1186/s13321-025-00962-0)** (*2025*) `Journal of Cheminformatics`

  > 本工作提出了一种 LLM 驱动的策略，从临床试验数据中识别真正的阴性候选药物，解决了有监督药物重新定位中的一个关键瓶颈。通过使用 GPT-4 标记失败的药物，该方法显着提高了预测准确性，并实现了大规模、数据驱动的药物再利用。

- **[Assessing the performance of generative artificial intelligence in retrieving information against manually curated genetic and genomic data](https://academic.oup.com/database/article-abstract/doi/10.1093/database/baaf011/8019548)** (*2025*) `Database`

  > 本研究将 GPT-3.5 和 GPT-4 的性能与用于遗传特征和 QTL 提取的专业人工管理进行了基准测试。结果表明，GPT-4 在文档分类和特征检索方面实现了高精度，支持生物数据库的混合人机管理范式。

- **[Intuitive Human–Artificial Intelligence Theranostic Complementarity](https://www.liebertpub.com/doi/abs/10.1089/cbr.2025.0021)** (*2025*) `Cancer Biotherapy and Radiopharmaceuticals`

  > 本文主张在治疗诊断核医学中，生成式 AI 和人类临床医生之间应发挥互补作用。它强调，虽然 AI 擅长统计推断，但人类的直觉、责任感和同理心对于个性化癌症治疗决策仍然至关重要。

- **[Giving AI Personalities Leads to More Human-Like Reasoning](https://arxiv.org/abs/2502.14155)** (*2025*) `arXiv`

  > This paper explores personality-based prompting as a mechanism to capture the diversity of human reasoning in LLMs. By combining psychological personality models with genetic algorithms, the approach enables LLMs to approximate human response distributions across intuitive and deliberative reasoning tasks.


## 5. 资源整合


### 知识增强智能体

- **[ChatGPT for phenotypes extraction: one model to rule them all?](https://ieeexplore.ieee.org/abstract/document/10340611/)** (*2023*) `IEEE EMBC`
  > 本研究探讨大型语言模型 (LLM) 是否能够捕捉全方位的人类推理，包括快速、直觉的系统 1 和缓慢、深思熟虑的系统 2 过程。使用通用的自然语言推理任务和众包的人类反应分布，作者评估了 LLM 复制不仅是多数答案，而且是人类判断的全部多样性的能力。他们引入了受大五人格模型启发的基于人格的提示，通过遗传算法进行优化，以从 LLM 中引出不同的推理风格。结果表明，这种方法显着改善了与人类反应分布的对齐，开源模型优于专有模型，表明对个性和次优推理进行建模是实现更类人 AI 认知的关键。




- **[Boosting GPT Models for Genomics Analysis: Generating Trusted Genetic Variant Annotations and Interpretations through RAG and fine-tuning](https://academic.oup.com/bioinformaticsadvances/article-abstract/5/1/vbaf019/8002096)** (*2025*) `Bioinformatics Advances`
  > 本研究旨在通过使用检索增强生成 (RAG) 和微调结合大规模变异注释数据，提高基因组学中大型语言模型的性能。通过将来自五个主要数据集的 1.9 亿个精心策划的变异注释整合到 GPT-4o 中，该系统能够进行准确、有推理支持的变异查询和解释。结果表明，虽然微调改善了某些注释字段的性能，但在注入事实基因组知识的可扩展性、准确性和成本效率方面，RAG 总体上更有效。这项工作证明了 LLM 作为一种可访问且高效的工具在变异解释和专业基因组学应用中的潜力。




- **[Bioinformatics and biomedical informatics with ChatGPT: Year one review](https://onlinelibrary.wiley.com/doi/abs/10.1002/qub2.67)** (*2024*) `Quantitative Biology`
  > 这篇综述回顾了 2023 年 ChatGPT 在生物信息学和生物医学信息学应用中的快速扩展。它涵盖了广泛的领域，包括组学和遗传学、生物医学文本挖掘、药物发现、图像理解、生物信息学编程和教育。作者分析了 ChatGPT 在这些领域中的优势和局限性，并讨论了主要挑战。该调查还概述了大型语言模型在生物信息学中未来发展的有前途的方向。




- **[Benchmarking Large Language Models for Replication of Guideline-Based PGx Recommendations](https://www.nature.com/articles/s41397-025-00383-0)** (*2025*) `Research Square`
  > 本研究评估大型语言模型在多大程度上能够生成符合 CPIC 指南且在临床上准确的药物基因组学 (PGx) 建议。使用 599 个精选的基因-药物-表型场景和一个新的经过专家验证的语义指标 (LLM Score)，作者表明通用 LLM 经常产生不完整或不安全的建议。相比之下，一个领域适应的、微调的模型获得了好得多的准确性 (LLM Score = 0.92) 和更快的推理。结果强调，对于安全、有效的人工智能驱动的个性化医疗，微调和结构化提示比单纯的模型规模更关键。




- **[Leveraging Generative AI to Assist Biocuration of Medical Actions for Rare Disease](https://academic.oup.com/bioinformaticsadvances/article/5/1/vbaf141/8160944)** (*2025*) `Bioinformatics Advances`
  > 本文介绍 AutoMAxO，这是一种基于 LLM 的半自动化工作流，旨在扩展罕见病医疗行动本体 (MAxO) 的生物管理，以解决手动注释的局限性。AutoMAxO 使用 LLM 从文献摘要中提取候选治疗和医疗行动信息，并通过后处理将它们与 MAxO、HPO 和 MONDO 本体术语对齐。整理后的结果呈现给人类专家进行验证，以确保准确性和可靠性。该系统应用于 37 种罕见遗传病，识别了 958 种新的治疗注释，证明了 LLM 辅助的生物管理在扩展临床知识库方面的有效性。




- **[Change of Heart: Can Artificial Intelligence Transform Infective Endocarditis Management?](https://pmc.ncbi.nlm.nih.gov/articles/PMC12030482/)** (*2025*) `Pathogens`
  > 这篇综述总结了人工智能如何越来越多地应用于感染性心内膜炎这种临床复杂且高发病率疾病的诊断和管理。与传统方法相比，机器学习模型和人工智能增强的成像及微生物学技术在诊断、风险分层、病原体鉴定和结果预测方面显示出更高的准确性。尽管这些结果很有希望，但在数据可用性、可解释性、伦理和临床验证方面仍然存在挑战。作者得出的结论是，包括作为决策支持工具的生成式 AI 在内，精心整合和验证的 AI 可以显着改善感染性心内膜炎护理中的患者结果和安全性。




- **[Improving Automated Deep Phenotyping Through Large Language Models Using Retrieval Augmented Generation](https://link.springer.com/article/10.1186/s13073-025-01521-w)** (*2024*) `medRxiv`
  > 本文介绍 RAG-HPO，这是一种检索增强生成工具，可改进从临床文本中自动提取和分配人类表型本体 (HPO) 术语的过程。通过将基于 LLM 的短语提取与来自表型-HPO 映射的大型向量数据库的实时检索相结合，RAG-HPO 减少了幻觉并避免了昂贵的微调。在 112 份罕见疾病病例报告的评估中，它在准确率、召回率和 F1 分数方面显着优于现有的 HPO 提取工具，并且大多数误报是临床相关的祖先术语，而不是幻觉。结果表明，基于 RAG 的基础能够为临床基因组学和罕见疾病诊断提供准确、可靠的表型提取。




- **[Attitudes Toward Use of an APOL1 Genetic Testing Chatbot in Living Kidney Donor Evaluation: A Focus Group Study](https://onlinelibrary.wiley.com/doi/abs/10.1111/ctr.70026)** (*2024*) `Clinical Transplantation`
  > 这项研究探讨了在非裔美国人活体肾脏捐赠者候选人中，对使用 Gia® 遗传信息聊天机器人支持 APOL1 检测的态度。通过涉及捐赠者、接受者和社区成员的焦点小组和调查，参与者通常支持在临床就诊前使用聊天机器人，并表达了对 APOL1 检测的兴趣，但也出现了关于成本、个人偏好和个人障碍的担忧。总体而言，参与者愿意将 APOL1 聊天机器人整合到捐赠者评估工作流中。研究结果表明，文化适应性聊天机器人可以促进遗传检测的讨论和在临床护理中的整合。




- **[Consistent Performance of GPT-4o in Rare Disease Diagnosis Across Nine Languages and 4967 Cases](https://pmc.ncbi.nlm.nih.gov/articles/PMC11888497/)** (*2025*) `medRxiv`
  > 本研究使用近 5000 个源自 HPO 注释表型的结构化临床场景，评估了 GPT-4o 跨九种语言执行罕见遗传病鉴别诊断的能力。使用零样本提示和基于本体的自动评估，该模型在英语和八种非英语语言中取得了相当的性能，在大约 17-21% 的病例中将正确的诊断排在第一位，在大约 25-28% 的病例中排在前三位。跨语言结果的一致性表明，语言障碍可能不会显着降低基于 LLM 的诊断推理能力。总体而言，研究结果表明，像 GPT-4o 这样的 LLM 有可能在非英语临床环境中支持鉴别诊断。



### 工具增强智能体

- **[Autonomous chemical research with large language models](https://www.nature.com/articles/s41586-023-06792-0)** (*2023*) `Nature`
  > 本文介绍了 Coscientist，这是一个由 GPT-4 驱动的 AI 系统，它通过将大型语言模型与用于文献搜索、代码执行和实验自动化的工具相结合，自主设计、计划和执行复杂的科学实验。在六个代表性任务（包括钯催化反应优化）中，Coscientist 在半自主实验设计、执行和推理方面表现出强大的能力。这些结果突出了 LLM 驱动的 AI 系统在加速科学发现方面的多功能性、有效性和可解释性。


- **[CellAgent: An LLM-driven MultiAgent Framework for Automated Single-cell Data Analysis](https://arxiv.org/abs/2407.09811)** (*2024*) `bioRxiv`
  > 本文介绍了 CellAgent，这是一个由 LLM 驱动的多智能体框架，通过协调计划、执行和评估智能体进行分层决策和自我迭代优化，使单细胞 RNA-seq 数据分析完全自动化。CellAgent 自主选择合适的工具和超参数，执行端到端的分析，并在没有人工干预的情况下评估结果。涵盖各种组织和细胞类型的基准测试表明，CellAgent 实现了强大、高质量的性能，同时大大减少了分析师的工作量，推进了“科学智能体”的范例。

- **[RNA-GPT: Multimodal Generative System for RNA Sequence Understanding](https://arxiv.org/abs/2411.08900)** (*2024*) `arXiv`
  > 本文介绍 **RNA-GPT**，这是一种专注于 RNA 的多模态语言模型，旨在通过将 RNA 序列编码器与大型语言模型相结合来支持 RNA 研究。RNA-GPT 将 RNA 序列表示与文本知识对齐，使其能够处理用户提供的 RNA 序列并准确回答与 RNA 相关的复杂查询。该系统使用 RNA-QA 进行训练，RNA-QA 是一种自动化管道，从 RNACentral 提取并组织 RNA 注释以生成大规模指令微调数据。实验表明，RNA-GPT 在一个包含 400,000 多个用于模态对齐和指令微调的精选 RNA 样本的数据集支持下，有效地促进了 RNA 的发现。



- **[MRAgent: an LLM-based automated agent for causal knowledge discovery in disease via Mendelian randomization](https://academic.oup.com/bib/article-abstract/26/2/bbaf140/8107848)** (*2025*) `Briefings in Bioinformatics`
  > 本文介绍了 MRAgent，这是一个由 LLM 驱动的自动智能体，旨在促进使用孟德尔随机化进行大规模因果发现。MRAgent 自主挖掘科学文献以识别候选的暴露-结果对，然后使用全基因组关联研究数据执行 MR 分析，从而减少对人工整理假设的依赖。跨不同 LLM 的评估和概念验证案例研究证明了其执行端到端因果推理工作流的能力。结果强调 MRAgent 是复杂疾病研究中可扩展、系统的因果分析的强大工具。


- **[AutoPM3: Enhancing Variant Interpretation via LLM-driven PM3 Evidence Extraction from Scientific Literature](https://academic.oup.com/bioinformatics/advance-article-abstract/doi/10.1093/bioinformatics/btaf382/8178584)** (*2025*) `Bioinformatics`
  > 本文介绍 AutoPM3，这是一种自动化框架，可从生物医学文献中提取 ACMG/AMP PM3 变异证据以支持罕见病诊断。AutoPM3 使用开源 LLM 结合基于 Text2SQL 的变异提取器和检索增强生成模块，有效处理文本和表格。在最新整理的 PM3-Bench 数据集上进行评估，该方法实现了高精度和召回率，优于依赖更大模型的方法。结果表明，开源 LLM 可以为基于文献的变异解释提供快速、经济且可扩展的解决方案。






## 基准测试 (Benchmark)

This section curates benchmarks for evaluating AI systems in biomedical domains, organized into two categories: Biomedical Reasoning and Question Answering (knowledge and reasoning through Q&A formats) and Complex Real-World Biomedical Task (end-to-end research workflows including planning, tool use, and autonomous execution). This is a document that will be continuously updated.

### 生物医学推理和问答

- **[PubMedQA: A Dataset for Biomedical Research Question Answering](https://aclanthology.org/D19-1259/)** (*2019*) `EMNLP`

  > PubMedQA 是一个基于 PubMed 摘要构建的生物医学问答基准，要求模型使用相应的摘要作为证据，用是、否或也许来回答研究问题。每个实例都将一个源自论文标题的问题与摘要上下文以及总结的是/否/也许标签配对，该基准旨在评估对生物医学研究文本的推理，特别是它们的定量内容，而不是文档检索。

- **[MMLU-Pro: A More Robust and Challenging Multi-Task Language Understanding Benchmark](https://dl.acm.org/doi/10.5555/3737916.3740934)** (*2024*) `NIPS`

  > MMLU-Pro 是一个语言理解基准测试，旨在通过关注复杂的、推理密集型的多项选择题，对大型语言模型提供更具挑战性和区分度的评估。它由包含十个答案选项的问题组成，旨在减少噪音和琐碎性，强调在不同领域中超越表面知识的推理。该基准测试旨在对提示变化表现出更大的鲁棒性，并更好地反映从显式推理策略（如思维链）中获得的收益，从而在早期基准测试中的模型性能变得饱和时，能够更可靠地衡量进展。

- **[GPQA: A Graduate-Level Google-Proof Q&A Benchmark](https://openreview.net/pdf?id=Ti67584b98)** (*2024*) `COLM`

  > GPQA 是一个具有挑战性的多项选择基准，由 448 个由生物、物理和化学领域专家编写的高质量问题组成。这些问题被故意设计得极其困难且“防谷歌搜索”，因此即使是具有不受限制的网络访问权限的熟练非专家也很难可靠地回答它们。该数据集旨在评估超越表面知识的高级科学推理，并作为研究可扩展监督的测试平台，在这些问题中，人类必须在接近或超过专家级难度的问题上评估 AI 输出。

- **[LAB-Bench: Measuring Capabilities of Language Models for Biology Research](https://arxiv.org/abs/2407.10362)** (*2024*) `arXiv`

  > LAB-Bench 是一个全面的基准测试，旨在评估语言模型在实际生物学研究任务中的能力，包括两个关键子任务：数据库问答 (DbQA) 和序列问答 (SeqQA)。DbQA 要求模型对生物数据库进行结构化查询以检索和合成信息，而 SeqQA 则测试对 DNA 和蛋白质序列的推理。该基准测试涵盖了生物医学 AI 智能体的核心能力，包括工具使用、符号推理和结构化生物信息检索，其问题旨在反映实际的研究工作流程，而不仅仅是简单的事实回忆。

- **[Humanity's Last Exam:A Multi-Domain Expert-Level Reasoning Benchmark](https://arxiv.org/abs/2501.14249)** (*2025*) `arXiv`

  > Humanity's Last Exam 是一个具有挑战性的、开放式问题的基准测试，旨在测试跨不同科学和技术领域的高级推理能力。在生物医学子集中，它涵盖 14 个专业子领域，包括遗传学、分子生物学、神经科学、生物化学、微生物学、免疫学、计算生物学、生物物理学、生物信息学、基因组学和生理学。该基准测试专门用于评估真正的泛化能力，而无需任何开发集或特定任务的适应，强调将广泛的生物医学知识和推理应用于需要深度领域专业知识而不是表面模式匹配的陌生、复杂问题的能力。
### **复杂现实世界生物医学任务**

- **[BioLab: End-to-End Autonomous Life Sciences Research with Multi-Agents System Integrating Biological Foundation Models](https://www.biorxiv.org/content/10.1101/2025.09.03.674085v1)** (*2025*) `biorxiv`

  > BioResearchQA 是一个包含 20 个开放式研究问题的定制基准测试，涵盖分子生物学、免疫学、RNA 治疗、蛋白质设计和合成细胞工程。每个问题都被表述为一个现实的研究问题，需要多步骤计划和特定领域的工具选择。三位领域专家使用 5 点李克特量表在三个方面对输出进行评分：多模态规划、生物工具调用和全循环科学推理。

- **[Biomni Real-World Research Tasks: Eight Diverse Biomedical Benchmarks for Evaluating General-Purpose AI Agents](https://doi.org/10.1101/2025.05.30.656746)** (*2025*) `bioRxiv`

  > Biomni 真实世界研究任务是八个新策划的基准测试的集合，涵盖遗传学、基因组学、微生物学、药理学和临床医学，旨在评估在现实研究场景中的零样本泛化。任务包括变异优先级排序、GWAS 因果基因检测、CRISPR 扰动筛选设计、罕见病诊断、药物重新定位、单细胞 RNA-seq 注释、微生物组疾病分类分析和患者基因优先级排序。每个任务都被定义为一个明确但复杂的真实世界生物医学研究目标，需要动态工具组合、多步推理和特定领域的知识整合。性能评估无需任何特定于任务的微调或提示工程，指标包括准确性和相对于基线模型的相对性能提升。执行轨迹显示，模型通常每个任务执行 6-24 个不同的步骤，涉及专门工具、软件包和数据库查询的组合。

- **[AutoBA Multi-Omics Analysis Benchmark: 40 Real-World Bioinformatics Cases for Automated Analysis Evaluation](https://doi.org/10.1002/advs.202407094)** (*2024*) `Advanced Science`

  > AutoBA 多组学分析基准是一个定制评估框架，包含 40 个真实生物信息学分析案例，旨在评估自动化 AI 智能体在常规多组学分析任务上的表现。基准测试涵盖四个主要组学类别：基因组学（15 个案例，包括 WGS 组装、体细胞变异调用、ChIP-seq 峰调用、ATAC-seq、亚硫酸氢盐测序和长读长测序）、转录组学（23 个案例，包括大量 RNA-seq 差异表达、融合基因检测、选择性剪接、单细胞 RNA-seq 聚类、空间转录组学和各种 RNA 修饰分析）、蛋白质组学（1 个关于质谱蛋白质定量的案例）和代谢组学（1 个关于代谢物定量的案例）。生物信息学专家从三个维度评估每个案例：（1）提议的分析计划的质量，包括适当的软件选择和参数设置；（2）生成的用于环境设置和工具安装代码的正确性；以及（3）成功的自动端到端执行。基准测试通过要求系统自主处理软件依赖性、调试执行错误并根据输入数据变化调整分析策略（例如，为具有或没有匹配的正常对照的肿瘤样本选择不同的工具），强调了现实世界的复杂性。与孤立地关注问答或代码生成的现有基准测试不同，该基准测试评估了从原始数据输入到最终生物学结果的完整流程，测试了对于实际生物信息学工作流程至关重要的真正自动化能力。
### 基准测试 (Benchmark) Summary Table

| 基准测试 | 副标题 | 发布渠道 | 类别 | 论文链接 |
| ------------------------------------ | ------------------------------------------------------------ | --------------------- | --------------------------- | ----------------------------------------------------------- |
| **PubMedQA**                         | 生物医学研究问答数据集                                       | EMNLP 2019            | 生物医学推理和问答 | https://aclanthology.org/D19-1259/                          |
| **MMLU-Pro**                         | 更稳健和更具挑战性的多任务语言理解基准测试                   | NIPS 2024             | 生物医学推理和问答 | https://dl.acm.org/doi/10.5555/3737916.3740934              |
| **GPQA**                             | 研究生级防谷歌搜索的问答基准测试                             | COLM 2024             | 生物医学推理和问答 | https://openreview.net/pdf?id=Ti67584b98                    |
| **LAB-Bench**                        | 衡量用于生物学研究的语言模型的能力                           | arXiv 2024            | 生物医学推理和问答 | https://arxiv.org/abs/2407.10362                            |
| **Humanity's Last Exam**             | 多领域专家级推理基准测试                                     | arXiv 2025            | 生物医学推理和问答 | https://arxiv.org/abs/2501.14249                            |
| **BioResearchQA**                    | 端到端自主生命科学研究评估                                   | bioRxiv 2025          | 复杂现实世界任务            | https://www.biorxiv.org/content/10.1101/2025.09.03.674085v1 |
| **Biomni Real-World Research Tasks** | 评估通用 AI 智能体的八个多样化生物医学基准测试               | bioRxiv 2025          | 复杂现实世界任务            | https://doi.org/10.1101/2025.05.30.656746                   |
| **AutoBA Multi-Omics Analysis**      | 40 个用于自动分析评估的真实世界生物信息学案例               | Advanced Science 2024 | 复杂现实世界任务            | https://doi.org/10.1002/advs.202407094                      |

## 2. 库 (Libraries)

本节列出了构建 AI 智能体系统的重要 Python 库和框架，包括生物学 AI 智能体中常用的包以及更广泛的 AI 智能体社区中使用的基础库。这些库根据它们在智能体构建中的主要职责进行组织，包括智能体框架和编排、智能体记忆系统、LLM 后端和推理、智能体服务和监控。

### 智能体框架和编排

- **[AutoGen: Enabling Next-Gen LLM Applications via Multi-Agent Conversation](https://github.com/microsoft/autogen)** `Microsoft Research`

  > AutoGen is a framework for building agent conversation systems that enables the development of LLM applications using conversational agents. It provides foundations for task orchestration and agent coordination, implementing event-driven architecture with asynchronous message-passing protocols. The framework handles agent instantiation with specific functional roles and manages structured message-passing that supports both forward task progression and retrospective error correction across specialized agents (e.g., Planner, Reasoner, Memory, RAG, Tool executors, Code, Critic, Reporter).

- **[CodeAct: Executable Code Actions Elicit Better LLM Agents](https://github.com/xingyaoww/code-act) ** `UIUC & Apple`

  >CodeAct is a framework that consolidates LLM agents' actions into a unified code action space. Enables agents to execute Python code dynamically, revise prior actions through self-debugging, and emit new actions upon observations in multi-turn interactions. Supports complex operations through control and data flow, leverages extensive software packages for expanded action space, and provides automated feedback mechanisms for iterative task solving.

- **[LangChain: Platform for Reliable Agents](https://github.com/langchain-ai/langchain)** `LangChain`
  
  > LangChain is a comprehensive framework for building agent systems and LLM-powered applications. Provides modular components for chaining interoperable elements, integrating with diverse data sources and external systems, and enabling rapid prototyping through component-based architecture. Supports model interoperability, real-time data augmentation, and production-ready features with built-in monitoring and evaluation capabilities for deploying reliable agent applications.

- **[LangGraph: Build Resilient Language Agents as Graphs](https://github.com/langchain-ai/langgraph)**  `LangChain`

  >LangGraph is a low-level orchestration framework for building controllable, stateful multi-agent applications with complex workflows. Enables customizable agent architectures with built-in support for persistent checkpoints, cycles, and human-in-the-loop interactions. Provides graph-based workflow management for coordinating multiple agents, long-term memory capabilities, and production-ready deployment tools. Integrates seamlessly with LangChain ecosystem while supporting standalone usage for agent systems requiring precise control over execution flow.

- **[CrewAI: Framework for Orchestrating Role-Playing, Autonomous AI Agents](https://github.com/joaomdmoura/crewai)** `CrewAI`
  
  > CrewAI is a framework for building collaborative multi-agent systems with role-based task delegation. Enables developers to create crews of specialized agents that work together to accomplish complex tasks, with built-in process orchestration (sequential, hierarchical, consensual). Provides task decomposition and assignment mechanisms, inter-agent communication protocols, and memory sharing across agent crews for collaborative problem-solving.

- **[BioChatter: A Platform for the Biomedical Application of Large Language Models](https://biochatter.org)** `Heidelberg University & EMBL-EBI`
  
  > BioChatter is an open-source Python framework designed for developing custom biomedical research software using LLMs while adhering to open science principles. Provides unified API abstraction layer that harmonizes different LLM deployment tools and proprietary providers, enabling seamless model switching without code changes. Integrates with BioCypher knowledge graphs and vector databases for retrieval-augmented generation, facilitates external API integration through robust parameterization, and supports multi-agent systems with reflection-based workflows. Features continuous benchmarking infrastructure for reproducibility, customizable system prompts for domain alignment, and modular architecture supporting deployment spectrum from rapid prototyping to fully encapsulated production systems with complete data sovereignty.

### 智能体记忆系统
- **[LlamaIndex: Building LLM-powered Agents over Data](https://github.com/run-llama/llama_index)** `LlamaIndex`
  
  > LlamaIndex is a data framework for building context-aware agent systems with persistent knowledge management capabilities. Provides data connectors to ingest information from diverse sources (APIs, PDFs, databases, documents), structures data through customizable indices and knowledge graphs for efficient retrieval, and offers advanced query interfaces for agents to access relevant context. Enables agents to augment LLM reasoning with external and private data through RAG (Retrieval-Augmented Generation) patterns, supports both high-level APIs for rapid prototyping and low-level components for custom memory architectures, and integrates seamlessly with agent frameworks for building knowledge-grounded applications.

- **[Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory](https://github.com/mem0ai/mem0)** `Mem0 AI`

  > Mem0 is a framework designed for building AI agents with scalable, persistent memory capabilities. It provides hierarchical memory design, implementing both short-term memory (STM) for transient task-level context and long-term memory (LTM) for persistent knowledge storage. The framework supports user-profile stores and vector-based factual stores with semantic retrieval capabilities, enabling agents to maintain context across sessions and perform analogical reasoning across different problems.

- **[Redis: The Real-Time Data Platform](https://github.com/redis/redis)** `Redis`

  > Redis is an in-memory data structure store used as a database, cache, and message broker. In agent systems, Redis provides the backing store for agent memory with real-time state tracking capabilities. It supports memory buffers (with first-in-first-out eviction) and serves as an indexing layer for approximate nearest-neighbor search in vector stores, enabling fast semantic retrieval of validated facts, procedural workflows, and experimental findings across agent sessions.

- **[ChromaDB: Open-source search and retrieval database for AI applications](https://github.com/chroma-core/chroma)** `Chroma`
  
  > ChromaDB is an AI-native embedding database designed for building LLM applications with semantic search capabilities. Provides efficient storage and retrieval of embeddings for agent memory systems, supports metadata filtering and hybrid search, and offers both in-memory and persistent storage options. Enables agents to maintain vector-based knowledge stores with fast similarity search, integrates seamlessly with LangChain and LlamaIndex, and includes built-in embedding functions for multiple models.
  
- **[Qdrant: Vector Search Engine for the Next Generation of AI Applications](https://github.com/qdrant/qdrant)** `Qdrant`
  
  > Qdrant is a high-performance vector similarity search engine designed for agent memory and retrieval systems. Features advanced filtering, payload-based queries, and efficient approximate nearest neighbor search. Supports distributed deployments, provides JSON-based filtering for complex queries, and offers both cloud and self-hosted options for production agent applications.

### LLM后端和智能体推理

- **[Transformers: State-of-the-Art Natural Language Processing](https://github.com/huggingface/transformers)** `Hugging Face`

  > Transformers is a library providing thousands of pretrained models for natural language processing tasks. It serves as the core inference engine for agent reasoning capabilities, enabling systems to leverage large language models for task decomposition, scientific reasoning, and decision-making. The library powers various LLM-based agent components including query rewriting, information synthesis, and LLM-driven consolidation processes in memory systems.

- **[vLLM: High-throughput and memory-efficient LLM inference engine](https://github.com/vllm-project/vllm)** `UC Berkeley`
  
  > vLLM is a fast and memory-efficient inference engine for large language models. Optimizes agent inference with PagedAttention for efficient memory management, continuous batching for high throughput, and optimized CUDA kernels. Enables agents to handle multiple concurrent requests efficiently, supports various quantization methods for reduced memory footprint, and provides OpenAI-compatible API for seamless integration with agent frameworks.
  
- **[Ollama: Get Up and Running With Large Language Models](https://github.com/ollama/ollama)** `Ollama`
  
  > Ollama is a local runtime for running large language models on personal machines without relying on cloud services. Enables agents to execute LLM inference locally with support for multiple open-source models including Llama, Mistral, Gemma, and DeepSeek. Provides a unified API for model management, supports model customization through Modelfiles, and offers GPU acceleration with CUDA and Vulkan. Allows agents to maintain data privacy while accessing powerful language models, includes support for multimodal inputs, and integrates seamlessly with agent frameworks through its REST API and Python/JavaScript libraries.

- **[OpenAI Python: Official Python client for the OpenAI API](https://github.com/openai/openai-python)** `OpenAI`

  > OpenAI Python is the official Python library for accessing OpenAI's REST API, providing agent systems with direct access to GPT models and other OpenAI services. Features type-safe request and response handling with full autocomplete support, both synchronous and asynchronous client implementations, and auto-paginating iterators for list operations. Enables agents to leverage OpenAI's language models for reasoning, text generation, vision understanding, and tool calling capabilities. Supports streaming responses for real-time agent interactions, comprehensive timeout and retry configurations, and integration with various agent frameworks for building production-ready AI applications.

- **[Anthropic Python: Official Python client for the Anthropic API](https://github.com/anthropics/anthropic-sdk-python)** `Anthropic`

  > Anthropic Python is the official Python library for accessing Anthropic's REST API, providing agent systems with direct access to Claude models and advanced AI capabilities. Features type-safe request and response handling with Pydantic models, both synchronous and asynchronous client implementations, and native support for streaming responses. Enables agents to leverage Claude's language models for reasoning, analysis, tool use (function calling), and extended thinking capabilities. Supports prompt caching for cost optimization, vision understanding for multimodal inputs, and seamless integration with agent frameworks. Provides comprehensive configuration options for timeouts, retries, and custom headers, with built-in support for Amazon Bedrock deployments for enterprise agent applications.

### 智能体服务和监控

- **[MLflow: Open-Source Platform for Productionizing AI](https://github.com/mlflow/mlflow)** `Databricks`

  > MLflow is an open-source platform for managing the end-to-end machine learning lifecycle. For agent systems, MLflow enables logging and versioning of agent episodes, ensuring reproducibility across experimental runs. It tracks agent execution traces, intermediate results, tool invocations, and decision rationales, maintaining provenance metadata for all computational experiments. The platform enables auditing of entire workflows from planning through execution and validation, with deterministic seed initialization for reproducible agent behaviors.

- **[Chainlit: Build Conversational AI in minutes](https://github.com/Chainlit/chainlit)** `Chainlit`
  
  > Chainlit is a framework for rapidly building conversational interfaces for agent systems. Enables developers to create chat-based UIs with built-in support for streaming responses, multi-step interactions, and visualization of agent workflows. Features automatic conversation history management, file upload handling, and integration with major frameworks including LangChain, LlamaIndex, and OpenAI. Provides decorators for defining message handlers and tool execution steps, supports real-time collaboration, and includes data layer capabilities for persistent storage with PostgreSQL and cloud storage backends. Allows rapid prototyping of agent interfaces with minimal code while maintaining production-ready scalability.

- **[Flask: Lightweight Web Framework](https://github.com/pallets/flask)** `Pallets`
  
  > Flask is a lightweight WSGI web framework for building web applications and APIs in Python. Commonly used to create HTTP endpoints for agent systems, providing flexible routing, request handling, and response formatting capabilities. Features a minimalist core with extensive ecosystem of extensions for authentication, database integration, and API development. Enables developers to build custom web interfaces for agent interactions, deploy agent services as REST APIs, and integrate agent systems into larger web applications. Supports both synchronous and asynchronous operations, offers template rendering with Jinja2, and provides straightforward deployment options for serving agent-powered applications.
-  **[FastAPI: Modern, fast web framework for building APIs](https://github.com/tiangolo/fastapi)** `Sebastián Ramírez`
  
  > FastAPI is a modern, high-performance web framework for building APIs with Python. Widely used for deploying agent systems as production services with automatic API documentation, asynchronous request handling, and type validation through Pydantic. Provides WebSocket support for real-time agent interactions, dependency injection for managing agent lifecycles, and OpenAPI schema generation for agent endpoint documentation. Enables rapid development of agent APIs with built-in data validation and serialization.
  
- **[Gradio: Build Machine Learning Web Apps](https://github.com/gradio-app/gradio)** `Hugging Face`
  
  > Gradio is a Python library for quickly creating customizable UI components for machine learning models and agent systems. Enables developers to build interactive interfaces for agent demonstrations with minimal code, supports various input types including text, images, and audio, and provides real-time feedback visualization. Features built-in sharing capabilities, component composition for complex workflows, and seamless integration with Hugging Face Spaces for public deployment of agent applications.

### 库总结表

| 库          | 副标题                                                     | 组织      | 类别                            | GitHub 链接                                        |
| ---------------- | ------------------------------------------------------------ | ------------------ | ---------------------------------- | -------------------------------------------------- |
| AutoGen          | 通过多智能体对话实现下一代 LLM 应用程序 | Microsoft Research | 智能体框架和编排 | https://github.com/microsoft/autogen               |
| CodeAct          | 可执行的代码操作能引出更好的 LLM 智能体             | UIUC & Apple       | 智能体框架和编排 | https://github.com/xingyaoww/code-act              |
| LangChain        | 可靠智能体平台                                 | LangChain          | 智能体框架和编排 | https://github.com/langchain-ai/langchain          |
| LangGraph        | 将弹性语言智能体构建为图                    | LangChain          | 智能体框架和编排 | https://github.com/langchain-ai/langgraph          |
| CrewAI           | 编排角色扮演和自主 AI 智能体的框架 | CrewAI             | 智能体框架和编排 | https://github.com/joaomdmoura/crewai              |
| LlamaIndex       | 在数据之上构建由 LLM 驱动的智能体                        | LlamaIndex         | 智能体记忆系统               | https://github.com/run-llama/llama_index           |
| Mem0             | 使用可扩展长期记忆构建生产就绪的 AI 智能体 | Mem0 AI            | 智能体记忆系统               | https://github.com/mem0ai/mem0                     |
| Redis            | 实时数据平台                                  | Redis              | 智能体记忆系统               | https://github.com/redis/redis                     |
| ChromaDB         | 适用于 AI 应用程序的开源搜索和检索数据库 | Chroma             | 智能体记忆系统               | https://github.com/chroma-core/chroma              |
| Qdrant           | 下一代 AI 应用程序的向量搜索引擎 | Qdrant             | 智能体记忆系统               | https://github.com/qdrant/qdrant                   |
| Transformers     | 最先进的自然语言处理                 | Hugging Face       | LLM后端和智能体推理   | https://github.com/huggingface/transformers        |
| vLLM             | 高吞吐量且内存高效的 LLM 推理引擎    | UC Berkeley        | LLM后端和智能体推理  | https://github.com/vllm-project/vllm               |
| Ollama           | 启动并运行大型语言模型                | Ollama             | LLM后端和智能体推理  | https://github.com/ollama/ollama                   |
| OpenAI Python    | OpenAI API 的官方 Python 客户端                    | OpenAI             | LLM后端和智能体推理  | https://github.com/openai/openai-python            |
| Anthropic Python | Anthropic API 的官方 Python 客户端                 | Anthropic          | LLM后端和智能体推理  | https://github.com/anthropics/anthropic-sdk-python |
| MLflow           | 将 AI 生产化的开源平台                  | Databricks         | 智能体服务和监控      | https://github.com/mlflow/mlflow                   |
| Chainlit         | 分钟级构建对话式 AI                           | Chainlit           | 智能体服务和监控       | https://github.com/Chainlit/chainlit               |
| Flask            | 轻量级 Web 框架                                    | Pallets            | 智能体服务和监控      | https://github.com/pallets/flask                   |
| FastAPI          | 用于构建 API 的现代、快速 Web 框架                 | Sebastián Ramírez  | 智能体服务和监控      | https://github.com/tiangolo/fastapi                |
| Gradio           | 构建机器学习 Web 应用程序                              | Hugging Face       | 智能体服务和监控      | https://github.com/gradio-app/gradio               |

## 3. 知识库

本目录提供了计算生物学和生物医学研究中 AI 智能体系统的生物医学数据库和文献平台。资源按生物学内容类型进行组织：基因组学和临床数据库（变异、表达、临床数据）、分子和结构数据库（蛋白质、通路、药物）、专门的生物医学数据库（单细胞、模型生物、试剂）和科学文献（出版物、预印本）。

**[TODO]注**：未来版本将包含访问方法标签（API、批量下载、Web 界面）以方便智能体实现。
### 基因组学和临床数据库

- **[ClinVar: Public archive of interpretations of clinically relevant variants](https://www.ncbi.nlm.nih.gov/clinvar/)** `NCBI`

  > ClinVar is a freely accessible database archiving clinical interpretations of genomic variations and their relationships to human health conditions. Aggregates variant classifications from clinical testing laboratories, research groups, expert panels, and locus-specific databases worldwide, providing agents with authoritative variant-disease associations essential for clinical diagnosis and precision medicine. Features structured submission records (SCV accessions), aggregated variant interpretations (RCV accessions), evidence documentation, and review status indicators. Supports programmatic access through E-utilities API and monthly data releases in XML, VCF, and tabular formats for systematic variant interpretation workflows.

- **[MyGene2: Sharing Information to Learn About Genes and Rare Conditions](https://mygene2.org/)** `University of Washington`

  > MyGene2 is a patient-driven registry and data-sharing platform connecting individuals and families affected by rare genetic conditions to facilitate gene discovery and improve variant interpretation. Provides genetic variants, phenotypic descriptions, clinical histories, and natural history data reported directly by patients and families with rare and ultra-rare disorders often lacking sufficient published literature. Enables agents to access patient-reported genotype-phenotype correlations, novel variant-disease associations, clinical outcome data, and family experiences supporting variant classification, gene-disease relationship validation, and natural history studies for rare disease research and clinical interpretation of variants of uncertain significance.


- **[MPD: Mouse Phenome Database](https://www.jax.org/research-and-faculty/resources/mouse-phenome-database)** `The Jackson Laboratory`

  > MPD is a comprehensive resource for strain characteristics, phenotypic data, genotypic information, and experimental protocols for laboratory mouse strains used in biomedical research. Provides standardized phenotype measurements across cardiovascular, metabolic, behavioral, hematological, and other physiological systems for hundreds of inbred, recombinant inbred, and mutant mouse strains. Enables agents to access comparative phenotypic data, quantitative trait loci (QTL) mapping results, genetic variation information, and experimental protocols supporting translational research, disease modeling, and genotype-phenotype correlation studies in model organism research.

- **[gnomAD: Genome Aggregation Database](https://gnomad.broadinstitute.org/)** `Broad Institute`

  > gnomAD is the world's largest public database of human genetic variation, aggregating and harmonizing exome and genome sequencing data from over 800,000 individuals across diverse global populations. Provides population allele frequencies, constraint metrics, and variant annotations enabling agents to distinguish pathogenic variants from benign population variation in clinical interpretation workflows. Features ancestry-specific frequency data, loss-of-function variant catalogues, structural variant annotations, and quality-controlled variant calls accessible through browser interface, API, and cloud-based data releases on AWS, Azure, and Google Cloud platforms.

- **[UCSC Genome Browser: Integrated tool for visualizing and analyzing genome assemblies](https://genome.ucsc.edu/)** `UC Santa Cruz Genomics Institute`

  > UCSC Genome Browser is a comprehensive platform for exploring genomic annotations, comparative genomics, and experimental data across multiple species and genome assemblies. Provides agents with integrated access to reference sequences, gene predictions, regulatory elements, conservation scores, variation data, and thousands of experimental tracks from ENCODE, GTEx, and other large-scale projects. Supports programmatic data retrieval through REST API, MySQL database access, and downloadable track data for systematic genome analysis and cross-species comparative studies.

- **[COSMIC: Catalogue of Somatic Mutations in Cancer](https://cancer.sanger.ac.uk/cosmic)** `Wellcome Sanger Institute`

  > COSMIC is the world's most comprehensive database of somatic mutations in human cancer, cataloging millions of tumor-associated genetic alterations across cancer types and genes. Integrates data from large-scale cancer genome sequencing projects (TCGA, ICGC) with manually curated literature-derived mutations, providing agents with mutation frequencies, tissue distributions, functional predictions, and drug resistance associations. Features cancer gene census annotations, fusion gene data, copy number variants, and structural rearrangements accessible through web interface, downloads, and programmatic API for cancer genomics analysis.

- **[Open Targets Genetics: Systematic drug target identification and prioritization](https://genetics.opentargets.org/)** `Open Targets`

  > Open Targets Genetics is a comprehensive platform integrating genome-wide association studies (GWAS), functional genomics, and variant-to-gene mapping to establish disease-gene relationships for therapeutic target discovery. Aggregates data from GWAS Catalog, UK Biobank, FinnGen, and other sources with locus-to-gene scoring, quantitative trait loci (QTL) data, and pathway enrichment analyses. Enables agents to prioritize drug targets based on genetic evidence strength, explore variant functional consequences, and assess target tractability through systematic integration of population genetics and molecular data.

- **[RegulomeDB: Annotation of regulatory variants in the human genome](http://www.regulomedb.org/)** `Stanford University`

  > RegulomeDB is a database annotating regulatory potential of human genetic variants using evidence from ENCODE, Roadmap Epigenomics, and other functional genomics projects. Provides scoring of non-coding variants based on transcription factor binding, DNase hypersensitivity, histone modifications, chromatin states, and expression quantitative trait loci (eQTL) associations. Enables agents to prioritize regulatory variants, predict functional impacts on gene expression, and identify variants affecting transcriptional regulation in cell type-specific contexts.

- **[GEO: Gene Expression Omnibus](https://www.ncbi.nlm.nih.gov/geo/)** `NCBI`

  > GEO is a public repository archiving high-throughput gene expression and functional genomics data from microarray, RNA-seq, ChIP-seq, and other platforms across millions of samples. Provides curated datasets (GEO DataSets), standardized sample metadata, platform annotations, and processed expression matrices enabling agents to perform meta-analyses and comparative transcriptomics studies. Supports programmatic access through GEOquery API, direct data downloads, and integration with NCBI's analysis tools for systematic exploration of gene expression patterns across experimental conditions, tissues, and diseases.

- **[SRA: Sequence Read Archive](https://www.ncbi.nlm.nih.gov/sra/)** `NCBI`

  > SRA is the largest public repository for high-throughput sequencing data, storing raw sequencing reads and alignment information from next-generation sequencing platforms. Part of the International Nucleotide Sequence Database Collaboration (INSDC) with EBI and DDBJ, SRA contains over 25 petabase pairs from 14.8M+ runs spanning all branches of life including genomic, transcriptomic, metagenomic, and epigenomic studies. Agents access SRA data through E-utilities API, SRA Toolkit for format conversion (FASTQ, BAM), and cloud platforms (AWS S3, Google Cloud BigQuery) enabling large-scale sequence data retrieval, reanalysis of published datasets, and meta-analyses across thousands of sequencing experiments for comparative genomics and variant discovery.

- **[ENCODE: Encyclopedia of DNA Elements](https://www.encodeproject.org/)** `NHGRI`

  > ENCODE systematically maps functional elements in human and mouse genomes through comprehensive experimental characterization of transcription, transcription factor binding, chromatin structure, histone modifications, and DNA methylation. Phase III data includes 5,992 experimental datasets across 503 cell/tissue types, defining 926,535 human and 339,815 mouse candidate cis-regulatory elements covering 7.9% and 3.4% of respective genomes. Agents utilize ENCODE data for regulatory element annotation, epigenomic state analysis, variant interpretation in non-coding regions, and understanding gene regulation mechanisms. Data accessible through ENCODE Portal REST API, available on AWS Open Data Registry, with uniform processing pipelines ensuring high-quality ChIP-seq, RNA-seq, ATAC-seq, and Hi-C datasets.

- **[NCBI RefSeq: Reference Sequence Database](https://www.ncbi.nlm.nih.gov/refseq/)** `NCBI`

  > RefSeq provides curated, non-redundant reference sequences for genomes, transcripts, and proteins across 55,000+ organisms spanning prokaryotes, eukaryotes, and viruses. Distinguished by unique accession format (e.g., NM_, NP_), RefSeq records integrate information from multiple sources with expert curation, representing current consensus sequences with comprehensive functional annotation including coding regions, conserved domains, variation, and standardized nomenclature. Agents use RefSeq as the gold standard for sequence alignment, variant annotation, gene identification, and comparative genomics. Accessible via Entrez queries, BLAST searches, FTP downloads, and programmatic retrieval through E-utilities, with specialized projects including MANE (matched clinical transcripts), RefSeqGene (clinical reference standards), and RefSeq Functional Elements.

- **[Ensembl: Genome Browser and Annotation System](http://www.ensembl.org/index.html)** `EMBL-EBI`

  > Ensembl provides comprehensive genome annotation, comparative genomics, and variation data for 50,000+ genomes through automated annotation pipelines and expert curation. The system integrates gene predictions, homology relationships, regulatory features, genetic variation (SNPs, indels, structural variants), and phenotype associations within an interactive genome browser supporting vertebrates via main Ensembl site and non-vertebrates through Ensembl Genomes (Plants, Metazoa, Bacteria, Fungi, Protists). Agents leverage Ensembl's REST API and Perl API to programmatically retrieve gene structures, orthology mappings, variant annotations, regulatory build data, and cross-species alignments. Includes Variant Effect Predictor (VEP) for variant consequence prediction and BioMart for bulk data extraction across multiple species and data types.


### 分子和结构数据库

- **[PDB: Protein Data Bank](https://www.rcsb.org/)** `RCSB`

  > PDB is the global repository for experimentally determined three-dimensional structures of proteins, nucleic acids, and complex assemblies determined by X-ray crystallography, NMR spectroscopy, and cryo-electron microscopy. Provides atomic coordinates, experimental data, structural quality metrics, and functional annotations for hundreds of thousands of biomolecular structures enabling agents to perform structure-based drug design, protein engineering, and molecular function prediction. Features advanced search capabilities, structure alignment tools, and programmatic access through REST API and file downloads in PDB, mmCIF, and other standard formats.
- **[miRBase: The MicroRNA Database](https://www.mirbase.org/)** `University of Manchester`

  > miRBase is the primary online repository for published microRNA sequences, nomenclature, annotations, and predicted gene targets across metazoan, plant, and viral genomes. Provides curated miRNA gene sequences, genomic locations, hairpin precursor structures, mature miRNA sequences, expression data, and standardized nomenclature for thousands of microRNA loci across hundreds of organisms. Enables agents to identify miRNAs, analyze post-transcriptional gene regulation mechanisms, predict miRNA-target interactions, explore regulatory networks in development and disease, and retrieve sequence data through web interface, downloadable flat files, and MySQL database access for non-coding RNA research.
- **[UniProt: Universal Protein Resource](https://www.uniprot.org/)** `UniProt Consortium`

  > UniProt is the most comprehensive and high-quality protein sequence and functional information database, integrating data from scientific literature and computational analyses into unified protein records. Provides expertly curated annotations in Swiss-Prot including protein function, subcellular localization, post-translational modifications, protein-protein interactions, disease associations, and structural features, alongside computationally annotated TrEMBL entries for complete proteome coverage. Enables agents to retrieve standardized protein identifiers, cross-references to over 150 biological databases, sequence variants, and GO term annotations through web services, SPARQL endpoints, and bulk data downloads.

- **[AlphaFold DB: AlphaFold Protein Structure Database](https://alphafold.ebi.ac.uk/)** `DeepMind & EMBL-EBI`

  > AlphaFold DB provides AI-predicted protein structures for over 200 million proteins across all domains of life, generated using DeepMind's AlphaFold system achieving near-experimental accuracy. Offers high-confidence structural models with per-residue confidence scores (pLDDT) and predicted aligned error (PAE) matrices for virtually complete proteomes including human, model organisms, and UniProt reference proteomes. Enables agents to access predicted structures for proteins lacking experimental data through downloadable coordinate files, interactive 3D visualization, and programmatic API, dramatically expanding structural coverage for structure-based analysis and computational drug discovery.

- **[InterPro: Protein Sequence Analysis and Classification](https://www.ebi.ac.uk/interpro/)** `EMBL-EBI`

  > InterPro integrates protein signatures from multiple member databases (Pfam, PROSITE, SMART, PRINTS, ProDom) into a unified classification system for protein families, domains, and functional sites. Provides comprehensive functional annotation through sequence-based predictions of conserved regions, structural domains, active sites, and binding sites with hierarchical organization and GO term associations. Enables agents to infer protein function, identify evolutionary relationships, predict domain architecture, and annotate novel sequences through InterProScan service, web interface, and downloadable signature libraries for high-throughput protein classification.

- **[KEGG: Kyoto Encyclopedia of Genes and Genomes](https://www.genome.jp/kegg/)** `Kanehisa Laboratories`

  > KEGG is a comprehensive database integrating genomic, chemical, and systemic functional information through manually curated metabolic pathways, regulatory networks, and disease associations across thousands of organisms. Provides pathway maps, enzyme reactions, compound structures, drug-target relationships, disease genes, and genome annotations enabling agents to analyze biological systems at molecular and cellular levels. Features KEGG Orthology for functional annotation, BRITE hierarchies for biological entities, and network-based approaches for understanding gene functions, metabolic capabilities, and drug mechanisms through REST API and flat file downloads.

- **[Reactome: Pathway Knowledgebase](https://reactome.org/)** `Reactome`

  > Reactome is a manually curated, peer-reviewed database of human biological pathways and processes, providing detailed molecular mechanisms with experimental evidence and cross-species pathway projections. Features hierarchically organized pathways covering metabolism, signal transduction, transcriptional regulation, and disease processes with protein-protein interactions, post-translational modifications, and subcellular localization information. Supports agents with pathway enrichment analysis tools, pathway diagram exports, programmatic access through REST API and graph database queries, and integration with omics data for functional interpretation and systems biology analysis.

- **[JASPAR: Open-Access Database of Transcription Factor Binding Profiles](https://jaspar.genereg.net/)** `JASPAR Consortium`

  > JASPAR is the largest open-access database of curated, non-redundant transcription factor (TF) binding profiles derived from published collections of experimentally defined binding sites for eukaryotes. Provides position frequency matrices (PFMs), position weight matrices (PWMs), sequence logos, and validated TF binding sites for hundreds of transcription factors across multiple species including human, mouse, and other model organisms. Enables agents to predict transcription factor binding sites in regulatory sequences, analyze promoter regions, identify cis-regulatory elements, and understand gene regulatory mechanisms through web-based scanning tools, downloadable matrix collections, and programmatic API access.

- **[BindingDB: Database of Measured Binding Affinities](https://www.bindingdb.org/)** `UC San Diego`

  > BindingDB is a public database of measured binding affinities focusing on interactions between proteins and small molecules relevant to drug discovery and chemical biology. Provides quantitative binding data including dissociation constants (Kd), inhibition constants (Ki), IC50, and EC50 values for hundreds of thousands of protein-ligand complexes extracted from peer-reviewed scientific literature and patents. Enables agents to analyze structure-activity relationships, build predictive QSAR models, support virtual screening campaigns, and inform medicinal chemistry decisions through searchable web interface, downloadable datasets, and programmatic access for computational drug design workflows.

- **[DrugBank: Comprehensive Bioinformatics and Cheminformatics Resource](https://www.drugbank.com/)** `University of Alberta`

  > DrugBank is a comprehensive database combining detailed drug information with comprehensive molecular biology and pharmacology data for thousands of drug entries including FDA-approved drugs, experimental compounds, and nutraceuticals. Provides chemical structures, mechanisms of action, pharmacokinetics (ADME), pharmacodynamics, drug-drug interactions, drug-target relationships, metabolic pathways, adverse effects, dosing information, and clinical trial data. Supports agents with structured drug knowledge including protein targets, associated pathways, disease indications, patent information, and literature references accessible through web interface, REST API, and downloadable datasets for drug repurposing, polypharmacology analysis, and therapeutic target discovery.

### 专门的生物医学数据库

- **[CellxGene: Single-Cell Data Explorer and Census](https://cellxgene.cziscience.com/)** `Chan Zuckerberg Initiative`

  > CellxGene is a comprehensive platform for exploring, analyzing, and sharing single-cell RNA-seq datasets from diverse tissues, organisms, and experimental conditions across millions of individual cells. Provides the CZ CELLxGENE Discover collection with standardized, quality-controlled datasets annotated with cell types, tissues, diseases, and experimental metadata following community standards. Enables agents to query cell type-specific gene expression profiles, perform comparative analyses across studies, access curated cell annotations, and retrieve processed single-cell expression matrices through web interface, downloadable h5ad files, and programmatic API for large-scale single-cell genomics analysis.


- **[IUCN Red List: The IUCN Red List of Threatened Species](https://www.iucnredlist.org/)** `International Union for Conservation of Nature`

  > IUCN Red List is the world's most comprehensive inventory of global conservation status assessments for biological species, providing extinction risk evaluations, population trends, and conservation needs for over 150,000 species. Offers detailed information on species distributions, population sizes, habitat requirements, ecological roles, threats, conservation actions, and Red List Categories (Extinct, Critically Endangered, Endangered, Vulnerable, etc.) based on standardized criteria. Supports agents analyzing biodiversity patterns, conservation priorities, extinction risk factors, and ecological research across taxonomic groups through searchable database, species accounts, spatial data downloads, and API access for conservation biology and macroecology applications.

- **[Human Microbiome Project: Data Analysis and Coordination Center](https://commonfund.nih.gov/hmp)** `National Institutes of Health`

  > Human Microbiome Project provides comprehensive metagenomic, metatranscriptomic, metabolomic, and clinical datasets characterizing microbial communities from multiple human body sites including gut, oral, skin, and urogenital regions. Offers standardized sampling protocols, reference microbial genomes, multi-omics data integration, and longitudinal microbiome profiles linking microbial community composition to human health and disease states. Enables agents to analyze host-microbiome interactions, study microbial diversity patterns, investigate metabolic functions of microbial communities, and explore relationships between microbiome dysbiosis and diseases through downloadable datasets, cloud-based analysis workbenches, and API access for microbiome research applications.

- **[Addgene: Nonprofit Plasmid Repository](https://www.addgene.org/)** `Addgene`

  > Addgene is a nonprofit plasmid repository archiving and distributing research-ready molecular biology tools for genome engineering, gene expression, and functional genomics. The collection contains 147,000+ plasmids including CRISPR/Cas systems, lentiviral vectors, fluorescent protein constructs, optogenetic tools, shRNA knockdown plasmids, and expression backbones spanning all major model organisms and experimental systems. Each plasmid entry includes annotated sequence maps, cloning information, resistance markers, quality control data, and links to original publications ensuring proper attribution to depositing laboratories. Agents access Addgene's database through BLAST sequence search for finding similar constructs, browsing curated collections by application (genome editing, protein tagging, biosensors), and retrieving standardized plasmid sequences with comprehensive metadata for computational design of cloning strategies and experimental planning.
- **[10X Genomics Datasets](https://www.10xgenomics.com/datasets)** `10x Genomics`

  > 10X Genomics provides publicly available reference datasets from Chromium single-cell and spatial genomics platforms including single-cell RNA-seq (3' and 5' gene expression), immune profiling (V(D)J sequencing), ATAC-seq, multiome (RNA+ATAC), and Visium spatial transcriptomics across diverse tissue types and species. Datasets include PBMC samples, tissue dissociations, cancer specimens, and developmental studies with accompanying FASTQ files, processed gene-barcode matrices, analysis outputs from Cell Ranger pipeline, and Loupe Browser visualization files. Agents access these gold-standard benchmark datasets for method validation, pipeline testing, tutorial development, and comparative analysis of single-cell analysis algorithms. All datasets include comprehensive metadata on sample preparation, sequencing parameters, and quality metrics enabling reproducible computational workflows.

### 科学文献

- **[PubMed: Free Biomedical Literature Search Engine](https://pubmed.ncbi.nlm.nih.gov/)** `NCBI`

  > PubMed is a free comprehensive database providing access to over 39 million citations and abstracts for biomedical literature from MEDLINE, life science journals, and online books spanning medicine, biology, biochemistry, and related disciplines. Features MeSH (Medical Subject Headings) controlled vocabulary for precise searching, advanced query builders, clinical queries filters, and automated linking to full-text articles via PubMed Central and publisher websites. Enables agents to perform systematic literature searches, retrieve evidence-based information, access publication metadata, and utilize E-utilities API for programmatic access supporting automated literature reviews, knowledge extraction, and citation network analysis for biomedical research applications.

- **[Google Scholar: Stand on the Shoulders of Giants](https://scholar.google.com/)** `Google`

  > Google Scholar is a comprehensive academic search engine indexing scholarly literature across all disciplines including peer-reviewed papers, theses, dissertations, books, preprints, patents, and conference proceedings from academic publishers, universities, and scholarly organizations. Provides citation metrics, related articles discovery, author profiles, and cross-disciplinary coverage extending beyond biomedical literature to physical sciences, social sciences, arts, and humanities. Enables agents to discover interdisciplinary research connections, track citation networks, assess research impact through h-index and citation counts, and access diverse scholarly resources through broad indexing that complements domain-specific databases for comprehensive knowledge discovery.

- **[bioRxiv: The Preprint Server for Biology](https://www.biorxiv.org/)** `Cold Spring Harbor Laboratory`

  > bioRxiv is a free online preprint repository enabling rapid dissemination of biological research findings prior to peer review, covering over 25 subject areas including genomics, neuroscience, bioinformatics, cell biology, developmental biology, and systems biology. Provides immediate public access to complete unpublished manuscripts with digital object identifiers (DOIs) for citation, version tracking for manuscript updates, and automated linking to subsequently published journal articles. Enables agents to access cutting-edge research methods, emerging computational tools, preliminary findings, and novel experimental approaches months before formal publication, essential for tracking rapidly evolving research areas, identifying trending methodologies, and maintaining awareness of latest developments in biological sciences through RSS feeds, API access, and bulk download capabilities.

- **[Google Search: Search the World's Information](https://www.google.com/)** `Google`

  > Google Search is a comprehensive web search engine providing real-time access to billions of web pages, news articles, images, videos, and diverse online content across the internet. Offers advanced search operators, date filtering for recent content, site-specific searches, and natural language query processing enabling agents to discover breaking research news, conference announcements, laboratory updates, and emerging scientific discussions beyond traditional literature databases. Features programmable search through Custom Search JSON API and web scraping capabilities for systematic information gathering, real-time trend monitoring, and discovery of preliminary research findings shared on institutional websites, scientific blogs, and research organization announcements before formal publication.

- **[Zenodo: Open Science Repository](https://zenodo.org/)** `CERN & OpenAIRE`

  > Zenodo is a general-purpose open research repository operated by CERN storing all forms of research outputs including datasets, publications, software, presentations, posters, images, videos, and code across all scientific disciplines. Accepts uploads of any size (50GB default per dataset with higher quotas available) and format without restrictions, providing long-term preservation in CERN Data Centre with automatic DOI assignment for citation, versioning support, GitHub integration, and flexible access control (open, embargoed, restricted, closed). Agents utilize Zenodo for accessing supplementary datasets from publications, retrieving research software packages, downloading replication data for computational studies, and programmatically querying metadata via OAI-PMH API. Particularly valuable for accessing domain-specific communities (e.g., biomedical data collections, computational biology workflows) and ensuring reproducibility through preservation of exact analysis code and intermediate data files.

### 知识库总结表

| 数据库                     | 副标题                                                     | 组织                                  | 类别                         | 链接                                                          |
| ---------------------------- | ------------------------------------------------------------ | ---------------------------------------------- | -------------------------------- | ------------------------------------------------------------ |
| **ClinVar**                  | 临床相关变异解释的公共档案 | NCBI                                           | 基因组学和临床数据库     | https://www.ncbi.nlm.nih.gov/clinvar/                        |
| **MyGene2**                  | 共享信息以了解基因和罕见疾病 | University of Washington                       | 基因组学和临床数据库     | https://mygene2.org/                                         |
| **MPD**                      | 小鼠表型数据库                                       | The Jackson Laboratory                         | 基因组学和临床数据库     | https://www.jax.org/research-and-faculty/resources/mouse-phenome-database |
| **gnomAD**                   | 基因组聚合数据库                                  | Broad Institute                                | 基因组学和临床数据库     | https://gnomad.broadinstitute.org/                           |
| **UCSC Genome Browser**      | 可视化和分析基因组组装的集成工具 | UC Santa Cruz Genomics Institute               | 基因组学和临床数据库     | https://genome.ucsc.edu/                                     |
| **COSMIC**                   | 癌症体细胞突变目录                     | Wellcome Sanger Institute                      | 基因组学和临床数据库     | https://cancer.sanger.ac.uk/cosmic                           |
| **Open Targets Genetics**    | 系统性药物靶点识别和优先级排序     | Open Targets                                   | 基因组学和临床数据库     | https://genetics.opentargets.org/                            |
| **RegulomeDB**               | 人类基因组中调控变异的注释        | Stanford University                            | 基因组学和临床数据库     | http://www.regulomedb.org/                                   |
| **GEO**                      | 基因表达综合库                                      | NCBI                                           | 基因组学和临床数据库     | https://www.ncbi.nlm.nih.gov/geo/                            |
| **SRA**                      | 序列读取档案                                        | NCBI                                           | 基因组学和临床数据库     | https://www.ncbi.nlm.nih.gov/sra/                            |
| **ENCODE**                   | DNA 元件百科全书                                 | NHGRI                                          | 基因组学和临床数据库     | https://www.encodeproject.org/                               |
| **NCBI RefSeq**              | 参考序列数据库                                  | NCBI                                           | 基因组学和临床数据库     | https://www.ncbi.nlm.nih.gov/refseq/                         |
| **Ensembl**                  | 基因组浏览器和注释系统                         | EMBL-EBI                                       | 基因组学和临床数据库     | http://www.ensembl.org/index.html                            |
| **PDB**                      | 蛋白质数据库                                            | RCSB                                           | 分子和结构数据库 | https://www.rcsb.org/                                        |
| **miRBase**                  | MicroRNA 数据库                                        | University of Manchester                       | 分子和结构数据库 | https://www.mirbase.org/                                     |
| **UniProt**                  | 通用蛋白质资源                                   | UniProt Consortium                             | 分子和结构数据库 | https://www.uniprot.org/                                     |
| **AlphaFold DB**             | AlphaFold 蛋白质结构数据库                         | DeepMind & EMBL-EBI                            | 分子和结构数据库 | https://alphafold.ebi.ac.uk/                                 |
| **InterPro**                 | 蛋白质序列分析和分类                 | EMBL-EBI                                       | 分子和结构数据库 | https://www.ebi.ac.uk/interpro/                              |
| **KEGG**                     | 京都基因与基因组百科全书                      | Kanehisa Laboratories                          | 分子和结构数据库 | https://www.genome.jp/kegg/                                  |
| **Reactome**                 | 通路知识库                                        | Reactome                                       | 分子和结构数据库 | https://reactome.org/                                        |
| **JASPAR**                   | 转录因子结合谱的开放获取数据库 | JASPAR Consortium                              | 分子和结构数据库 | https://jaspar.genereg.net/                                  |
| **BindingDB**                | 测量结合亲和力数据库                      | UC San Diego                                   | 分子和结构数据库 | https://www.bindingdb.org/                                   |
| **DrugBank**                 | 综合生物信息学和化学信息学资源    | University of Alberta                          | 分子和结构数据库 | https://www.drugbank.com/                                    |
| **CellxGene**                | 单细胞数据浏览器和普查                         | Chan Zuckerberg Initiative                     | 专门的生物医学数据库 | https://cellxgene.cziscience.com/                            |
| **IUCN Red List**            | IUCN 受威胁物种红色名录                      | International Union for Conservation of Nature | 专门的生物医学数据库 | https://www.iucnredlist.org/                                 |
| **Human Microbiome Project** | 数据分析与协调中心                        | National Institutes of Health                  | 专门的生物医学数据库 | https://commonfund.nih.gov/hmp                               |
| **Addgene**                  | 非营利性质粒库                                 | Addgene                                        | 专门的生物医学数据库 | https://www.addgene.org/                                     |
| **10X Genomics Datasets**    | 来自 Chromium 单细胞和空间基因组学平台的参考数据集 | 10x Genomics                                   | 专门的生物医学数据库 | https://www.10xgenomics.com/datasets                         |
| **PubMed**                   | 免费生物医学文献搜索引擎                     | NCBI                                           | 科学文献            | https://pubmed.ncbi.nlm.nih.gov/                             |
| **Google Scholar**           | 站在巨人的肩膀上                             | Google                                         | 科学文献            | https://scholar.google.com/                                  |
| **bioRxiv**                  | 生物学预印本服务器                              | Cold Spring Harbor Laboratory                  | 科学文献            | https://www.biorxiv.org/                                     |
| **Google Search**            | 搜索世界信息                               | Google                                         | 科学文献            | https://www.google.com/                                      |
| **Zenodo**                   | 开放科学知识库                                      | CERN & OpenAIRE                                | 科学文献            | https://zenodo.org/                                          |

## 4. 工具 (Tools)

本目录为 AI 智能体系统执行生物信息学分析工作流提供了计算工具和软件。工具按分析功能组织：核心 NGS 管道（质量控制、比对、格式转换）、基因组组装和变异分析（组装、变异调用、注释）、转录组学和表达分析（bulk/单细胞/空间 RNA-seq）、表观基因组学和调控分析（ChIP-seq、ATAC-seq、甲基化）、多组学整合（跨平台方法）、特定技术工具（蛋白质组学、宏基因组学、长读长、小 RNA）、AI/ML 基础模型（结构预测、序列模型、单细胞基础）以及可视化和探索（基因组浏览器、交互式查看器）。

**[TODO]** 未来版本将包含更多针对新兴技术（长读长 RNA-seq、多模态成像、蛋白质基因组学）的工具组合。

### 核心NGS管道

- **[FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)** `Babraham Bioinformatics`
  > A quality control tool for high-throughput sequencing data that generates comprehensive QC reports including per-base quality scores, sequence length distribution, adapter contamination, and overrepresented sequences. Available as a command-line tool or GUI application with visual HTML reports. AI agents can use FastQC to automatically assess data quality before alignment, identify problematic samples requiring trimming, and determine optimal preprocessing parameters based on quality metrics.

- **[Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)** `Usadel Lab`
  > A flexible read trimming tool for Illumina NGS data that performs adapter removal, quality-based trimming, and filtering of low-quality reads. Supports paired-end and single-end data with configurable parameters for sliding window trimming, minimum length filtering, and quality thresholds. AI agents can invoke Trimmomatic to clean raw sequencing data based on FastQC reports, automatically determine optimal trimming parameters, and prepare high-quality reads for alignment workflows.

- **[BWA: Burrows-Wheeler Aligner](http://bio-bwa.sourceforge.net/)** `Heng Li Lab`
  > A fast and memory-efficient aligner for mapping short DNA sequences (70bp-1Mbp) against large reference genomes using the Burrows-Wheeler Transform algorithm. Includes three algorithms: BWA-backtrack for reads <100bp, BWA-SW for longer reads, and BWA-MEM (most commonly used) for 70bp-1Mbp sequences with superior performance on split alignments. AI agents can use BWA-MEM for whole-genome sequencing alignment, automatically select appropriate algorithms based on read length, and generate sorted BAM files for variant calling pipelines.

- **[STAR: Spliced Transcripts Alignment to a Reference](https://github.com/alexdobin/STAR)** `Alexander Dobin`
  > An ultrafast RNA-seq aligner designed to detect splice junctions with high accuracy, achieving speeds >100 million reads/hour. Uses suffix array-based mapping with 2-pass alignment mode for improved junction detection. Outputs include aligned BAM files, splice junction tables, and gene-level read counts. AI agents can execute STAR for transcriptome alignment tasks, automatically configure genome indexes, detect novel splice variants, and generate count matrices for differential expression analysis.

- **[Minimap2](https://github.com/lh3/minimap2)** `Heng Li`
  > A versatile alignment tool optimized for long-read sequencing data (PacBio, Oxford Nanopore) and assembly-to-assembly comparison, supporting read lengths from kilobases to megabases. Features include fast all-vs-all alignment, spliced alignment for long-read RNA-seq, and accurate mapping for noisy long reads. AI agents can use Minimap2 for long-read genomic/transcriptomic alignment, structural variant detection workflows, and rapid comparison of draft genome assemblies.

- **[Samtools](http://www.htslib.org/)** `Genome Research Ltd`
  > A comprehensive suite of utilities for manipulating SAM/BAM/CRAM format alignments, providing core functionalities including sorting, indexing, merging, filtering, and format conversion. Supports parallel processing, CRAM compression (up to 60% size reduction vs BAM), and region-specific data extraction. AI agents can invoke Samtools for standard BAM file operations (sort, index, merge, view), calculate alignment statistics, extract specific genomic regions, and prepare files for downstream variant calling or visualization.

- **[BEDTools](https://bedtools.readthedocs.io/)** `Quinlan Lab`
  > A powerful toolset for genome arithmetic operations on genomic intervals (BED, GFF, VCF formats), enabling tasks like intersection, merge, complement, and coverage calculations across genomic regions. Supports operations on millions of intervals with high efficiency. AI agents can use BEDTools to identify overlapping features between datasets, calculate coverage statistics, merge adjacent intervals, find closest features, and perform complex genomic interval queries essential for ChIP-seq, ATAC-seq, and variant analysis workflows.

- **[Picard](https://broadinstitute.github.io/picard/)** `Broad Institute`
  > A suite of Java-based command-line tools for manipulating high-throughput sequencing data and formats, including SAM/BAM/CRAM, VCF, and various quality metrics. Key functions include marking PCR duplicates, collecting alignment metrics, fixing mate-pair information, and converting between file formats. AI agents can invoke Picard to mark duplicate reads before variant calling, validate BAM file integrity, collect comprehensive alignment and insert size metrics, and ensure data quality standards for GATK-based analysis pipelines.


### 基因组组装和变异分析

- **[SPAdes: St. Petersburg genome Assembler](https://github.com/ablab/spades)** `Center for Algorithmic Biotechnology, St. Petersburg State University`
  
  > A versatile de novo genome assembler designed for small genomes (bacteria, fungi) using short-read Illumina data, with specialized modes for single-cell, metagenomic, plasmid, and RNA-seq assembly. Uses multi-sized de Bruijn graphs and built-in error correction to handle uneven coverage and sequencing errors. AI agents can invoke SPAdes for bacterial genome assembly tasks, automatically select assembly modes based on data type, iteratively optimize k-mer sizes, and integrate with downstream annotation pipelines.
  
- **[Flye](https://github.com/fenderglass/Flye)** `Kolmogorov Lab`
  > A long-read de novo assembler optimized for PacBio and Oxford Nanopore data, capable of assembling genomes ranging from bacterial to mammalian scale using repeat graph-based algorithms. Handles high error rates in raw long reads and produces accurate assemblies with excellent contiguity. AI agents can use Flye for long-read assembly workflows, automatically configure parameters based on coverage and read length, perform metagenomic assembly, and generate high-quality reference genomes for variant calling.

- **[Canu](https://github.com/marbl/canu)** `Koren & Walenz Labs`
  > A comprehensive long-read assembly toolkit for high-noise single-molecule sequencing (PacBio, Oxford Nanopore), featuring adaptive k-mer weighting, aggressive error correction, and optimized algorithms for large eukaryotic genomes. Includes modules for read correction, trimming, and assembly with support for distributed computing. AI agents can execute Canu for complex genome assembly projects, manage resource-intensive computations across HPC clusters, tune sensitivity parameters for repetitive regions, and produce chromosome-scale assemblies.

- **[QUAST: QUality ASsessment Tool](https://github.com/ablab/quast)** `Center for Algorithmic Biotechnology`
  > A comprehensive assembly quality evaluation tool that computes metrics including N50, misassemblies, genome fraction coverage, and gene completeness when reference genomes are available. Generates interactive HTML reports with visualizations and supports metagenomic assembly evaluation. AI agents can invoke QUAST to automatically assess assembly quality, compare multiple assembly strategies, identify potential misassemblies, and select optimal assembly parameters based on quantitative metrics.

- **[Bandage: Bioinformatics Application for Navigating De novo Assembly Graphs Easily](https://github.com/rrwick/Bandage)** `Ryan Wick`
  > A GUI-based visualization tool for exploring de Bruijn graphs and assembly graphs from tools like SPAdes and Velvet, enabling interactive inspection of graph structure, repeat regions, and assembly paths. Supports BLAST searches within graphs and custom graph coloring based on coverage or sequence identity. AI agents can leverage Bandage's command-line interface to generate assembly graph images, identify problematic regions in assemblies, visualize structural variants, and guide targeted assembly refinement.

- **[GATK: Genome Analysis Toolkit](https://gatk.broadinstitute.org/)** `Broad Institute`
  > The gold-standard toolkit for variant discovery from high-throughput sequencing data, implementing best-practice workflows for germline and somatic variant calling including SNPs, indels, and CNVs. Features include base quality score recalibration, variant quality score recalibration, and joint genotyping across cohorts. AI agents can execute GATK workflows for clinical-grade variant calling, automatically apply VQSR filtering, perform multi-sample joint calling for population studies, and integrate with downstream annotation tools for variant interpretation.

- **[bcftools](http://samtools.github.io/bcftools/)** `Genome Research Ltd`
  > A comprehensive toolkit for VCF/BCF file manipulation and variant calling, providing utilities for filtering, merging, annotating, and calling variants from aligned sequencing data. Features highly optimized algorithms for large-scale population genomics with support for multi-sample calling. AI agents can use bcftools for rapid variant calling on BAM files, perform complex VCF filtering operations, merge multi-sample VCFs, calculate population statistics, and extract specific variants or samples for downstream analysis.

- **[Manta](https://github.com/Illumina/manta)** `Illumina`
  > A structural variant (SV) caller designed to detect deletions, insertions, inversions, and translocations from paired-end sequencing data with high sensitivity and specificity. Uses paired and split-read evidence with local assembly refinement to accurately resolve breakpoints. AI agents can invoke Manta for detecting large genomic rearrangements, integrate SV calls with SNP/indel data for comprehensive variant analysis, identify cancer-related fusion genes, and prioritize pathogenic structural variants in clinical sequencing.

- **[FreeBayes](https://github.com/freebayes/freebayes)** `Erik Garrison`
  
  > A Bayesian genetic variant detector designed to find SNPs, indels, and complex variants in populations, featuring haplotype-based variant calling without requiring read realignment. Supports both diploid and polyploid genomes with flexible ploidy settings. AI agents can use FreeBayes for population-scale variant calling, detect complex multi-nucleotide polymorphisms, perform somatic mutation detection in cancer samples, and generate high-quality variant calls from targeted sequencing panels.
  
- **[Pindel](https://github.com/genome/pindel)** `Wellcome Trust Sanger Institute`
  
  > A pattern-growth approach to detect breakpoints of large deletions, medium-sized insertions, inversions, and tandem duplications using paired-end short reads. Excels at detecting mid-size indels (1bp-10kb) often missed by standard variant callers. AI agents can execute Pindel to complement GATK/bcftools calls with improved indel detection, identify pathogenic deletion/insertion variants in clinical exomes, and characterize complex structural rearrangements in cancer genomes.
  
- **[VEP: Variant Effect Predictor](https://www.ensembl.org/vep)** `EMBL-EBI / Ensembl`
  
  > The most comprehensive variant annotation tool that predicts functional consequences of genomic variants on genes, transcripts, and proteins, integrating 30+ prediction algorithms (SIFT, PolyPhen, CADD) and clinical databases (ClinVar, gnomAD). Available as web interface, command-line tool, or REST API with support for custom annotations. AI agents can invoke VEP to annotate VCF files with transcript consequences, retrieve population frequencies, predict deleteriousness scores, identify clinically relevant variants, and generate structured reports for variant interpretation.
  
- **[SnpEff](https://pcingola.github.io/SnpEff/)** `Pablo Cingolani`
  
  > A fast variant annotation and functional effect prediction tool that categorizes variants by impact (HIGH, MODERATE, LOW, MODIFIER) and provides gene-based annotations, amino acid changes, and codon degeneracy information. Supports 38,000+ genomes with pre-built databases. AI agents can use SnpEff for rapid batch variant annotation, prioritize high-impact variants, generate summary statistics of variant distributions across functional categories, and integrate with Galaxy workflows for automated variant analysis pipelines.
  
- **[ANNOVAR](https://annovar.openbioinformatics.org/)** `Kai Wang Lab`
  
  > A versatile variant annotation tool that integrates gene-based, region-based, and filter-based annotations from hundreds of databases including RefSeq, UCSC, dbSNP, 1000 Genomes, and custom datasets. Supports flexible custom database integration and table-based output formats. AI agents can execute ANNOVAR to annotate variants with multiple database sources, filter variants based on population frequency and predicted pathogenicity, generate tab-delimited reports for clinical review, and customize annotation workflows with disease-specific databases.
### 转录组学和表达分析

- **[DESeq2](https://bioconductor.org/packages/DESeq2/)** `Michael Love, Simon Anders, Wolfgang Huber`

  > The most widely-used R/Bioconductor package for differential gene expression analysis from count data, implementing negative binomial generalized linear models with robust variance estimation and empirical Bayes shrinkage. Handles complex experimental designs with multiple factors and supports likelihood ratio tests for model comparisons. AI agents can execute DESeq2 to identify differentially expressed genes between conditions, automatically detect outliers, normalize count data accounting for library size and composition, generate publication-quality MA plots and volcano plots, and export results with adjusted p-values for downstream pathway analysis.

- **[edgeR](https://bioconductor.org/packages/edgeR/)** `Gordon Smyth Lab`

  > A powerful R/Bioconductor package for differential expression analysis using empirical Bayes methods and generalized linear models, particularly effective for experiments with small sample sizes. Features quasi-likelihood F-tests and robust variance modeling for complex experimental designs. AI agents can use edgeR for differential expression analysis with limited replicates, perform multi-factor designs with interaction terms, conduct gene set testing with camera/roast methods, and integrate with limma-voom for RNA-seq data normalization and precision weighting.

- **[StringTie](https://ccb.jhu.edu/software/stringtie/)** `Johns Hopkins University Center for Computational Biology`

  > A fast and efficient transcript assembler that reconstructs full-length transcripts from RNA-seq alignments, quantifies expression levels, and identifies novel isoforms and alternative splicing events. Uses network flow algorithms and optional reference-guided assembly for improved accuracy. AI agents can invoke StringTie to assemble transcripts de novo or with reference guidance, quantify gene and transcript-level expression simultaneously, detect novel splice junctions, merge assemblies across multiple samples, and generate count matrices compatible with DESeq2/edgeR.

- **[Salmon](https://combine-lab.github.io/salmon/)** `Rob Patro Lab`

  > An ultra-fast transcript quantification tool that estimates abundance from RNA-seq reads without alignment, using dual-phase parallel inference and lightweight mapping for 10-100x speed improvement over traditional methods. Produces accurate TPM and estimated counts with uncertainty quantification. AI agents can execute Salmon for rapid transcript-level quantification, bypass time-consuming alignment steps, automatically detect and correct for sequence-specific biases, generate bootstrap samples for uncertainty estimation, and produce count matrices ready for differential expression analysis in minutes rather than hours.

- **[HTSeq](https://htseq.readthedocs.io/)** `Simon Anders Lab`

  > A Python framework for processing high-throughput sequencing data, most commonly used via htseq-count for generating gene-level read counts from aligned BAM files with flexible feature assignment rules. Handles paired-end data and supports multiple overlap resolution modes. AI agents can use HTSeq to count reads overlapping genomic features from BAM files, apply different counting modes (union, intersection-strict, intersection-nonempty) based on experimental needs, process large BAM files efficiently, and generate count tables for downstream differential expression analysis.

- **[Scanpy](https://scanpy.readthedocs.io/)** `Theis Lab`

  > A comprehensive Python toolkit for analyzing single-cell RNA-seq data, providing scalable implementations of preprocessing, clustering, trajectory inference, and visualization methods for datasets with millions of cells. Integrates with AnnData format and includes PAGA for topology inference. AI agents can execute Scanpy workflows to normalize and filter single-cell data, identify highly variable genes, perform dimensionality reduction (PCA, UMAP, t-SNE), cluster cells using Leiden/Louvain algorithms, infer developmental trajectories, identify marker genes, and visualize results with publication-ready plots.

- **[Seurat](https://satijalab.org/seurat/)** `Satija Lab`

  > The most popular R toolkit for single-cell RNA-seq analysis, offering comprehensive workflows for QC, normalization, integration, clustering, and differential expression with over 100,000 citations. Version 5 introduces scalable on-disk analysis and improved multi-modal integration capabilities. AI agents can invoke Seurat to process 10X Genomics data, integrate multiple datasets using anchors or harmony, perform SCTransform normalization, identify cell types using reference-based annotation, analyze spatial transcriptomics with Visium, and generate interactive visualizations with customizable UMAP/t-SNE plots.

- **[Cell Ranger](https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/what-is-cell-ranger)** `10X Genomics`

  > The official analysis pipeline for processing 10X Genomics single-cell and spatial transcriptomics data, handling demultiplexing, barcode processing, alignment, UMI counting, and cell calling with optimized algorithms for 10X chemistry. Outputs include feature-barcode matrices and quality metrics. AI agents can execute Cell Ranger to process raw BCL files from 10X experiments, automatically detect cell barcodes and UMIs, align reads to reference genomes, generate filtered gene-barcode matrices, aggregate multiple samples, and produce web-based QC summary reports for immediate quality assessment.

- **[scVI: Single-cell Variational Inference](https://scvi-tools.org/)** `Yosef Lab`

  > A deep learning framework for probabilistic modeling of single-cell omics data using variational autoencoders, enabling batch correction, imputation, dimensionality reduction, and integration of multi-modal datasets (RNA, ATAC, protein). Includes models like scVI, scANVI for annotation transfer, and totalVI for multi-modal analysis. AI agents can leverage scVI to remove batch effects while preserving biological variation, impute dropout events, integrate datasets across technologies and species, perform probabilistic cell type annotation, and generate biologically meaningful low-dimensional embeddings for downstream analysis.

- **[scGPT](https://scgpt.readthedocs.io/)** `Cui Lab`

  > A foundation model for single-cell biology that uses transformer architecture pre-trained on 33 million cells, enabling zero-shot cell type annotation, gene network inference, perturbation prediction, and multi-batch integration. Learns generalizable gene representations across diverse cell types and tissues. AI agents can invoke scGPT for transfer learning on new datasets, predict gene expression changes under perturbations, annotate rare cell types without reference data, infer gene regulatory relationships, and perform cross-species or cross-tissue analysis leveraging pre-trained biological knowledge.

- **[Squidpy](https://squidpy.readthedocs.io/)** `Theis Lab`

  > A Python toolkit for spatial molecular data analysis that extends Scanpy with methods for spatial statistics, tissue structure analysis, ligand-receptor interaction inference, and image feature extraction. Supports multiple spatial technologies including Visium, Slide-seq, and imaging-based methods. AI agents can use Squidpy to compute spatial neighbor graphs, identify spatially variable genes, perform spatial autocorrelation analysis, extract morphological features from H&E images using deep learning, infer cell-cell communication through ligand-receptor databases, and visualize spatial patterns with tissue context.

- **[Tangram](https://tangram-sc.readthedocs.io/)** `Regev Lab`

  > A deep learning method for mapping single-cell or cell type signatures to spatial locations in tissues, enabling spatial deconvolution and cross-technology data integration. Uses neural network optimization to align gene expression profiles while preserving spatial coherence. AI agents can execute Tangram to map scRNA-seq data onto spatial transcriptomics slides, deconvolve cell type compositions at spatial locations, transfer annotations from single-cell atlases to spatial data, predict spatial locations of cell types not captured by spatial technology, and integrate multi-modal spatial datasets.

- **[STUtility](https://ludvigla.github.io/STUtility_web_site/)** `Lundeberg Lab`

  > An R package for analyzing and visualizing spatially resolved transcriptomics data, particularly Visium, with tools for tissue detection, image alignment, spatial feature identification, and integration with Seurat. Provides interactive visualization of tissue sections with gene expression overlays. AI agents can invoke STUtility to align tissue images with spot coordinates, automatically detect tissue regions, identify spatially variable genes using spatial autocorrelation, perform region-based differential expression, integrate spatial data with scRNA-seq references, and generate publication-quality spatial plots with anatomical context.

- **[SPATA2](https://themilolab.github.io/SPATA2/)** `Kuppe Lab`

  > An R framework for comprehensive spatial transcriptomics analysis with emphasis on trajectory inference, surface modeling, and interactive visualization of spatial patterns. Features advanced spatial statistics and dimensionality reduction tailored for tissue architecture. AI agents can use SPATA2 to infer spatial trajectories across tissue regions, model gene expression as continuous surfaces, identify spatial gradients and transition zones, perform spatial clustering with anatomical constraints, and create interactive 3D visualizations of gene expression landscapes in tissue context.

- **[Giotto](https://giottosuite.readthedocs.io/)** `Yuan Lab`

  > A comprehensive toolbox for spatial transcriptomics and multiplexed imaging data analysis in both R and Python, offering methods for spatial statistics, cell proximity analysis, ligand-receptor interaction modeling, and spatial enrichment. Supports over 10 spatial data types including Visium, Slide-seq, MERFISH, and seqFISH. AI agents can execute Giotto to create spatial expression maps, perform spatial co-expression network analysis, identify spatial domains using hidden Markov random fields, calculate spatial enrichment scores for cell type interactions, infer intercellular communication patterns, and integrate multi-resolution spatial datasets.

### 表观基因组学和调控分析

- **[MACS2: Model-based Analysis of ChIP-Seq](https://github.com/macs3-project/MACS)** `Tao Liu Lab`

  > The most widely-used peak caller for ChIP-seq and ATAC-seq data, using dynamic Poisson distribution to model local biases and identify enriched regions with high sensitivity and specificity. Supports broad peak calling for histone marks and narrow peak calling for transcription factors. AI agents can invoke MACS2 to call peaks from treatment vs control BAM files, automatically estimate fragment size and background, detect broad domains for histone modifications, generate bedGraph and bigWig files for visualization, calculate fold enrichment and FDR values, and produce summit files for motif analysis.

- **[HOMER: Hypergeometric Optimization of Motif EnRichment](http://homer.ucsd.edu/homer/)** `Christopher Benner`

  > A comprehensive suite for motif discovery, ChIP-seq analysis, and genomic annotation that identifies enriched DNA sequence motifs in regulatory regions using optimized scoring algorithms. Includes tools for peak annotation, differential binding analysis, and histone modification analysis. AI agents can execute HOMER to discover de novo motifs in peak regions, annotate peaks with nearest genes and genomic features, find known motif instances across the genome, perform differential peak analysis between conditions, create tag directories for visualization, and generate comprehensive HTML reports with motif logos and enrichment statistics.

- **[MEME Suite](https://meme-suite.org/)** `Timothy Bailey Lab`

  > A collection of tools for motif discovery and analysis, including MEME for de novo motif finding, FIMO for scanning sequences with known motifs, and TOMTOM for motif comparison. Features advanced algorithms for gapped motifs and position-specific scoring matrices. AI agents can use MEME to discover ungapped or gapped motifs in DNA/protein sequences, scan genomes for motif occurrences with FIMO, compare discovered motifs against databases with TOMTOM, analyze motif spacing and orientation, perform motif enrichment analysis, and generate publication-quality sequence logos with statistical significance metrics.

- **[Bismark](https://www.bioinformatics.babraham.ac.uk/projects/bismark/)** `Babraham Bioinformatics`

  > A specialized aligner for bisulfite-treated sequencing data that maps reads and extracts DNA methylation information, handling both directional and non-directional libraries with support for paired-end reads. Performs simultaneous alignment and methylation calling with context-specific resolution (CpG, CHG, CHH). AI agents can invoke Bismark to align bisulfite-converted reads to reference genomes, extract methylation calls at single-base resolution, generate methylation reports with coverage statistics, perform deduplication for WGBS data, create bedGraph files for genome browser visualization, and quantify global methylation patterns across genomic contexts.

- **[deepTools](https://deeptools.readthedocs.io/)** `Ramírez Lab`

  > A comprehensive toolkit for exploring and visualizing deep-sequencing data, providing utilities for BAM file processing, normalization, heatmap generation, and quality control across ChIP-seq, ATAC-seq, and RNA-seq experiments. Features include multiBamSummary, plotHeatmap, and computeMatrix for creating publication-ready figures. AI agents can use deepTools to generate correlation plots between samples, create signal heatmaps around genomic features (TSS, gene bodies, peaks), compute coverage tracks with various normalization methods (RPKM, CPM, RPGC), assess fragment size distributions, perform GC-bias correction, and visualize genome-wide signal patterns with customizable color schemes.

- **[ATACseqQC](https://bioconductor.org/packages/ATACseqQC/)** `Jianhong Ou, Julie Zhu`

  > An R/Bioconductor package specifically designed for quality control and analysis of ATAC-seq data, assessing fragment size distribution, transcription start site enrichment, nucleosome positioning, and library complexity. Provides diagnostic plots for troubleshooting experimental issues. AI agents can execute ATACseqQC to evaluate ATAC-seq data quality by checking fragment size periodicity (nucleosome ladder), calculate TSS enrichment scores, visualize insert size distributions, assess promoter/enhancer enrichment, detect mitochondrial contamination, identify low-quality libraries requiring re-sequencing, and generate comprehensive QC reports with standardized metrics.

- **[ChromHMM](http://compbio.mit.edu/ChromHMM/)** `Ernst & Kellis Lab`

  > A hidden Markov model-based method for chromatin state discovery and characterization from histone modification ChIP-seq data, learning and annotating combinatorial chromatin states (promoters, enhancers, insulators, heterochromatin) genome-wide. Produces browser-ready tracks and emission/transition parameters. AI agents can invoke ChromHMM to learn chromatin state models from multiple histone marks, automatically segment genomes into functional states, compare chromatin landscapes across cell types or conditions, identify state transitions during differentiation, annotate enhancers and promoters based on chromatin signatures, and generate genome browser tracks showing predicted regulatory elements with biological interpretations.

### 多组学整合

- **[MOFA+: Multi-Omics Factor Analysis](https://biofam.github.io/MOFA2/)** `Ricard Argelaguet, Britta Velten`

  > A statistical framework for unsupervised integration of multi-omics data using group factor analysis, identifying latent factors that explain coordinated variation across transcriptomics, epigenomics, proteomics, and other molecular layers. Handles missing data and supports multi-group comparisons. AI agents can execute MOFA+ to integrate multi-modal single-cell data, identify shared and unique sources of variation across omics layers, perform variance decomposition to quantify each factor's contribution, cluster samples based on latent factors, impute missing values across incomplete datasets, and visualize coordinated molecular changes driving biological processes.

- **[Seurat V5](https://satijalab.org/seurat/)** `Satija Lab`

  > The latest version of Seurat featuring scalable multi-modal integration through bridge integration and sketch-based analysis for million-cell datasets, supporting simultaneous analysis of RNA, ATAC, protein, and spatial data. Introduces on-disk data storage and streamlined integration workflows. AI agents can invoke Seurat V5 to integrate datasets across technologies using bridge integration anchors, perform sketch-based analysis on very large datasets (>1M cells), analyze CITE-seq data with weighted nearest neighbor (WNN) graphs, map query datasets to reference atlases, integrate spatial and single-cell data, and leverage BPCells for memory-efficient processing of massive datasets.

- **[MultiVI](https://docs.scvi-tools.org/en/stable/user_guide/models/multivi.html)** `Gayoso, Steier et al.`

  > A deep generative model within scvi-tools for joint analysis of single-cell RNA-seq and ATAC-seq data, learning a unified latent representation that captures both gene expression and chromatin accessibility while accounting for technical noise and batch effects. Uses amortized inference for scalability. AI agents can use MultiVI to integrate paired or unpaired scRNA-seq and scATAC-seq datasets, infer joint cell embeddings capturing both modalities, impute missing modalities (predict gene expression from ATAC or vice versa), remove batch effects while preserving biological variation, perform differential accessibility and expression analysis jointly, and transfer cell type annotations across modalities.

- **[totalVI](https://docs.scvi-tools.org/en/stable/user_guide/models/totalvi.html)** `Gayoso, Steier et al.`

  > A probabilistic model for joint analysis of CITE-seq data (RNA + surface proteins) using variational autoencoders, modeling the technical characteristics of both modalities including protein background and RNA dropout events. Enables denoised protein quantification and integrated clustering. AI agents can execute totalVI to jointly analyze gene expression and protein abundance from CITE-seq experiments, remove protein background noise and ambient RNA contamination, generate denoised protein expression matrices, perform integrated clustering using both modalities, conduct differential expression analysis for genes and proteins simultaneously, and impute missing protein measurements in datasets lacking ADT data.

- **[LIGER: Linked Inference of Genomic Experimental Relationships](https://github.com/welch-lab/liger)** `Joshua Welch Lab`

  > An integrative non-negative matrix factorization (iNMF) framework for identifying shared and dataset-specific features across multi-modal single-cell datasets, particularly effective for integrating scRNA-seq, scATAC-seq, spatial transcriptomics, and DNA methylation data. Preserves biological variation while removing batch effects. AI agents can invoke LIGER to integrate diverse single-cell modalities using iNMF, identify shared metagene programs and dataset-specific factors, align datasets from different technologies or species, perform multi-dataset trajectory inference, integrate spatial and non-spatial data, quantify gene loading contributions across factors, and visualize integrated data with joint UMAP embeddings.

- **[Scissor](https://github.com/sunduanchen/Scissor)** `Duan Chen Sun`

  > A method for phenotype-associated single-cell subpopulation identification by correlating bulk tissue phenotypes (survival, drug response, clinical outcomes) with single-cell expression profiles using regularized regression. Bridges bulk genomics and single-cell data to identify disease-relevant cell populations. AI agents can execute Scissor to identify cell subpopulations associated with patient survival outcomes, link single-cell states to bulk tumor phenotypes, discover therapy-resistant cell populations from treatment response data, correlate cellular states with continuous clinical variables, prioritize cell types for therapeutic targeting based on phenotypic associations, and integrate TCGA bulk data with single-cell atlases for clinical insights.

### 特定技术工具

- **[OpenMS](https://www.openms.de/)** `OpenMS Team`

  > A comprehensive open-source framework for mass spectrometry data analysis, providing tools for peak picking, feature detection, peptide identification, protein quantification, and metabolomics workflows. Supports multiple MS platforms and formats (mzML, mzXML) with TOPP tools for command-line processing. AI agents can execute OpenMS pipelines to process raw MS/MS data, perform label-free quantification, identify post-translational modifications, conduct targeted proteomics analysis with SRM/MRM data, integrate with database search engines (Mascot, X!Tandem), and generate standardized outputs for downstream statistical analysis.

- **[MaxQuant](https://www.maxquant.org/)** `Jürgen Cox, Max Planck Institute`

  > A widely-used quantitative proteomics software platform for analyzing large-scale MS data with Andromeda search engine, featuring label-free quantification (LFQ), isobaric labeling (TMT/iTRAQ), and match-between-runs for improved peptide identification. Includes Perseus for statistical analysis. AI agents can invoke MaxQuant to process Thermo, Bruker, and Sciex raw files, perform peptide identification with FDR control, quantify protein abundance across samples using LFQ or TMT, identify protein groups and isoforms, perform SILAC-based quantification, and export results to Perseus for differential expression analysis and pathway enrichment.

- **[ProteoWizard](http://proteowizard.sourceforge.net/)** `Spielberg Family Center for Applied Proteomics`

  > A suite of open-source tools for mass spectrometry data conversion and analysis, with msConvert for converting vendor-specific formats to open standards (mzML, mzXML) and tools for data filtering, peak picking, and quality control. Supports 30+ instrument vendors. AI agents can use ProteoWizard to convert proprietary MS formats (RAW, WIFF, .d) to open standards, apply spectral filters and centroiding during conversion, extract specific scan ranges or MS levels, perform batch conversion of large datasets, prepare data for downstream analysis in OpenMS/MaxQuant, and ensure data interoperability across proteomics platforms.

- **[QIIME2: Quantitative Insights Into Microbial Ecology](https://qiime2.org/)** `Caporaso Lab`

  > A comprehensive microbiome analysis platform for processing amplicon sequencing data (16S/18S/ITS), featuring plugin-based architecture for quality control, denoising with DADA2/Deblur, taxonomic classification, diversity analysis, and visualization. Supports reproducible workflows with artifact provenance tracking. AI agents can execute QIIME2 pipelines to denoise amplicon sequences into ASVs, assign taxonomy using trained classifiers (SILVA, Greengenes2), calculate alpha/beta diversity metrics, perform differential abundance testing with ANCOM-BC, generate interactive visualizations, conduct compositional data analysis, and integrate metadata for statistical testing of microbiome-phenotype associations.

- **[MetaPhlAn: Metagenomic Phylogenetic Analysis](https://github.com/biobakery/MetaPhlAn)** `Huttenhower Lab`

  > A computational tool for profiling microbial community composition from metagenomic shotgun sequencing using clade-specific marker genes, providing species-level taxonomic abundance without requiring assembly. Includes 1M+ markers from 100,000+ genomes in the latest mpa_vJan21 database. AI agents can invoke MetaPhlAn to rapidly profile taxonomic composition from WGS metagenomes, quantify relative abundances of bacteria, archaea, viruses, and eukaryotes, detect strain-level variation, merge profiles across samples for comparative analysis, integrate with HUMAnN for functional profiling, and generate abundance tables ready for statistical analysis.

- **[Kraken2](https://github.com/DerrickWood/kraken2)** `Derrick Wood & Steven Salzberg`

  > An ultrafast taxonomic classifier for metagenomic sequences using exact k-mer matches against a reference database, achieving classification speeds >100 times faster than previous methods while maintaining high accuracy. Supports custom database construction from RefSeq/GenBank. AI agents can execute Kraken2 to classify millions of reads in minutes, build custom databases for specific environments or pathogens, detect contamination in sequencing samples, identify microbes in clinical samples for pathogen detection, quantify taxonomic abundance with Bracken, and filter host-derived reads from metagenomic datasets.

- **[HUMAnN: HMP Unified Metabolic Analysis Network](https://huttenhower.sph.harvard.edu/humann/)** `Huttenhower Lab`

  > A pipeline for functional profiling of microbial communities from metagenomic sequencing, quantifying gene families, pathways, and metabolic potential using UniRef and MetaCyc databases. Integrates with MetaPhlAn for species-specific functional profiling. AI agents can invoke HUMAnN to profile metabolic pathways and gene family abundances, stratify functional contributions by organism, identify differentially abundant pathways between conditions, map to KEGG/MetaCyc/GO databases, normalize for sequencing depth and gene length, and generate pathway abundance tables for multi-omics integration.

- **[NanoPlot](https://github.com/wdecoster/NanoPlot)** `Wouter De Coster`

  > A visualization tool for quality control of long-read sequencing data from Oxford Nanopore and PacBio, generating comprehensive plots of read length distributions, quality scores, and yield statistics. Processes FASTQ, BAM, and sequencing summary files. AI agents can execute NanoPlot to assess long-read sequencing run quality, visualize read length N50 and distribution histograms, monitor quality scores over time during sequencing, identify failed pores or channels, compare multiple runs or barcodes, and generate publication-quality QC reports for evaluating library preparation and sequencing performance.

- **[Medaka](https://github.com/nanoporetech/medaka)** `Oxford Nanopore Technologies`

  > A neural network-based consensus tool for polishing draft genome assemblies from Oxford Nanopore reads, correcting systematic errors to improve base-level accuracy. Uses recurrent neural networks trained on specific basecaller versions and flowcell types. AI agents can invoke Medaka to polish draft assemblies after Flye/Canu, improve consensus accuracy to >99.9% for bacterial genomes, call variants from long-read alignments, select appropriate models based on basecaller version (Guppy/Dorado), perform iterative polishing rounds, and prepare assemblies for downstream annotation or comparative genomics.

- **[Racon](https://github.com/lbcb-sci/racon)** `Vaser et al.`

  > A rapid consensus module for polishing genome assemblies using long reads, employing partial order alignment (POA) graphs to correct errors in draft assemblies from noisy long-read data. Complements Medaka with faster but less accurate correction. AI agents can execute Racon for initial rapid polishing of draft assemblies, perform multiple polishing iterations to improve accuracy, integrate with minimap2 for alignment-based polishing, process large eukaryotic genomes efficiently, combine with Medaka for hybrid polishing strategies, and prepare assemblies for downstream variant calling or structural analysis.

- **[Clair3](https://github.com/HKU-BAL/Clair3)** `Luo et al.`

  > A deep learning-based small variant caller for long-read sequencing (ONT, PacBio HiFi) using pileup and full-alignment networks to achieve high precision and recall for SNPs and indels. Supports germline and somatic variant calling with model selection based on sequencing platform. AI agents can invoke Clair3 to call SNPs and indels from long-read BAM files, automatically select platform-specific models (ONT R9/R10, PacBio HiFi), perform trio-based variant calling with parent genotypes, call somatic mutations in tumor samples, generate high-quality VCF files with confidence scores, and integrate with short-read data for hybrid variant calling strategies.

- **[miRDeep2](https://github.com/rajewsky-lab/mirdeep2)** `Friedländer Lab`

  > A probabilistic algorithm for discovering novel microRNAs from small RNA sequencing data by analyzing read depth patterns and secondary structure compatibility with Dicer processing. Quantifies known and novel miRNA expression across samples. AI agents can execute miRDeep2 to identify novel miRNAs from small RNA-seq data, quantify expression of known miRNAs from miRBase, predict precursor structures and mature sequences, score candidates based on Dicer processing signatures, filter false positives using probabilistic models, and generate lists of high-confidence novel miRNAs for experimental validation.

- **[sRNAbench](https://bioinfo2.ugr.es/srnatoolbox/srnabench/)** `University of Granada`

  > A comprehensive web-based and standalone tool for small RNA-seq analysis, providing read processing, annotation against multiple databases (miRBase, piRNABank, tRNAs), differential expression analysis, and isomiR detection. Supports multiple species and custom reference libraries. AI agents can invoke sRNAbench to process and map small RNA reads, annotate different RNA biotypes (miRNA, piRNA, tRNA fragments, snoRNA), identify isomiRs and RNA modifications, perform differential expression analysis between conditions, predict novel miRNAs, and generate comprehensive reports with expression profiles across RNA categories.

- **[rMATS: replicate Multivariate Analysis of Transcript Splicing](http://rnaseq-mats.sourceforge.net/)** `Manabu Shen Lab`

  > A computational tool for detecting differential alternative splicing from RNA-seq data, identifying and quantifying five major splicing event types (SE, MXE, A5SS, A3SS, RI) with statistical significance testing across biological replicates. Handles both paired and unpaired sample comparisons. AI agents can execute rMATS to detect alternative splicing events from STAR-aligned BAM files, quantify inclusion levels (PSI values) for each event type, perform statistical testing for differential splicing between conditions, filter events by coverage and FDR thresholds, visualize splicing patterns with sashimi plots, and identify splicing changes associated with disease or developmental transitions.

- **[SUPPA: Super-fast Pipeline for Alternative Splicing](https://github.com/comprna/SUPPA)** `Eduardo Eyras Lab`

  > A lightweight tool for alternative splicing analysis from transcript quantification (Salmon, Kallisto), calculating PSI values and detecting differential splicing across conditions without requiring alignment files. Supports local and transcript-level splicing analysis. AI agents can invoke SUPPA to generate splicing event libraries from GTF annotations, calculate PSI values from transcript TPM estimates, perform fast differential splicing analysis across hundreds of samples, cluster samples by splicing profiles, identify splicing outliers, and analyze both local events and global transcript usage changes.

- **[LeafCutter](https://davidaknowles.github.io/leafcutter/)** `David Knowles & Jonathan Pritchard`

  > An annotation-free method for detecting and quantifying intron excision events from RNA-seq data, discovering novel and complex splicing patterns by clustering introns sharing splice sites. Performs differential splicing analysis with linear mixed models. AI agents can execute LeafCutter to discover intron clusters from junction reads without GTF annotation, quantify intron excision ratios across samples, detect differential intron usage between conditions, identify cryptic splicing events and novel exons, perform QTL mapping for splicing variation (sQTL), and visualize complex splicing patterns with leafviz browser.

### AI/ML基础模型

- **[AlphaFold](https://alphafold.ebi.ac.uk/)** `DeepMind / Google`

  > A revolutionary deep learning system for protein structure prediction that achieved near-experimental accuracy using transformer architecture and evolutionary information from multiple sequence alignments. AlphaFold2 database contains 200M+ predicted structures covering most known proteins. AI agents can invoke AlphaFold to predict 3D structures from amino acid sequences, access pre-computed structures from the database, estimate prediction confidence with pLDDT scores, identify intrinsically disordered regions, model protein complexes using AlphaFold-Multimer, and integrate predicted structures into drug discovery or protein engineering workflows.

- **[ESMFold](https://esmatlas.com/)** `Meta AI`

  > A language model-based protein structure prediction system trained on 250M+ protein sequences without requiring MSAs, enabling 60x faster prediction than AlphaFold while maintaining competitive accuracy. Uses ESM-2 protein language model embeddings for structure generation. AI agents can execute ESMFold to rapidly predict structures for orphan proteins lacking homologs, generate structures for metagenomic sequences, batch-process thousands of proteins efficiently, access the ESM Metagenomic Atlas with 600M+ predicted structures, predict structures for designed or mutated sequences, and integrate with protein design pipelines requiring fast iteration.

- **[RoseTTAFold](https://github.com/RosettaCommons/RoseTTAFold)** `David Baker Lab`

  > A three-track neural network for protein structure prediction combining 1D sequence, 2D distance maps, and 3D coordinate representations with attention mechanisms. Includes RoseTTAFold All-Atom for predicting structures with small molecules and modified residues. AI agents can invoke RoseTTAFold to predict protein structures with limited MSA depth, model protein-ligand complexes, predict structures with post-translational modifications, perform functional site prediction, integrate with Rosetta suite for structure refinement, and handle proteins with non-standard amino acids or cofactors.

- **[xTrimo](https://github.com/biomap-research/xTrimo)** `BioMap Research`

  > A multimodal foundation model pre-trained on genomic sequences, RNA secondary structures, and functional annotations, supporting tasks including variant effect prediction, regulatory element identification, RNA structure prediction, and gene expression forecasting. Uses transformer architecture with 1B+ parameters. AI agents can invoke xTrimo to predict pathogenicity of genetic variants, identify regulatory elements in non-coding regions, forecast gene expression changes from sequence, predict RNA secondary structures, perform zero-shot transfer to new genomic tasks, and integrate sequence-based predictions with experimental data for variant prioritization.

- **[Nucleotide Transformer](https://github.com/instadeepai/nucleotide-transformer)** `InstaDeep`

  > A collection of genomic language models pre-trained on 3,202 diverse genomes using self-supervised learning, providing embeddings for DNA sequences that capture evolutionary and functional constraints. Models range from 50M to 2.5B parameters with context lengths up to 1000bp. AI agents can use Nucleotide Transformer to generate contextualized sequence embeddings, predict regulatory elements and promoters, identify functional variants, perform few-shot learning on limited datasets, transfer knowledge across species, fine-tune for specific genomic prediction tasks, and extract features for downstream machine learning models.

- **[DNABERT](https://github.com/jerryji1993/DNABERT)** `Ji et al.`

  > A BERT-based pre-trained model for DNA sequences using k-mer tokenization (k=3,4,5,6), capturing sequence patterns and motifs through bidirectional transformers. Pre-trained on human reference genome for genomic understanding tasks. AI agents can execute DNABERT to predict promoter regions and transcription factor binding sites, identify splice sites and polyadenylation signals, classify regulatory elements, perform motif discovery through attention visualization, fine-tune on specific genomic annotation tasks, and generate sequence representations for variant effect prediction.

- **[Geneformer](https://huggingface.co/ctheodoris/Geneformer)** `Gladstone Institutes / Christina Theodoris`

  > A transformer-based foundation model pre-trained on 30M single-cell transcriptomes from diverse tissues and cell types, learning context-specific gene network dynamics. Uses rank-based tokenization and attention mechanisms to capture gene-gene relationships. AI agents can invoke Geneformer to perform in silico perturbation predictions, identify disease-associated cell states, predict cell fate transitions, extract gene embeddings capturing functional relationships, perform few-shot cell type annotation, predict transcription factor targets, and model gene regulatory networks from expression data.

- **[scFoundation](https://github.com/biomap-research/scFoundation)** `BioMap Research`

  > A foundation model for single-cell biology pre-trained on 50M+ cells across multiple species and tissues using masked cell modeling, providing universal cell representations for diverse downstream tasks including cell type annotation, drug response prediction, and perturbation modeling. AI agents can execute scFoundation to annotate cell types with zero-shot learning, predict cellular responses to genetic or chemical perturbations, generate cell embeddings for clustering and visualization, perform cross-species cell type mapping, identify disease-relevant cell states, and integrate multi-modal single-cell data.

- **[UCE: Universal Cell Embeddings](https://github.com/snap-stanford/UCE)** `Stanford SNAP Lab`

  > A foundational model providing universal representations for single cells by pre-training on 36M cells from human and mouse tissues, enabling robust cell type identification and biological discovery across datasets. Uses contrastive learning and masked cell prediction. AI agents can invoke UCE to generate high-quality cell embeddings for any scRNA-seq dataset, perform reference-free cell type annotation, identify novel cell states, integrate datasets across batches and technologies, predict cell-cell relationships, build cell atlases with consistent embeddings, and enable few-shot learning for rare cell types.

- **[DiffDock](https://github.com/gcorso/DiffDock)** `Corso et al. / MIT`

  > A diffusion-based model for molecular docking that predicts protein-ligand binding poses using geometric deep learning, achieving state-of-the-art accuracy while being 1000x faster than traditional docking methods. Generates multiple diverse binding poses with confidence estimates. AI agents can execute DiffDock to predict ligand binding poses for drug discovery, screen virtual compound libraries rapidly, generate diverse binding mode hypotheses, estimate binding confidence without computationally expensive scoring, integrate with molecular dynamics for pose refinement, and prioritize compounds for experimental validation.

- **[EquiBind](https://github.com/HannesStark/EquiBind)** `Stärk et al. / MIT`

  > A geometric deep learning framework for fast and accurate blind protein-ligand docking using equivariant graph neural networks, predicting binding poses directly without requiring pocket specification or docking scoring functions. Provides uncertainty quantification for predictions. AI agents can invoke EquiBind to perform rapid ligand docking without predefined binding sites, screen large compound libraries efficiently, predict binding poses for flexible ligands, generate initial poses for molecular dynamics simulations, integrate with downstream binding affinity prediction, and enable high-throughput virtual screening workflows.

- **[RFdiffusion](https://github.com/RosettaCommons/RFdiffusion)** `David Baker Lab`

  > A diffusion-based generative model for de novo protein design that creates protein backbones with desired shapes, functions, or binding properties using denoising diffusion probabilistic models trained on protein structures. Enables design of binders, enzymes, and scaffolds. AI agents can execute RFdiffusion to design proteins with specified geometries, generate binders for target proteins, create enzyme scaffolds for desired active sites, design symmetric protein assemblies, produce motif-scaffolding proteins, inpaint protein regions while preserving function, and integrate with ProteinMPNN for sequence design to create novel functional proteins.

### 可视化和探索

- **[IGV: Integrative Genomics Viewer](https://igv.org/)** `Broad Institute`

  > A high-performance genome browser for interactive visualization of diverse genomic data types including alignments (BAM/CRAM), variants (VCF), coverage tracks, gene annotations, and ChIP-seq peaks. Supports real-time navigation across reference genomes with synchronized multi-track views. AI agents can invoke IGV to visually inspect variant calls and alignment quality, validate structural variants and splice junctions, examine read depth and coverage patterns, visualize epigenetic modifications and regulatory elements, generate publication-ready screenshots of genomic regions, integrate multiple data tracks for comprehensive variant interpretation, and perform batch processing for automated snapshot generation.

- **[Loupe Browser](https://www.10xgenomics.com/support/software/loupe-browser)** `10X Genomics`

  > An interactive desktop application for exploring single-cell and spatial transcriptomics data from 10X Genomics platforms, providing intuitive visualization of clusters, gene expression, and spatial tissue architecture. Includes tools for differential expression, pathway enrichment, and cell type annotation. AI agents can guide users to explore Cell Ranger outputs in Loupe, interactively define cell populations and subclusters, visualize gene expression overlays on tissue images for Visium data, perform on-the-fly differential expression analysis, annotate cell types with custom markers, export high-resolution images for publications, and compare expression patterns across spatial regions or experimental conditions.

- **[cellxgene](https://cellxgene.cziscience.com/)** `Chan Zuckerberg Initiative`

  > A web-based interactive explorer for single-cell transcriptomics data that enables dynamic visualization, gene expression queries, and cell subset selection through an intuitive interface. Serves as both a data portal (CZ CELLxGENE Discover with 50M+ cells) and local visualization tool. AI agents can deploy cellxgene to provide interactive data exploration for collaborators, visualize AnnData objects with UMAP/t-SNE projections, dynamically color cells by gene expression or metadata, select and export cell subsets for re-analysis, integrate with computational notebooks, host datasets for publication sharing, and enable researchers to explore single-cell atlases without programming expertise.

- **[Napari](https://napari.org/)** `Napari Community`

  > A fast, multi-dimensional image viewer for Python designed for visualizing and analyzing large biological imaging datasets including microscopy, spatial transcriptomics imaging, and volumetric data. Features GPU-accelerated rendering and extensible plugin architecture. AI agents can invoke Napari to visualize spatial transcriptomics H&E images alongside gene expression, display multi-channel fluorescence microscopy with custom colormaps, perform manual annotation and segmentation of cells/nuclei, integrate deep learning models for automated image analysis, create 3D visualizations of volumetric imaging data, prototype image processing workflows interactively, and develop custom plugins for specialized imaging tasks.

### 工具总结表

| 工具                       | 副标题                                                     | 组织                        | 类别                              | 链接                                                          |
| -------------------------- | ------------------------------------------------------------ | ------------------------------------ | ------------------------------------- | ------------------------------------------------------------ |
| **FastQC**                 | 高通量测序数据质量控制工具     | Babraham Bioinformatics              | 核心 NGS 管道                     | https://www.bioinformatics.babraham.ac.uk/projects/fastqc/   |
| **Trimmomatic**            | 灵活的 Illumina NGS 数据读取修剪工具            | Usadel Lab                           | 核心 NGS 管道                     | http://www.usadellab.org/cms/?page=trimmomatic               |
| **BWA**                    | Burrows-Wheeler 比对器                                      | Heng Li Lab                          | 核心 NGS 管道                     | http://bio-bwa.sourceforge.net/                              |
| **STAR**                   | 拼接转录本到参考基因组的比对                 | Alexander Dobin                      | 核心 NGS 管道                     | https://github.com/alexdobin/STAR                            |
| **Minimap2**               | Versatile alignment tool for long-read sequencing            | Heng Li                              | 核心 NGS 管道                     | https://github.com/lh3/minimap2                              |
| **Samtools**               | Suite of utilities for manipulating SAM/BAM/CRAM alignments  | Genome Research Ltd                  | 核心 NGS 管道                     | http://www.htslib.org/                                       |
| **BEDTools**               | 工具set for genome arithmetic operations                     | Quinlan Lab                          | 核心 NGS 管道                     | https://bedtools.readthedocs.io/                             |
| **Picard**                 | 工具s for manipulating high-throughput sequencing data       | Broad Institute                      | 核心 NGS 管道                     | https://broadinstitute.github.io/picard/                     |
| **SPAdes**                 | St. Petersburg genome Assembler                              | Center for Algorithmic Biotechnology | 基因组组装和变异分析    | https://github.com/ablab/spades                              |
| **Flye**                   | Long-read de novo assembler                                  | Kolmogorov Lab                       | 基因组组装和变异分析    | https://github.com/fenderglass/Flye                          |
| **Canu**                   | Long-read assembly toolkit                                   | Koren & Walenz Labs                  | 基因组组装和变异分析    | https://github.com/marbl/canu                                |
| **QUAST**                  | QUality ASsessment Tool for genome assemblies                | Center for Algorithmic Biotechnology | 基因组组装和变异分析    | https://github.com/ablab/quast                               |
| **Bandage**                | Bioinformatics Application for Navigating De novo Assembly Graphs Easily | Ryan Wick                            | 基因组组装和变异分析    | https://github.com/rrwick/Bandage                            |
| **GATK**                   | Genome Analysis Toolkit                                      | Broad Institute                      | 基因组组装和变异分析    | https://gatk.broadinstitute.org/                             |
| **bcftools**               | 工具kit for VCF/BCF file manipulation and variant calling    | Genome Research Ltd                  | 基因组组装和变异分析    | http://samtools.github.io/bcftools/                          |
| **Manta**                  | Structural variant caller                                    | Illumina                             | 基因组组装和变异分析    | https://github.com/Illumina/manta                            |
| **FreeBayes**              | Bayesian genetic variant detector                            | Erik Garrison                        | 基因组组装和变异分析    | https://github.com/freebayes/freebayes                       |
| **Pindel**                 | Pattern-growth approach to detect breakpoints                | Wellcome Trust Sanger Institute      | 基因组组装和变异分析    | https://github.com/genome/pindel                             |
| **VEP**                    | Variant Effect Predictor                                     | EMBL-EBI / Ensembl                   | 基因组组装和变异分析    | https://www.ensembl.org/vep                                  |
| **SnpEff**                 | Variant annotation and functional effect prediction          | Pablo Cingolani                      | 基因组组装和变异分析    | https://pcingola.github.io/SnpEff/                           |
| **ANNOVAR**                | Versatile variant annotation tool                            | Kai Wang Lab                         | 基因组组装和变异分析    | https://annovar.openbioinformatics.org/                      |
| **DESeq2**                 | Differential gene expression analysis from count data        | Love, Anders, Huber                  | 转录组学和表达分析 | https://bioconductor.org/packages/DESeq2/                    |
| **edgeR**                  | Differential expression analysis using empirical Bayes       | Gordon Smyth Lab                     | 转录组学和表达分析 | https://bioconductor.org/packages/edgeR/                     |
| **StringTie**              | Transcript assembler and quantifier                          | Johns Hopkins University CCB         | 转录组学和表达分析 | https://ccb.jhu.edu/software/stringtie/                      |
| **Salmon**                 | Ultra-fast transcript quantification                         | Rob Patro Lab                        | 转录组学和表达分析 | https://combine-lab.github.io/salmon/                        |
| **HTSeq**                  | 框架 for processing high-throughput sequencing data     | Simon Anders Lab                     | 转录组学和表达分析 | https://htseq.readthedocs.io/                                |
| **Scanpy**                 | 工具kit for analyzing single-cell RNA-seq data               | Theis Lab                            | 转录组学和表达分析 | https://scanpy.readthedocs.io/                               |
| **Seurat**                 | 工具kit for single-cell RNA-seq analysis                     | Satija Lab                           | 转录组学和表达分析 | https://satijalab.org/seurat/                                |
| **Cell Ranger**            | Analysis pipeline for 10X Genomics data                      | 10X Genomics                         | 转录组学和表达分析 | https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/what-is-cell-ranger |
| **scVI**                   | Single-cell Variational Inference                            | Yosef Lab                            | 转录组学和表达分析 | https://scvi-tools.org/                                      |
| **scGPT**                  | Foundation model for single-cell biology                     | Cui Lab                              | 转录组学和表达分析 | https://scgpt.readthedocs.io/                                |
| **Squidpy**                | 工具kit for spatial molecular data analysis                  | Theis Lab                            | 转录组学和表达分析 | https://squidpy.readthedocs.io/                              |
| **Tangram**                | Deep learning for mapping single-cell to spatial             | Regev Lab                            | 转录组学和表达分析 | https://tangram-sc.readthedocs.io/                           |
| **STUtility**              | Analyzing and visualizing spatially resolved transcriptomics | Lundeberg Lab                        | 转录组学和表达分析 | https://ludvigla.github.io/STUtility_web_site/               |
| **SPATA2**                 | 框架 for spatial transcriptomics analysis               | Kuppe Lab                            | 转录组学和表达分析 | https://themilolab.github.io/SPATA2/                         |
| **Giotto**                 | 工具box for spatial and multiplexed imaging data             | Yuan Lab                             | 转录组学和表达分析 | https://giottosuite.readthedocs.io/                          |
| **MACS2**                  | 模型-based Analysis of ChIP-Seq                             | Tao Liu Lab                          | 表观基因组学和调控分析     | https://github.com/macs3-project/MACS                        |
| **HOMER**                  | Hypergeometric Optimization of Motif EnRichment              | Christopher Benner                   | 表观基因组学和调控分析     | http://homer.ucsd.edu/homer/                                 |
| **MEME Suite**             | 工具s for motif discovery and analysis                       | Timothy Bailey Lab                   | 表观基因组学和调控分析     | https://meme-suite.org/                                      |
| **Bismark**                | Aligner for bisulfite-treated sequencing data                | Babraham Bioinformatics              | 表观基因组学和调控分析     | https://www.bioinformatics.babraham.ac.uk/projects/bismark/  |
| **deepTools**              | 工具kit for exploring deep-sequencing data                   | Ramírez Lab                          | 表观基因组学和调控分析     | https://deeptools.readthedocs.io/                            |
| **ATACseqQC**              | Quality control and analysis for ATAC-seq                    | Jianhong Ou, Julie Zhu               | 表观基因组学和调控分析     | https://bioconductor.org/packages/ATACseqQC/                 |
| **ChromHMM**               | Chromatin state discovery from histone modifications         | Ernst & Kellis Lab                   | 表观基因组学和调控分析     | http://compbio.mit.edu/ChromHMM/                             |
| **MOFA+**                  | Multi-Omics Factor Analysis                                  | Ricard Argelaguet, Britta Velten     | 多组学整合               | https://biofam.github.io/MOFA2/                              |
| **Seurat V5**              | Latest Seurat with multi-modal integration                   | Satija Lab                           | 多组学整合               | https://satijalab.org/seurat/                                |
| **MultiVI**                | Deep model for joint RNA-seq and ATAC-seq                    | Gayoso, Steier et al.                | 多组学整合               | https://docs.scvi-tools.org/en/stable/user_guide/models/multivi.html |
| **totalVI**                | Probabilistic model for CITE-seq data                        | Gayoso, Steier et al.                | 多组学整合               | https://docs.scvi-tools.org/en/stable/user_guide/models/totalvi.html |
| **LIGER**                  | 链接ed Inference of Genomic Experimental Relationships       | Joshua Welch Lab                     | 多组学整合               | https://github.com/welch-lab/liger                           |
| **Scissor**                | Phenotype-associated single-cell subpopulation identification | Duan Chen Sun                        | 多组学整合               | https://github.com/sunduanchen/Scissor                       |
| **OpenMS**                 | 框架 for mass spectrometry data analysis                | OpenMS Team                          | 特定技术工具             | https://www.openms.de/                                       |
| **MaxQuant**               | Quantitative proteomics software platform                    | Jürgen Cox, Max Planck Institute     | 特定技术工具             | https://www.maxquant.org/                                    |
| **ProteoWizard**           | 工具s for mass spectrometry data conversion                  | Spielberg Family Center              | 特定技术工具             | http://proteowizard.sourceforge.net/                         |
| **QIIME2**                 | Quantitative Insights Into Microbial Ecology                 | Caporaso Lab                         | 特定技术工具             | https://qiime2.org/                                          |
| **MetaPhlAn**              | Metagenomic Phylogenetic Analysis                            | Huttenhower Lab                      | 特定技术工具             | https://github.com/biobakery/MetaPhlAn                       |
| **Kraken2**                | Ultrafast taxonomic classifier for metagenomics              | Derrick Wood & Steven Salzberg       | 特定技术工具             | https://github.com/DerrickWood/kraken2                       |
| **HUMAnN**                 | HMP Unified Metabolic Analysis Network                       | Huttenhower Lab                      | 特定技术工具             | https://huttenhower.sph.harvard.edu/humann/                  |
| **NanoPlot**               | Visualization tool for long-read sequencing QC               | Wouter De Coster                     | 特定技术工具             | https://github.com/wdecoster/NanoPlot                        |
| **Medaka**                 | Neural network-based consensus tool for Nanopore             | Oxford Nanopore Technologies         | 特定技术工具             | https://github.com/nanoporetech/medaka                       |
| **Racon**                  | Rapid consensus module for polishing assemblies              | Vaser et al.                         | 特定技术工具             | https://github.com/lbcb-sci/racon                            |
| **Clair3**                 | Deep learning-based variant caller for long reads            | Luo et al.                           | 特定技术工具             | https://github.com/HKU-BAL/Clair3                            |
| **miRDeep2**               | Probabilistic algorithm for discovering microRNAs            | Friedländer Lab                      | 特定技术工具             | https://github.com/rajewsky-lab/mirdeep2                     |
| **sRNAbench**              | Comprehensive tool for small RNA-seq analysis                | University of Granada                | 特定技术工具             | https://bioinfo2.ugr.es/srnatoolbox/srnabench/               |
| **rMATS**                  | replicate Multivariate Analysis of Transcript Splicing       | Manabu Shen Lab                      | 特定技术工具             | http://rnaseq-mats.sourceforge.net/                          |
| **SUPPA**                  | Super-fast Pipeline for Alternative Splicing                 | Eduardo Eyras Lab                    | 特定技术工具             | https://github.com/comprna/SUPPA                             |
| **LeafCutter**             | Annotation-free method for detecting intron excision         | David Knowles & Jonathan Pritchard   | 特定技术工具             | https://davidaknowles.github.io/leafcutter/                  |
| **AlphaFold**              | Deep learning system for protein structure prediction        | DeepMind / Google                    | AI/ML 基础模型               | https://alphafold.ebi.ac.uk/                                 |
| **ESMFold**                | Language model-based protein structure prediction            | Meta AI                              | AI/ML 基础模型               | https://esmatlas.com/                                        |
| **RoseTTAFold**            | Three-track neural network for structure prediction          | David Baker Lab                      | AI/ML 基础模型               | https://github.com/RosettaCommons/RoseTTAFold                |
| **xTrimo**                 | Multimodal foundation model for genomics                     | BioMap Research                      | AI/ML 基础模型               | https://github.com/biomap-research/xTrimo                    |
| **Nucleotide Transformer** | Genomic language models pre-trained on diverse genomes       | InstaDeep                            | AI/ML 基础模型               | https://github.com/instadeepai/nucleotide-transformer        |
| **DNABERT**                | BERT-based pre-trained model for DNA sequences               | Ji et al.                            | AI/ML 基础模型               | https://github.com/jerryji1993/DNABERT                       |
| **Geneformer**             | Transformer-based foundation model for single-cell           | Gladstone Institutes                 | AI/ML 基础模型               | https://huggingface.co/ctheodoris/Geneformer                 |
| **scFoundation**           | Foundation model for single-cell biology                     | BioMap Research                      | AI/ML 基础模型               | https://github.com/biomap-research/scFoundation              |
| **UCE**                    | Universal Cell Embeddings                                    | Stanford SNAP Lab                    | AI/ML 基础模型               | https://github.com/snap-stanford/UCE                         |
| **DiffDock**               | Diffusion-based model for molecular docking                  | Corso et al. / MIT                   | AI/ML 基础模型               | https://github.com/gcorso/DiffDock                           |
| **EquiBind**               | Geometric deep learning for protein-ligand docking           | Stärk et al. / MIT                   | AI/ML 基础模型               | https://github.com/HannesStark/EquiBind                      |
| **RFdiffusion**            | Diffusion-based generative model for protein design          | David Baker Lab                      | AI/ML 基础模型               | https://github.com/RosettaCommons/RFdiffusion                |
| **IGV**                    | Integrative Genomics Viewer                                  | Broad Institute                      | 可视化和探索           | https://igv.org/                                             |
| **Loupe Browser**          | Interactive explorer for 10X Genomics data                   | 10X Genomics                         | 可视化和探索           | https://www.10xgenomics.com/support/software/loupe-browser   |
| **cellxgene**              | Web-based interactive explorer for single-cell data          | Chan Zuckerberg Initiative           | 可视化和探索           | https://cellxgene.cziscience.com/                            |
| **Napari**                 | Multi-dimensional image viewer for biological imaging        | Napari Community                     | 可视化和探索           | https://napari.org/                                          |



---

## 维护与更新

本代码库旨在作为**活资源**，并将随着新的生物 AI 智能体系统、基准测试和评估实践的出现而不断更新。

---

## 引用

如果您发现此代码库有用，请引用相应的论文：
```
@article{qi2026artificial,
  title={Artificial Intelligence agents for biological research: a survey},
  author={Qi, Cong and Wang, Wenbo and Jiang, Siqi and Liu, Qin and Song, Xun and Fang, Hanzhang and Wei, Zhi},
  journal={Briefings in Bioinformatics},
  volume={27},
  number={1},
  pages={bbag075},
  year={2026},
  publisher={Oxford University Press}
}
```
