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
  > 本工作介绍了 PheNormGPT，这是一个基于大型语言模型的框架，用于从非结构化临床文本中提取表型发现并将其标准化为人类表型本体概念。通过使用微调的 GPT 模型和新颖的自适应少样本选择策略，PheNormGPT 在 BioCreative VIII 表型提取挑战中取得了最先进的性能。结果证明了 LLM 驱动方法在准确临床表型标准化方面的有效性。



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
  > 本研究通过整合转录组数据、功能富集分析和多种机器学习方法，探讨了自身免疫过程与颅内动脉瘤 (IA) 之间的遗传联系。研究确定了两个关键的自身免疫相关诊断基因 ADIPOQ 和 IL21R，并用它们构建了一个具有强大预测性能的神经网络模型 (AUC = 0.944)。结果强调免疫浸润和基因-miRNA-药物调控网络是 IA 发病机制的重要贡献者，提示了潜在的治疗靶点。



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

  > 本研究分析了早期泌乳期饮食中不同精料水平如何影响奶牛的肝脏转录组反应。结果揭示了胎次特异性的代谢和炎症反应，为缓解负能量平衡的营养策略提供了见解。



- **[Benchmarking Large Language Models for Predictive Modeling in Biomedical Research With a Focus on Reproductive Health](https://pmc.ncbi.nlm.nih.gov/articles/PMC12312170/)** (*2025*) `bioRxiv`

  > 作者使用 DREAM 挑战数据集对多个大型语言模型在生物医学预测建模中的自动代码生成进行了基准测试。该研究表明，表现最佳的 LLM 可以匹配或超越专家设计的模型，特别是在标准化组学分析中。



- **[Bridging the Early Science Gap with Artificial Intelligence: Evaluating Large Language Models as Tools for Early Childhood Science Education](https://dl.acm.org/doi/full/10.1145/3706599.3721261)** (*2025*) `CHI EA`

  > 本文评估了领先的大型语言模型生成适合学龄前儿童的科学解释的能力。通过专家教师评估，它突出了 LLM 在支持幼儿科学教育方面的前景和局限性。



- **[Leveraging Large Language Models for Decision Support in Personalized Oncology](https://jamanetwork.com/journals/jamanetworkopen/article-abstract/2812097)** (*2023*) `JAMA Network Open`

  > 该研究探讨了使用对话式大型语言模型来辅助精准肿瘤学中的临床决策。它讨论了 LLM 在支持复杂生物标志物解释和简化获取先前生物医学知识方面的潜力。



- **[Evaluating the Use of Generative Artificial Intelligence to Support Genetic Counseling for Rare Diseases](https://www.mdpi.com/2075-4418/15/6/672)** (*2025*) `Diagnostics`

  > 本工作评估了多个生成式 AI 模型在回答与遗传咨询相关的罕见病问题时的准确性和安全性。虽然整体表现强劲，但该研究强调了错误信息的风险以及专家监督的必要性。



- **[Leveraging Generative AI to Accelerate Biocuration of Medical Actions for Rare Disease](https://pmc.ncbi.nlm.nih.gov/articles/PMC11370550/)** (*2024*) `medRxiv`

  > 本文介绍了 AutoMAxO，这是一个基于 LLM 的半自动化工作流程，用于扩展罕见病医疗行动的生物管理。通过将 AI 驱动的提取与本体对齐和人工验证相结合，该方法显著加速了结构化知识管理。



- **[Importance of Prior Patient Interactions With the Healthcare System to Engaging With Pretest Cancer Genetic Services via Digital Health Tools](https://onlinelibrary.wiley.com/doi/abs/10.1111/1475-6773.14652)** (*2025*) `Health Services Research`

  > 这项随机试验研究了先前的医疗保健系统参与如何影响患者对癌症遗传服务数字工具的使用。研究结果表明，现有的患者-系统互动是参与基因检测工作流程的关键预测因素。



- **[Comparison of the Performance of Five Generative Artificial Intelligence Models on a Medical Molecular Biology Examination](https://www.cureus.com/articles/358057-comparison-of-the-performance-of-five-generative-artificial-intelligence-models-on-a-medical-molecular-biology-examination.pdf)** (*2025*) `Cureus`

  > 本研究比较了五个中国生成式 AI 模型在医学分子生物学考试中的表现。结果显示，几个模型的表现优于本科生，同时强调了在教育中需要批判性评估和特定领域 AI 系统的必要性。

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

  > 本文探讨了基于人格的提示作为捕捉 LLM 中人类推理多样性的机制。通过将心理人格模型与遗传算法相结合，该方法使 LLM 能够在直觉和深思熟虑的推理任务中近似人类反应分布。


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

本节整理了用于评估生物医学领域 AI 系统的基准测试，分为两类：生物医学推理和问答（通过问答格式进行知识和推理）以及复杂的现实世界生物医学任务（端到端的研究工作流，包括计划、工具使用和自主执行）。这是一份将不断更新的文档。

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

  > AutoGen 是一个用于构建智能体对话系统的框架，支持通过对话智能体开发 LLM 应用。它提供任务编排与智能体协同的基础，采用事件驱动架构和异步消息传递协议。框架支持按功能角色实例化智能体，并管理结构化消息传递，既支持任务前向推进，也支持在专用智能体之间的回溯纠错（如 Planner、Reasoner、Memory、RAG、Tool executors、Code、Critic、Reporter）。

- **[CodeAct: Executable Code Actions Elicit Better LLM Agents](https://github.com/xingyaoww/code-act) ** `UIUC & Apple`

  > CodeAct 是一个将 LLM 智能体动作统一到代码动作空间的框架。支持智能体动态执行 Python 代码，通过自我调试修订先前动作，并在多轮交互中根据观察输出新的动作。通过控制流与数据流支持复杂操作，借助丰富的软件包扩展动作空间，并提供自动化反馈机制以支持迭代式任务求解。

- **[LangChain: Platform for Reliable Agents](https://github.com/langchain-ai/langchain)** `LangChain`
  
  > LangChain 是用于构建智能体系统和 LLM 应用的综合框架。提供模块化组件以串联可互操作元素，支持与多样数据源和外部系统集成，并通过组件化架构实现快速原型。支持模型互操作、实时数据增强，并内置监控与评估能力，提供生产就绪特性以部署可靠的智能体应用。

- **[LangGraph: Build Resilient Language Agents as Graphs](https://github.com/langchain-ai/langgraph)**  `LangChain`

  > LangGraph 是用于构建可控、有状态多智能体应用的底层编排框架，适合复杂工作流。支持可定制的智能体架构，内置持久化检查点、循环以及人机协作（human-in-the-loop）交互。提供基于图的工作流管理以协调多个智能体，具备长期记忆能力和生产级部署工具。可与 LangChain 生态无缝集成，同时支持独立使用，满足对执行流精确控制的系统需求。

- **[CrewAI: Framework for Orchestrating Role-Playing, Autonomous AI Agents](https://github.com/joaomdmoura/crewai)** `CrewAI`
  
  > CrewAI 是一个用于构建协作式多智能体系统的框架，支持基于角色的任务委派。开发者可创建由专业智能体组成的团队共同完成复杂任务，内置流程编排（顺序、分层、共识）。提供任务分解与分配机制、智能体间通信协议，以及团队级记忆共享，用于协作式问题求解。

- **[BioChatter: A Platform for the Biomedical Application of Large Language Models](https://biochatter.org)** `Heidelberg University & EMBL-EBI`
  
  > BioChatter 是一个开源 Python 框架，旨在遵循开放科学原则，使用 LLM 构建定制化生物医学研究软件。提供统一的 API 抽象层，协调不同 LLM 部署工具和专有服务商，实现无代码改动的模型切换。与 BioCypher 知识图谱和向量数据库集成用于检索增强生成（RAG），通过稳健参数化便于外部 API 集成，并通过反思式工作流支持多智能体系统。具备持续基准评测基础设施以保障可复现性、可定制的系统提示用于领域对齐，以及覆盖从快速原型到完全封装、具备数据主权的生产系统的模块化架构。

### 智能体记忆系统
- **[LlamaIndex: Building LLM-powered Agents over Data](https://github.com/run-llama/llama_index)** `LlamaIndex`
  
  > LlamaIndex 是用于构建具备持久知识管理能力的上下文感知智能体系统的数据框架。提供数据连接器以摄取多源信息（API、PDF、数据库、文档），通过可定制索引与知识图谱结构化数据以实现高效检索，并提供高级查询接口让智能体访问相关上下文。支持通过 RAG 将外部或私有数据注入 LLM 推理，既提供快速原型的高层 API，也提供可定制记忆架构的底层组件，并可与智能体框架无缝集成构建知识支撑型应用。

- **[Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory](https://github.com/mem0ai/mem0)** `Mem0 AI`

  > Mem0 是用于构建具备可扩展、持久记忆能力的 AI 智能体框架。提供分层记忆设计，同时实现短期记忆（STM）用于任务级临时上下文与长期记忆（LTM）用于持久知识存储。支持用户画像存储与基于向量的事实存储，并具备语义检索能力，使智能体能够跨会话保持上下文并在不同问题间进行类比推理。

- **[Redis: The Real-Time Data Platform](https://github.com/redis/redis)** `Redis`

  > Redis 是内存数据结构存储，常用作数据库、缓存和消息代理。在智能体系统中，Redis 可作为智能体记忆的后端存储，提供实时状态跟踪能力。支持带先入先出（FIFO）淘汰策略的内存缓冲区，并可作为向量存储的近似最近邻搜索索引层，实现对已验证事实、流程与实验发现的快速语义检索。

- **[ChromaDB: Open-source search and retrieval database for AI applications](https://github.com/chroma-core/chroma)** `Chroma`
  
  > ChromaDB 是一个 AI 原生嵌入数据库，专为构建具有语义搜索功能的 LLM 应用程序而设计。为智能体记忆系统提供高效的嵌入存储和检索，支持元数据过滤和混合搜索，并提供内存和持久存储选项。使智能体能够维护基于向量的知识库以进行快速相似性搜索，与 LangChain 和 LlamaIndex 无缝集成，并包含多个模型的内置嵌入函数。
  
- **[Qdrant: Vector Search Engine for the Next Generation of AI Applications](https://github.com/qdrant/qdrant)** `Qdrant`
  
  > Qdrant 是一个高性能的向量相似度搜索引擎，专为智能体记忆和检索系统设计。具有高级过滤、基于有效载荷的查询和高效的近似最近邻搜索功能。支持分布式部署，为复杂查询提供基于 JSON 的过滤，并为生产智能体应用程序提供云端和自托管选项。

### LLM后端和智能体推理

- **[Transformers: State-of-the-Art Natural Language Processing](https://github.com/huggingface/transformers)** `Hugging Face`

  > Transformers 是一个提供数千个用于自然语言处理任务的预训练模型的库。它作为智能体推理能力的核心推理引擎，使系统能够利用大型语言模型进行任务分解、科学推理和决策。该库为各种基于 LLM 的智能体组件提供支持，包括查询重写、信息综合以及内存系统中的 LLM 驱动整合过程。

- **[vLLM: High-throughput and memory-efficient LLM inference engine](https://github.com/vllm-project/vllm)** `UC Berkeley`
  
  > vLLM 是一个快速且内存高效的大型语言模型推理引擎。通过 PagedAttention 优化智能体推理以实现高效的内存管理，连续批处理以实现高吞吐量，并优化 CUDA 内核。使智能体能够高效处理多个并发请求，支持各种量化方法以减少内存占用，并提供与 OpenAI 兼容的 API 以与智能体框架无缝集成。
  
- **[Ollama: Get Up and Running With Large Language Models](https://github.com/ollama/ollama)** `Ollama`
  
  > Ollama 是一个用于在个人机器上运行大型语言模型的本地运行时，无需依赖云服务。使智能体能够在本地执行 LLM 推理，支持包括 Llama、Mistral、Gemma 和 DeepSeek 在内的多个开源模型。提供统一的模型管理 API，支持通过 Modelfiles 进行模型自定义，并提供 CUDA 和 Vulkan 的 GPU 加速。允许智能体在访问强大的语言模型的同时维护数据隐私，包括支持多模态输入，并通过其 REST API 和 Python/JavaScript 库与智能体框架无缝集成。pSeek。提供统一的模型管理 API，支持通过 Modelfiles 进行模型自定义，并提供 CUDA 和 Vulkan 的 GPU 加速。允许智能体在访问强大语言模型的同时保持数据隐私，包括对多模态输入的支持，并通过其 REST API 和 Python/JavaScript 库与智能体框架无缝集成。

- **[OpenAI Python: Official Python client for the OpenAI API](https://github.com/openai/openai-python)** `OpenAI`

  > OpenAI Python 是用于访问 OpenAI REST API 的官方 Python 库，为智能体系统提供直接访问 GPT 模型和其他 OpenAI 服务的途径。具有类型安全的请求和响应处理、完全自动完成支持、同步和异步客户端实现以及列表操作的自动分页迭代器。使智能体能够利用 OpenAI 的语言模型进行推理、文本生成、视觉理解和工具调用功能。支持实时智能体交互的流式响应、全面的超时和重试配置，以及与各种智能体框架的集成，以构建生产就绪的 AI 应用程序。

- **[Anthropic Python: Official Python client for the Anthropic API](https://github.com/anthropics/anthropic-sdk-python)** `Anthropic`

  > Anthropic Python 是用于访问 Anthropic REST API 的官方 Python 库，为智能体系统提供对 Claude 模型和高级 AI 功能的直接访问。通过 Pydantic 模型提供类型安全的请求和响应处理、同步和异步客户端实现以及对流式响应的本机支持。使智能体能够利用 Claude 的语言模型进行推理、分析、工具使用（函数调用）和扩展思维能力。支持用于成本优化的提示缓存、用于多模态输入的视觉理解，并与智能体框架无缝集成。为超时、重试和自定义标头提供全面的配置选项，并内置对用于企业智能体应用程序的 Amazon Bedrock 部署的支持。

### 智能体服务和监控

- **[MLflow: Open-Source Platform for Productionizing AI](https://github.com/mlflow/mlflow)** `Databricks`

  > MLflow 是一个用于管理端到端机器学习生命周期的开源平台。对于智能体系统，MLflow 能够记录智能体会话和进行版本控制，确保在实验运行中的可重复性。它跟踪智能体执行轨迹、中间结果、工具调用和决策基本原理，为所有计算实验维护来源元数据。该平台能够审核从规划到执行和验证的整个工作流，并通过确定性种子初始化来实现可重复的智能体行为。

- **[Chainlit: Build Conversational AI in minutes](https://github.com/Chainlit/chainlit)** `Chainlit`
  
  > Chainlit 是一个用于快速构建智能体系统对话界面的框架。使开发人员能够创建基于聊天的 UI，内置支持流式响应、多步骤交互和智能体工作流可视化。具有自动对话历史管理、文件上传处理以及与主要框架（包括 LangChain、LlamaIndex 和 OpenAI）的集成。提供用于定义消息处理程序和工具执行步骤的装饰器，支持实时协作，并包括用于 PostgreSQL 和云存储后端持久存储的数据层功能。允许以最少的代码快速原型化智能体界面，同时保持生产就绪的可扩展性。

- **[Flask: Lightweight Web Framework](https://github.com/pallets/flask)** `Pallets`
  
  > Flask 是一个轻量级的 WSGI Web 框架，用于在 Python 中构建 Web 应用程序和 API。通常用于为智能体系统创建 HTTP 端点，提供灵活的路由、请求处理和响应格式化功能。具有极简的核心和广泛的扩展生态系统，用于身份验证、数据库集成和 API 开发。使开发人员能够为智能体交互构建自定义 Web 界面，将智能体服务部署为 REST API，并将智能体系统集成到更大的 Web 应用程序中。支持同步和异步操作，提供 Jinja2 模板渲染，并为服务智能体驱动的应用程序提供直接的部署选项。
-  **[FastAPI: 现代、快速的 API Web 框架](https://github.com/tiangolo/fastapi)** `Sebastián Ramírez`
  
  > FastAPI 是一个现代、高性能的 Web 框架，用于使用 Python 构建 API。广泛用于将智能体系统部署为生产服务，具有自动 API 文档、异步请求处理和通过 Pydantic 进行的类型验证。为实时智能体交互提供 WebSocket 支持，为管理智能体生命周期提供依赖项注入，并为智能体端点文档提供 OpenAPI 架构生成。使具有内置数据验证和序列化功能的智能体 API 得以快速开发。
  
- **[Gradio: Build Machine Learning Web Apps](https://github.com/gradio-app/gradio)** `Hugging Face`
  
  > Gradio 是一个 Python 库，用于快速为机器学习模型和智能体系统创建可自定义的 UI 组件。使开发者能够用最少的代码构建用于智能体演示的交互式界面，支持包括文本、图像和音频在内的各种输入类型，并提供实时反馈可视化。具有内置的共享功能、针对复杂工作流的组件组合，以及与 Hugging Face Spaces 的无缝集成，可用于公开部署智能体应用程序。

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

  > ClinVar 是一个免费可访问的数据库，存档基因组变异的临床解释及其与人类健康状况的关系。汇聚来自临床检测实验室、研究团队、专家小组和特定位点数据库的变异分类，为临床诊断和精准医学提供权威的变异-疾病关联。包含结构化提交记录（SCV 登录号）、聚合解释（RCV 登录号）、证据文档与审阅状态指示。支持通过 E-utilities API 编程访问，并按月发布 XML、VCF 与表格格式数据，便于系统化变异解读流程。

- **[MyGene2: Sharing Information to Learn About Genes and Rare Conditions](https://mygene2.org/)** `University of Washington`

  > MyGene2 是一个由患者驱动的登记与数据共享平台，连接受罕见遗传病影响的个体和家庭，以促进基因发现并改进变异解读。提供由患者/家庭直接报告的遗传变异、表型描述、临床病史与自然史数据，尤其覆盖文献不足的罕见与超罕见疾病。使智能体能够获取患者报告的基因型-表型关联、新的变异-疾病关联、临床结局数据与家庭经验，支持变异分类、基因-疾病关系验证以及罕见病自然史研究与不确定意义变异的临床解读。


- **[MPD: Mouse Phenome Database](https://www.jax.org/research-and-faculty/resources/mouse-phenome-database)** `The Jackson Laboratory`

  > MPD 是用于生物医学研究实验小鼠品系的综合资源，包含品系特征、表型数据、基因型信息与实验方案。为数百个近交、重组近交和突变小鼠品系提供标准化表型测量，覆盖心血管、代谢、行为、血液学等生理系统。使智能体能够访问比较表型数据、数量性状位点（QTL）定位结果、遗传变异信息与实验方案，支持转化研究、疾病建模以及模型生物的基因型-表型关联研究。

- **[gnomAD: Genome Aggregation Database](https://gnomad.broadinstitute.org/)** `Broad Institute`

  > gnomAD 是全球最大的公开人类遗传变异数据库，汇聚并协调来自不同人群的 80 多万人的外显子组与全基因组测序数据。提供人群等位基因频率、约束度量与变异注释，帮助智能体在临床解读流程中区分致病变异与良性群体变异。包含祖源特异的频率数据、功能缺失变异目录、结构变异注释及质控后的变异调用结果，可通过浏览器界面、API 与云端数据发布（AWS、Azure、Google Cloud）访问。

- **[UCSC Genome Browser: Integrated tool for visualizing and analyzing genome assemblies](https://genome.ucsc.edu/)** `UC Santa Cruz Genomics Institute`

  > UCSC Genome Browser 是一个综合平台，用于跨多物种与多版本基因组组装探索基因组注释、比较基因组学与实验数据。为智能体提供参考序列、基因预测、调控元件、保守性评分、变异数据以及来自 ENCODE、GTEx 等大型项目的海量实验轨道的一体化访问。支持通过 REST API 编程检索、MySQL 数据库访问和轨道数据下载，用于系统化基因组分析与跨物种比较研究。

- **[COSMIC: Catalogue of Somatic Mutations in Cancer](https://cancer.sanger.ac.uk/cosmic)** `Wellcome Sanger Institute`

  > COSMIC 是全球最全面的人类癌症体细胞突变数据库，收录跨多种癌症类型与基因的数百万肿瘤相关遗传改变。整合大型癌症基因组测序项目（TCGA、ICGC）数据与人工整理的文献突变，为智能体提供突变频率、组织分布、功能预测与耐药关联等信息。包含癌症基因普查注释、融合基因数据、拷贝数变异和结构重排，可通过网页、下载与 API 访问，用于癌症基因组学分析。

- **[Open Targets Genetics: Systematic drug target identification and prioritization](https://genetics.opentargets.org/)** `Open Targets`

  > Open Targets Genetics 是一个综合平台，整合 GWAS、功能基因组学与变异-基因映射，用于建立疾病-基因关系以发现治疗靶点。汇聚 GWAS Catalog、UK Biobank、FinnGen 等来源数据，并提供位点-基因评分、数量性状位点（QTL）数据与通路富集分析。使智能体能够基于遗传证据强度进行靶点优先级排序，探索变异的功能影响，并通过系统整合群体遗传与分子数据评估靶点可成药性。

- **[RegulomeDB: Annotation of regulatory variants in the human genome](http://www.regulomedb.org/)** `Stanford University`

  > RegulomeDB 是一个用于注释人类遗传变异调控潜力的数据库，基于 ENCODE、Roadmap Epigenomics 等功能基因组学项目的证据。依据转录因子结合、DNase 超敏、组蛋白修饰、染色质状态与表达数量性状位点（eQTL）关联对非编码变异进行评分。使智能体能够优先级排序调控变异、预测对基因表达的功能影响，并识别在特定细胞类型中影响转录调控的变异。

- **[GEO: Gene Expression Omnibus](https://www.ncbi.nlm.nih.gov/geo/)** `NCBI`

  > GEO 是一个公共仓库，存档来自芯片、RNA-seq、ChIP-seq 等平台的高通量基因表达与功能基因组学数据，覆盖数百万样本。提供整理后的数据集（GEO DataSets）、标准化样本元数据、平台注释与处理后的表达矩阵，支持智能体进行荟萃分析与比较转录组研究。支持 GEOquery API 编程访问、直接下载数据，并可与 NCBI 分析工具集成，用于系统探索不同实验条件、组织与疾病中的基因表达模式。

- **[SRA: Sequence Read Archive](https://www.ncbi.nlm.nih.gov/sra/)** `NCBI`

  > SRA 是最大的公共高通量测序数据仓库，存储来自新一代测序平台的原始读段及比对信息。作为 INSDC（与 EBI、DDBJ）的一部分，SRA 收录超过 25 Pb 的数据、1,480 万+ 运行记录，覆盖基因组学、转录组学、宏基因组学和表观基因组学等生命科学分支。智能体可通过 E-utilities API、SRA Toolkit（FASTQ、BAM 转换）以及云平台（AWS S3、Google Cloud BigQuery）访问数据，实现大规模序列检索、已发表数据集再分析及跨成千上万实验的荟萃分析，用于比较基因组学与变异发现。

- **[ENCODE: Encyclopedia of DNA Elements](https://www.encodeproject.org/)** `NHGRI`

  > ENCODE 通过对转录、转录因子结合、染色质结构、组蛋白修饰与 DNA 甲基化的系统实验刻画，绘制人类与小鼠基因组的功能元件图谱。第三阶段数据包含 5,992 个实验数据集，覆盖 503 种细胞/组织类型，定义了 926,535 个候选人类顺式调控元件与 339,815 个小鼠顺式调控元件，分别覆盖其基因组的 7.9% 与 3.4%。智能体可利用 ENCODE 数据进行调控元件注释、表观基因组状态分析、非编码区变异解读及基因调控机制研究。数据可通过 ENCODE Portal REST API 访问，并在 AWS Open Data Registry 发布，统一处理流程保障高质量 ChIP-seq、RNA-seq、ATAC-seq 与 Hi-C 数据集。

- **[NCBI RefSeq: Reference Sequence Database](https://www.ncbi.nlm.nih.gov/refseq/)** `NCBI`

  > RefSeq 提供覆盖 55,000+ 物种（原核、生物、真核与病毒）的经专家整理、非冗余参考序列（基因组、转录本与蛋白质）。其唯一的登录号格式（如 NM_、NP_）便于识别；记录整合多源信息并经过专家审校，代表当前共识序列，包含编码区、保守结构域、变异与标准化命名等完整功能注释。智能体将 RefSeq 作为序列比对、变异注释、基因识别与比较基因组学的金标准。可通过 Entrez 查询、BLAST、FTP 下载与 E-utilities 编程检索访问，并包含 MANE（匹配临床转录本）、RefSeqGene（临床参考标准）与 RefSeq Functional Elements 等专项项目。

- **[Ensembl: Genome Browser and Annotation System](http://www.ensembl.org/index.html)** `EMBL-EBI`

  > Ensembl 通过自动化注释管道和专家管理，为 50,000 多个基因组提供全面的基因组注释、比较基因组学和变异数据。该系统在交互式基因组浏览器中整合了基因预测、同源关系、调控特征、遗传变异（SNP、插入缺失、结构变异）和表型关联，通过主 Ensembl 站点支持脊椎动物，通过 Ensembl Genomes（植物、后生动物、细菌、真菌、原生生物）支持非脊椎动物。智能体利用 Ensembl 的 REST API 和 Perl API 以编程方式检索基因结构、直系同源映射、变异注释、调控构建数据和跨物种比对。包括用于变异后果预测的变异效应预测器 (VEP) 和用于跨多个物种和数据类型批量数据提取的 BioMart。


### 分子和结构数据库

- **[PDB: Protein Data Bank](https://www.rcsb.org/)** `RCSB`

  > PDB 是全球实验解析的蛋白质、核酸及复合体三维结构的存储库，结构来源于 X 射线晶体学、NMR 与冷冻电镜等技术。提供原子坐标、实验数据、结构质量指标与功能注释，覆盖数十万生物大分子结构，使智能体能够进行结构基础的药物设计、蛋白工程与分子功能预测。具备高级检索、结构比对工具，并支持通过 REST API 与 PDB、mmCIF 等标准格式文件下载进行编程访问。
- **[miRBase: The MicroRNA Database](https://www.mirbase.org/)** `University of Manchester`

  > miRBase 是已发表 microRNA 序列、命名、注释与预测靶基因的主要在线仓库，覆盖后生动物、植物与病毒基因组。提供整理后的 miRNA 基因序列、基因组位置、发夹前体结构、成熟 miRNA 序列、表达数据与标准化命名，涵盖数百物种的数千 miRNA 位点。通过网页、可下载平面文件与 MySQL 数据库访问，支持智能体识别 miRNA、分析转录后调控机制、预测 miRNA-靶基因相互作用并探索发育与疾病中的调控网络。
- **[UniProt: Universal Protein Resource](https://www.uniprot.org/)** `UniProt Consortium`

  > UniProt 是最全面且高质量的蛋白质序列与功能信息数据库，将文献与计算分析数据整合为统一的蛋白记录。Swiss-Prot 提供专家整理的蛋白功能、亚细胞定位、翻译后修饰、蛋白互作、疾病关联与结构特征注释，TrEMBL 提供计算注释条目以实现全蛋白组覆盖。通过网页服务、SPARQL 端点与批量下载，支持智能体获取标准化蛋白标识符、与 150+ 生物数据库的交叉引用、序列变异与 GO 术语注释。

- **[AlphaFold DB: AlphaFold Protein Structure Database](https://alphafold.ebi.ac.uk/)** `DeepMind & EMBL-EBI`

  > AlphaFold DB 提供由 DeepMind AlphaFold 系统生成的 AI 预测蛋白结构，覆盖生命全域 2 亿+ 蛋白，精度接近实验水平。为几乎完整的蛋白组（包含人类、模式生物与 UniProt 参考蛋白组）提供高置信结构模型，并给出每个残基置信度分数（pLDDT）和预测对齐误差（PAE）矩阵。通过可下载坐标文件、交互式 3D 可视化与编程 API，支持智能体获取缺乏实验数据的蛋白结构，显著扩展结构覆盖范围，用于结构生物学分析与计算药物发现。

- **[InterPro: Protein Sequence Analysis and Classification](https://www.ebi.ac.uk/interpro/)** `EMBL-EBI`

  > InterPro 将多个成员数据库（Pfam、PROSITE、SMART、PRINTS、ProDom）的蛋白签名整合为统一的蛋白家族、结构域与功能位点分类体系。通过基于序列的保守区、结构域、活性位点与结合位点预测提供全面功能注释，并具备层级组织与 GO 术语关联。通过 InterProScan 服务、网页界面与可下载签名库，支持智能体推断蛋白功能、识别进化关系、预测结构域架构并注释新序列，实现高通量蛋白分类。

- **[KEGG: Kyoto Encyclopedia of Genes and Genomes](https://www.genome.jp/kegg/)** `Kanehisa Laboratories`

  > KEGG 是一个综合数据库，通过人工整理的代谢通路、调控网络与疾病关联，整合跨上千物种的基因组、化学与系统功能信息。提供通路图、酶反应、化合物结构、药物-靶点关系、疾病基因与基因组注释，使智能体能够在分子与细胞层面分析生物系统。包含用于功能注释的 KEGG Orthology、用于生物实体的 BRITE 层级体系，以及用于理解基因功能、代谢能力与药物机制的网络分析方法，可通过 REST API 与平面文件下载访问。

- **[Reactome: Pathway Knowledgebase](https://reactome.org/)** `Reactome`

  > Reactome 是一个经过人工整理和同行评审的人类生物通路与过程数据库，提供具备实验依据的详细分子机制，并包含跨物种通路投影。通路按层级组织，覆盖代谢、信号转导、转录调控与疾病过程，并包含蛋白-蛋白相互作用、翻译后修饰与亚细胞定位信息。通过通路富集分析工具、通路图导出、REST API 与图数据库查询等方式支持智能体，并可与组学数据整合进行功能解读与系统生物学分析。

- **[JASPAR: Open-Access Database of Transcription Factor Binding Profiles](https://jaspar.genereg.net/)** `JASPAR Consortium`

  > JASPAR 是最大的开放获取转录因子（TF）结合谱数据库，汇集并整理来自已发表实验结合位点集合的、非冗余的真核 TF 结合数据。提供位置频率矩阵（PFM）、位置权重矩阵（PWM）、序列 logo 以及数百种转录因子的验证结合位点，覆盖人类、小鼠与其他模式生物。通过网页扫描工具、可下载的矩阵集合与编程 API，支持智能体预测调控序列中的 TF 结合位点、分析启动子区域、识别顺式调控元件并理解基因调控机制。

- **[BindingDB: Database of Measured Binding Affinities](https://www.bindingdb.org/)** `UC San Diego`

  > BindingDB 是一个公开的结合亲和力数据库，聚焦与药物发现和化学生物学相关的蛋白-小分子相互作用。提供来自同行评审文献与专利的数十万蛋白-配体复合物的定量结合数据，包括解离常数（Kd）、抑制常数（Ki）、IC50 与 EC50。通过可搜索的网页界面、可下载数据集与编程接口，支持智能体分析构效关系、构建 QSAR 预测模型、支持虚拟筛选，并为药物化学决策提供依据。

- **[DrugBank: Comprehensive Bioinformatics and Cheminformatics Resource](https://www.drugbank.com/)** `University of Alberta`

  > DrugBank 是一个综合数据库，将详细的药物信息与分子生物学和药理学数据整合，涵盖数千种药物条目，包括 FDA 批准药物、实验化合物与营养保健品。提供化学结构、作用机制、药代动力学（ADME）、药效学、药物相互作用、药物-靶点关系、代谢通路、不良反应、给药信息与临床试验数据。通过网页、REST API 与可下载数据集提供结构化药物知识（蛋白靶点、相关通路、疾病适应证、专利信息与文献引用），用于药物再利用、多靶点药理分析与治疗靶点发现。

### 专门的生物医学数据库

- **[CellxGene: Single-Cell Data Explorer and Census](https://cellxgene.cziscience.com/)** `Chan Zuckerberg Initiative`

  > CellxGene 是一个综合平台，用于探索、分析和共享来自多组织、多物种与多实验条件的单细胞 RNA-seq 数据集，覆盖数百万细胞。提供 CZ CELLxGENE Discover 集合，包含遵循社区标准、经过质控并注释细胞类型、组织、疾病和实验元数据的数据集。通过网页、可下载的 h5ad 文件与编程 API，支持智能体查询细胞类型特异性表达谱、跨研究比较分析、获取整理后的细胞注释并检索处理后的单细胞表达矩阵，以进行大规模单细胞基因组学分析。


- **[IUCN Red List: The IUCN Red List of Threatened Species](https://www.iucnredlist.org/)** `International Union for Conservation of Nature`

  > IUCN Red List 是全球最全面的物种保护现状评估名录，为超过 150,000 个物种提供灭绝风险评估、种群趋势与保护需求。基于标准化标准，提供物种分布、种群规模、栖息地需求、生态角色、威胁因素、保护行动以及红色名录等级（灭绝、极危、濒危、易危等）的详细信息。通过可搜索数据库、物种条目、空间数据下载与 API 访问，支持智能体分析生物多样性格局、保护优先级、灭绝风险因素及跨类群生态研究，适用于保护生物学与宏生态学应用。

- **[Human Microbiome Project: Data Analysis and Coordination Center](https://commonfund.nih.gov/hmp)** `National Institutes of Health`

  > Human Microbiome Project 提供全面的宏基因组、宏转录组、代谢组与临床数据集，刻画来自肠道、口腔、皮肤与泌尿生殖系统等人体部位的微生物群落。提供标准化采样流程、参考微生物基因组、多组学数据整合与纵向微生物组剖面，将群落组成与健康/疾病状态关联。通过可下载数据集、云端分析工作台与 API 访问，支持智能体分析宿主-微生物相互作用、研究微生物多样性模式、探究群落代谢功能，并探索微生物组失衡与疾病的关系。

- **[Addgene: Nonprofit Plasmid Repository](https://www.addgene.org/)** `Addgene`

  > Addgene 是一个非营利性质粒资源库，存档并分发用于基因组工程、基因表达与功能基因组学的研究级分子生物学工具。收录 147,000+ 质粒，涵盖 CRISPR/Cas 系统、慢病毒载体、荧光蛋白构建、光遗传工具、shRNA 干扰质粒与表达载体骨架，覆盖主要模式生物与实验系统。每个质粒条目包含注释序列图谱、克隆信息、抗性标记、质控数据与原始文献链接，确保对存储实验室的恰当署名。智能体可通过 BLAST 序列搜索找到相似构建体，按应用场景（基因编辑、蛋白标记、生物传感器）浏览整理集合，并获取带完整元数据的标准化质粒序列，用于克隆策略的计算设计与实验规划。
- **[10X Genomics Datasets](https://www.10xgenomics.com/datasets)** `10x Genomics`

  > 10X Genomics 提供来自 Chromium 单细胞与空间基因组学平台的公开参考数据集，包括单细胞 RNA-seq（3' 与 5' 基因表达）、免疫谱分析（V(D)J 测序）、ATAC-seq、多组学（RNA+ATAC）以及 Visium 空间转录组学，覆盖多样组织类型与物种。数据集包含 PBMC 样本、组织解离样本、肿瘤标本与发育研究，并附带 FASTQ 文件、处理后的基因-条形码矩阵、Cell Ranger 流水线分析输出与 Loupe Browser 可视化文件。智能体可将这些金标准基准数据用于方法验证、流程测试、教程开发与单细胞算法的对比分析。所有数据集均包含样本制备、测序参数与质量指标等完整元数据，支持可复现的计算工作流。

### 科学文献

- **[PubMed: Free Biomedical Literature Search Engine](https://pubmed.ncbi.nlm.nih.gov/)** `NCBI`

  > PubMed 是一个免费的综合性数据库，提供超过 3900 万条生物医学文献的引文与摘要，来源于 MEDLINE、生命科学期刊与在线图书，覆盖医学、生物学、生物化学等相关学科。具备 MeSH 受控词表用于精确检索、高级查询构建器、临床检索过滤器，并通过 PubMed Central 与出版社网站自动链接全文。支持智能体进行系统性文献检索、获取循证信息、访问出版元数据，并利用 E-utilities API 实现自动化文献综述、知识抽取与引文网络分析等生物医学研究应用。

- **[Google Scholar: Stand on the Shoulders of Giants](https://scholar.google.com/)** `Google`

  > Google Scholar 是一个综合性的学术搜索引擎，索引来自学术出版商、大学与学术组织的同行评审论文、学位论文、书籍、预印本、专利与会议论文，覆盖所有学科。提供引文指标、相关文献发现、作者主页与跨学科覆盖，范围超出生物医学文献，延伸至物理科学、社会科学、艺术与人文学科。支持智能体发现跨学科研究关联、跟踪引文网络、通过 h-index 与引文计数评估影响力，并通过广泛索引补充领域数据库以实现全面知识发现。

- **[bioRxiv: The Preprint Server for Biology](https://www.biorxiv.org/)** `Cold Spring Harbor Laboratory`

  > bioRxiv 是一个免费的生物学预印本平台，可在同行评审前快速发布研究成果，覆盖基因组学、神经科学、生物信息学、细胞生物学、发育生物学与系统生物学等 25+ 领域。提供完整未发表手稿的即时公开访问、用于引用的 DOI、版本更新跟踪，并自动链接后续正式发表的期刊文章。使智能体能够在正式发表前数月获取前沿研究方法、新兴计算工具、初步发现与创新实验思路；通过 RSS、API 与批量下载能力跟踪快速演进的研究领域、识别趋势方法并保持对生物科学最新进展的关注。

- **[Google Search: Search the World's Information](https://www.google.com/)** `Google`

  > Google Search 是一个综合性的网络搜索引擎，可实时访问互联网上数十亿网页、新闻、图片、视频与多样内容。提供高级搜索运算符、时间过滤、站点限定检索与自然语言查询处理，使智能体能够发现传统文献数据库之外的突发研究新闻、会议公告、实验室动态与新兴科学讨论。通过 Custom Search JSON API 提供可编程搜索，并可结合网页抓取能力进行系统化信息收集、实时趋势监测，以及发现发布前出现在机构网站、科研博客或研究组织公告中的初步研究成果。

- **[Zenodo: Open Science Repository](https://zenodo.org/)** `CERN & OpenAIRE`

  > Zenodo 是 CERN 运营的通用开放科研存储库，覆盖所有学科，存储数据集、出版物、软件、报告、海报、图像、视频与代码等多种研究成果。可无格式限制上传任意大小的数据（默认每个数据集 50GB，可申请更高配额），在 CERN 数据中心长期保存，并自动分配 DOI 便于引用，支持版本管理、GitHub 集成与灵活访问控制（开放、限期公开、受限、关闭）。智能体可用 Zenodo 获取论文补充数据、研究软件包与可重复性数据，并通过 OAI-PMH API 编程检索元数据。对访问领域社区（如生物医学数据集、计算生物学工作流）与通过保存精确代码和中间数据来确保可复现性尤其有价值。

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
  > 用于高通量测序数据的质量控制工具，生成包含按碱基质量分数、序列长度分布、接头污染和过度代表序列等在内的综合 QC 报告。提供命令行工具或 GUI 应用，并输出可视化 HTML 报告。AI 智能体可使用 FastQC 在比对前自动评估数据质量、识别需要修剪的样本，并基于质量指标确定最佳预处理参数。

- **[Trimmomatic](http://www.usadellab.org/cms/?page=trimmomatic)** `Usadel Lab`
  > 灵活的 Illumina NGS 读段修剪工具，执行接头去除、基于质量的修剪与低质量读段过滤。支持双端与单端数据，可配置滑动窗口修剪、最小长度过滤与质量阈值。AI 智能体可基于 FastQC 报告清洗原始测序数据，自动确定最佳修剪参数，并为比对流程准备高质量读段。

- **[BWA: Burrows-Wheeler Aligner](http://bio-bwa.sourceforge.net/)** `Heng Li Lab`
  > 快速且内存高效的比对器，使用 Burrows-Wheeler 变换算法将短 DNA 序列（70bp-1Mbp）比对到大型参考基因组。包含三种算法：BWA-backtrack（<100bp 读段）、BWA-SW（更长读段）与 BWA-MEM（最常用，适用于 70bp-1Mbp，擅长分裂比对）。AI 智能体可使用 BWA-MEM 进行全基因组比对，根据读长自动选择算法，并生成排序后的 BAM 文件供变异检测流程使用。

- **[STAR: Spliced Transcripts Alignment to a Reference](https://github.com/alexdobin/STAR)** `Alexander Dobin`
  > 超高速 RNA-seq 比对器，旨在高精度检测剪接位点，速度可达每小时超过 1 亿条读段。采用后缀数组映射并支持 2-pass 比对模式以提升剪接检测。输出包含比对后的 BAM、剪接位点表与基因层面读数。AI 智能体可执行 STAR 进行转录组比对，自动配置基因组索引，检测新剪接变体，并生成差异表达分析所需的计数矩阵。

- **[Minimap2](https://github.com/lh3/minimap2)** `Heng Li`
  > 面向长读长测序数据（PacBio、Oxford Nanopore）和组装-组装对比优化的通用比对工具，支持从千碱基到兆碱基的读长。具备快速 all-vs-all 比对、长读长 RNA-seq 的剪接比对以及对噪声长读段的准确映射。AI 智能体可使用 Minimap2 进行长读长基因组/转录组比对、结构变异检测流程，以及草图基因组组装的快速对比。

- **[Samtools](http://www.htslib.org/)** `Genome Research Ltd`
  > 一套用于操作 SAM/BAM/CRAM 格式比对的综合实用工具，提供核心功能，包括排序、索引、合并、过滤和格式转换。支持并行处理、CRAM 压缩（与 BAM 相比可减少高达 60% 的大小）和特定区域的数据提取。AI 智能体可以调用 Samtools 进行标准 BAM 文件操作（排序、索引、合并、查看），计算比对统计信息，提取特定基因组区域，并为下游变异调用或可视化准备文件。

- **[BEDTools](https://bedtools.readthedocs.io/)** `Quinlan Lab`
  > 一个强大的工具集，用于对基因组区间（BED、GFF、VCF 格式）进行基因组算术运算，支持交集、合并、补集和覆盖率计算等任务。支持对数百万个区间进行高效操作。AI 智能体可以使用 BEDTools 识别数据集之间的重叠特征，计算覆盖率统计信息，合并相邻区间，查找最近的特征，并执行对 ChIP-seq、ATAC-seq 和变异分析工作流程至关重要的复杂基因组区间查询。

- **[Picard](https://broadinstitute.github.io/picard/)** `Broad Institute`
  > 一套基于 Java 的命令行工具，用于处理高通量测序数据与格式（SAM/BAM/CRAM、VCF 等）以及各类质量指标。关键功能包括标记 PCR 重复、收集比对指标、修复 mate-pair 信息与格式转换。AI 智能体可调用 Picard 在变异检测前标记重复读段、校验 BAM 文件完整性、收集全面的比对与插入片段指标，并确保满足基于 GATK 流水线的质量标准。


### 基因组组装和变异分析

- **[SPAdes: St. Petersburg genome Assembler](https://github.com/ablab/spades)** `Center for Algorithmic Biotechnology, St. Petersburg State University`
  
  > 面向小基因组（细菌、真菌）的多用途 de novo 组装器，使用 Illumina 短读数据，并提供单细胞、宏基因组、质粒与 RNA-seq 组装模式。采用多 k 值 de Bruijn 图并内置纠错以处理不均匀覆盖与测序错误。AI 智能体可使用 SPAdes 进行细菌基因组组装，按数据类型自动选择组装模式，迭代优化 k-mer，并与下游注释流程集成。
  
- **[Flye](https://github.com/fenderglass/Flye)** `Kolmogorov Lab`
  > 面向 PacBio 与 Oxford Nanopore 数据的长读长 de novo 组装器，采用基于重复图的算法，可组装从细菌到哺乳动物尺度的基因组。能够处理原始长读段的高错误率，并生成连续性优秀的高质量组装。AI 智能体可使用 Flye 进行长读长组装流程，根据覆盖度与读长自动配置参数，进行宏基因组组装，并生成用于变异检测的高质量参考基因组。

- **[Canu](https://github.com/marbl/canu)** `Koren & Walenz Labs`
  > 面向高噪声单分子测序（PacBio、Oxford Nanopore）的长读长组装工具包，具备自适应 k-mer 加权、强纠错与适用于大型真核基因组的优化算法。包含读段校正、修剪与组装模块，并支持分布式计算。AI 智能体可使用 Canu 执行复杂基因组组装项目，管理 HPC 集群上的高资源计算，针对重复区域调节敏感度参数，并产出染色体尺度的组装结果。

- **[QUAST: QUality ASsessment Tool](https://github.com/ablab/quast)** `Center for Algorithmic Biotechnology`
  > 综合性的组装质量评估工具，在有参考基因组时计算 N50、错组装、基因组覆盖比例、基因完整性等指标。生成包含可视化的交互式 HTML 报告，并支持宏基因组组装评估。AI 智能体可调用 QUAST 自动评估组装质量、比较多种组装策略、识别潜在错组装，并基于量化指标选择最佳组装参数。

- **[Bandage: Bioinformatics Application for Navigating De novo Assembly Graphs Easily](https://github.com/rrwick/Bandage)** `Ryan Wick`
  > 用于可视化 de Bruijn 图与组装图的 GUI 工具（适用于 SPAdes、Velvet 等输出），支持交互式查看图结构、重复区域与组装路径。可在图内进行 BLAST 搜索，并支持基于覆盖度或序列相似度的自定义着色。AI 智能体可利用 Bandage 的命令行接口生成组装图像、识别组装问题区域、可视化结构变异，并指导有针对性的组装优化。

- **[GATK: Genome Analysis Toolkit](https://gatk.broadinstitute.org/)** `Broad Institute`
  > 高通量测序变异发现的金标准工具包，提供胚系与体细胞变异调用的最佳实践流程（包括 SNP、indel 与 CNV）。功能包括碱基质量分数校准、变异质量分数校准与跨队列联合分型。AI 智能体可执行 GATK 流程进行临床级变异检测，自动应用 VQSR 过滤，进行多样本联合调用，并与下游注释工具集成以支持变异解读。

- **[bcftools](http://samtools.github.io/bcftools/)** `Genome Research Ltd`
  > 用于 VCF/BCF 文件处理与变异调用的综合工具集，提供过滤、合并、注释与从比对数据中调用变异等功能。针对大规模群体基因组学进行了高度优化，支持多样本调用。AI 智能体可使用 bcftools 在 BAM 上快速变异调用，执行复杂 VCF 过滤，合并多样本 VCF，计算群体统计量，并提取特定变异或样本用于下游分析。

- **[Manta](https://github.com/Illumina/manta)** `Illumina`
  > 结构变异（SV）检测器，针对双端测序数据识别缺失、插入、倒位与易位，具备高灵敏度与高特异性。结合配对读段与分裂读段证据并进行局部组装精细化，以准确解析断点。AI 智能体可调用 Manta 检测大规模基因组重排，将 SV 与 SNP/indel 数据整合以进行全面变异分析，识别癌相关融合基因，并在临床测序中优先排序致病性结构变异。

- **[FreeBayes](https://github.com/freebayes/freebayes)** `Erik Garrison`
  
  > 贝叶斯遗传变异检测器，用于在人群中发现 SNP、indel 与复杂变异，采用基于单倍型的变异调用，无需读段重比对。支持二倍体与多倍体基因组，并可灵活设置倍性。AI 智能体可使用 FreeBayes 进行群体规模变异调用，检测复杂的多核苷酸多态性，在肿瘤样本中进行体细胞突变检测，并从靶向测序面板生成高质量变异结果。
  
- **[Pindel](https://github.com/genome/pindel)** `Wellcome Trust Sanger Institute`
  
  > 使用配对短读段的模式生长方法检测大缺失、中等大小插入、倒位与串联重复的断点。擅长发现标准变异调用器常漏检的中等尺度 indel（1bp-10kb）。AI 智能体可使用 Pindel 补充 GATK/bcftools 的调用结果，提升 indel 检出率，在临床外显子组中识别致病性缺失/插入变异，并刻画癌症基因组的复杂结构重排。
  
- **[VEP: Variant Effect Predictor](https://www.ensembl.org/vep)** `EMBL-EBI / Ensembl`
  
  > 最全面的变异注释工具之一，用于预测基因组变异对基因、转录本与蛋白的功能影响，整合 30+ 预测算法（SIFT、PolyPhen、CADD）与临床数据库（ClinVar、gnomAD）。提供网页界面、命令行与 REST API，并支持自定义注释。AI 智能体可调用 VEP 对 VCF 进行转录本后果注释、获取群体频率、预测致损性评分、识别临床相关变异，并生成结构化报告用于变异解读。
  
- **[SnpEff](https://pcingola.github.io/SnpEff/)** `Pablo Cingolani`
  
  > 快速变异注释与功能效应预测工具，按影响程度（HIGH、MODERATE、LOW、MODIFIER）对变异分类，并提供基因注释、氨基酸改变与密码子简并信息。支持 38,000+ 基因组的预构建数据库。AI 智能体可使用 SnpEff 进行快速批量注释，优先排序高影响变异，生成功能类别分布统计，并与 Galaxy 流程集成实现自动化变异分析。
  
- **[ANNOVAR](https://annovar.openbioinformatics.org/)** `Kai Wang Lab`
  
  > 通用的变异注释工具，整合来自 RefSeq、UCSC、dbSNP、1000 Genomes 及自定义数据集等数百数据库的基因级、区域级与过滤型注释。支持灵活的自定义数据库集成与表格化输出格式。AI 智能体可使用 ANNOVAR 结合多源数据库进行变异注释，基于群体频率与预测致病性过滤变异，生成临床审核所需的制表报告，并使用疾病特异数据库定制注释流程。
### 转录组学和表达分析

- **[DESeq2](https://bioconductor.org/packages/DESeq2/)** `Michael Love, Simon Anders, Wolfgang Huber`

  > 最广泛使用的 R/Bioconductor 包，用于从计数数据进行差异表达分析，采用负二项广义线性模型、稳健方差估计与经验贝叶斯收缩。支持包含多因子的复杂实验设计，并支持用于模型比较的似然比检验。AI 智能体可使用 DESeq2 识别条件间差异表达基因、自动检测离群值、在考虑文库大小与组成的情况下进行归一化，生成发表级 MA 图与火山图，并导出带调整后 p 值的结果用于下游通路分析。

- **[edgeR](https://bioconductor.org/packages/edgeR/)** `Gordon Smyth Lab`

  > 强大的 R/Bioconductor 差异表达分析包，采用经验贝叶斯方法与广义线性模型，特别适用于小样本实验。包含准似然 F 检验与稳健方差建模以支持复杂实验设计。AI 智能体可使用 edgeR 在有限重复下进行差异表达分析，构建包含交互项的多因子设计，使用 camera/roast 进行基因集检验，并与 limma-voom 集成用于 RNA-seq 归一化与精度加权。

- **[StringTie](https://ccb.jhu.edu/software/stringtie/)** `Johns Hopkins University Center for Computational Biology`

  > 快速高效的转录本组装器，可从 RNA-seq 比对结果重建全长转录本、定量表达并识别新异构体与可变剪接事件。采用网络流算法，并支持参考引导组装以提升准确性。AI 智能体可调用 StringTie 进行 de novo 或参考引导组装，同时定量基因与转录本表达，检测新剪接位点，合并多样本组装，并生成与 DESeq2/edgeR 兼容的计数矩阵。

- **[Salmon](https://combine-lab.github.io/salmon/)** `Rob Patro Lab`

  > 超高速转录本定量工具，无需比对即可从 RNA-seq 读段估计丰度，采用双阶段并行推断与轻量映射，相比传统方法提升 10-100 倍速度。输出精确的 TPM 与估计计数并提供不确定性量化。AI 智能体可执行 Salmon 进行快速转录本定量，绕过耗时比对步骤，自动检测并校正序列特异性偏差，生成用于不确定性估计的 bootstrap 样本，并在分钟级生成用于差异表达分析的计数矩阵。

- **[HTSeq](https://htseq.readthedocs.io/)** `Simon Anders Lab`

  > 用于处理高通量测序数据的 Python 框架，最常用方式是通过 htseq-count 从比对后的 BAM 文件生成基因层面读数，并提供灵活的特征分配规则。支持双端数据与多种重叠处理模式。AI 智能体可使用 HTSeq 统计与基因组特征重叠的读段，根据实验需求选择计数模式（union、intersection-strict、intersection-nonempty），高效处理大型 BAM，并生成下游差异表达分析所需的计数表。

- **[Scanpy](https://scanpy.readthedocs.io/)** `Theis Lab`

  > 用于单细胞 RNA-seq 分析的综合 Python 工具包，提供可扩展的预处理、聚类、轨迹推断与可视化方法，支持百万级细胞数据集。与 AnnData 格式集成，并包含 PAGA 拓扑推断。AI 智能体可执行 Scanpy 流程进行单细胞数据归一化与过滤、识别高变基因、降维（PCA、UMAP、t-SNE）、使用 Leiden/Louvain 聚类、推断发育轨迹、识别标记基因并生成发表级图形。

- **[Seurat](https://satijalab.org/seurat/)** `Satija Lab`

  > 最流行的单细胞 RNA-seq 分析 R 工具包，提供从 QC、归一化、整合、聚类到差异表达的完整流程，并拥有 10 万+ 引用。第 5 版引入可扩展的磁盘级分析与更强的多模态整合能力。AI 智能体可调用 Seurat 处理 10X Genomics 数据，通过 anchors 或 harmony 整合多数据集，进行 SCTransform 归一化，使用参考注释识别细胞类型，使用 Visium 分析空间转录组，并生成可定制 UMAP/t-SNE 的交互式可视化。

- **[Cell Ranger](https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/what-is-cell-ranger)** `10X Genomics`

  > 10X Genomics 单细胞与空间转录组数据的官方分析流水线，针对 10X 化学体系进行了优化，完成拆分、条形码处理、比对、UMI 计数与细胞识别。输出包括特征-条形码矩阵与质量指标。AI 智能体可执行 Cell Ranger 处理 10X 实验的原始 BCL 文件，自动识别细胞条形码与 UMI，将读段比对到参考基因组，生成过滤后的基因-条形码矩阵，聚合多样本，并生成基于 Web 的 QC 汇总报告以进行快速质量评估。

- **[scVI: Single-cell Variational Inference](https://scvi-tools.org/)** `Yosef Lab`

  > 基于变分自编码器的单细胞组学概率建模深度学习框架，支持批次效应校正、缺失值填补、降维与多模态数据（RNA、ATAC、蛋白）的整合。包含用于注释迁移的 scVI、scANVI，以及用于多模态分析的 totalVI。AI 智能体可利用 scVI 在保留生物变异的同时去除批次效应，填补 dropout，跨技术与物种整合数据，进行概率型细胞类型注释，并生成具有生物学意义的低维嵌入用于下游分析。

- **[scGPT](https://scgpt.readthedocs.io/)** `Cui Lab`

  > 单细胞生物学基础模型，采用 Transformer 架构在 3300 万细胞上预训练，可实现零样本细胞类型注释、基因网络推断、扰动预测与多批次整合。学习跨多样细胞类型与组织的通用基因表示。AI 智能体可调用 scGPT 进行新数据集迁移学习，预测扰动下的基因表达变化，在缺乏参考数据时注释稀有细胞类型，推断基因调控关系，并利用预训练生物知识进行跨物种或跨组织分析。

- **[Squidpy](https://squidpy.readthedocs.io/)** `Theis Lab`

  > 用于空间分子数据分析的 Python 工具包，扩展了 Scanpy，包含空间统计、组织结构分析、配体-受体相互作用推断与图像特征提取方法。支持 Visium、Slide-seq 等多种空间技术及基于成像的方法。AI 智能体可使用 Squidpy 计算空间邻接图、识别空间变异基因、进行空间自相关分析、用深度学习从 H&E 图像提取形态学特征，通过配体-受体数据库推断细胞间通信，并结合组织上下文可视化空间模式。

- **[Tangram](https://tangram-sc.readthedocs.io/)** `Regev Lab`

  > 将单细胞或细胞类型特征映射到组织空间位置的深度学习方法，实现空间反卷积与跨技术数据整合。通过神经网络优化对齐基因表达谱，同时保持空间一致性。AI 智能体可执行 Tangram 将 scRNA-seq 数据映射到空间转录组切片，推断空间位置的细胞类型组成，将单细胞图谱注释迁移到空间数据，预测空间技术未捕获细胞类型的位置，并整合多模态空间数据集。

- **[STUtility](https://ludvigla.github.io/STUtility_web_site/)** `Lundeberg Lab`

  > 用于分析与可视化空间分辨转录组数据（尤其是 Visium）的 R 包，提供组织检测、图像对齐、空间特征识别与 Seurat 集成等工具。支持在组织切片上叠加基因表达的交互式可视化。AI 智能体可调用 STUtility 将组织图像与 spot 坐标对齐，自动检测组织区域，使用空间自相关识别空间变异基因，进行区域差异表达分析，将空间数据与 scRNA-seq 参考整合，并生成具有解剖学上下文的发表级空间图。

- **[SPATA2](https://themilolab.github.io/SPATA2/)** `Kuppe Lab`

  > 用于空间转录组综合分析的 R 框架，强调轨迹推断、表面建模与空间模式的交互式可视化。提供面向组织结构的高级空间统计与降维方法。AI 智能体可使用 SPATA2 推断跨组织区域的空间轨迹，将基因表达建模为连续表面，识别空间梯度与过渡区域，在解剖约束下进行空间聚类，并创建组织上下文中的交互式 3D 基因表达景观。

- **[Giotto](https://giottosuite.readthedocs.io/)** `Yuan Lab`

  > 覆盖 R 与 Python 的空间转录组与多重成像数据分析工具箱，提供空间统计、细胞邻近分析、配体-受体相互作用建模与空间富集分析方法。支持包括 Visium、Slide-seq、MERFISH、seqFISH 在内的 10+ 空间数据类型。AI 智能体可执行 Giotto 创建空间表达图谱，进行空间共表达网络分析，使用隐马尔可夫随机场识别空间域，计算细胞类型相互作用的空间富集分数，推断细胞间通信模式，并整合多分辨率空间数据集。

### 表观基因组学和调控分析

- **[MACS2: Model-based Analysis of ChIP-Seq](https://github.com/macs3-project/MACS)** `Tao Liu Lab`

  > 最常用的 ChIP-seq 与 ATAC-seq 峰调用工具，使用动态泊松分布建模局部偏差，以高灵敏度和特异性识别富集区域。支持组蛋白修饰的宽峰调用与转录因子的窄峰调用。AI 智能体可调用 MACS2 从处理组与对照组 BAM 文件进行峰调用，自动估计片段长度与背景，检测组蛋白修饰的广泛域，生成用于可视化的 bedGraph 与 bigWig 文件，计算倍数富集与 FDR，并输出峰顶（summit）文件用于基序分析。

- **[HOMER: Hypergeometric Optimization of Motif EnRichment](http://homer.ucsd.edu/homer/)** `Christopher Benner`

  > 用于基序发现、ChIP-seq 分析与基因组注释的综合套件，使用优化评分算法识别调控区域中富集的 DNA 基序。包含峰注释、差异结合分析与组蛋白修饰分析工具。AI 智能体可执行 HOMER 在峰区发现 de novo 基序，将峰注释到最近基因和基因组特征，在全基因组定位已知基序，进行条件间差异峰分析，创建用于可视化的 tag 目录，并生成包含基序 logo 与富集统计的 HTML 报告。

- **[MEME Suite](https://meme-suite.org/)** `Timothy Bailey Lab`

  > 基序发现与分析工具集合，包括用于 de novo 基序发现的 MEME、用于扫描已知基序的 FIMO，以及用于基序比较的 TOMTOM。支持含间隙基序与位置特异评分矩阵的高级算法。AI 智能体可使用 MEME 在 DNA/蛋白序列中发现无间隙或有间隙基序，使用 FIMO 扫描基因组中的基序出现位置，通过 TOMTOM 与数据库比较发现的基序，分析基序间距与方向，进行基序富集分析，并生成带统计显著性指标的发表级序列 logo。

- **[Bismark](https://www.bioinformatics.babraham.ac.uk/projects/bismark/)** `Babraham Bioinformatics`

  > 面向亚硫酸氢盐处理测序数据的专用比对器，可完成读段比对与 DNA 甲基化信息提取，支持方向性与非方向性文库，并支持双端读段。可在不同上下文（CpG、CHG、CHH）下进行比对与甲基化调用。AI 智能体可调用 Bismark 将亚硫酸氢盐转换读段比对到参考基因组，提取单碱基分辨率的甲基化调用，生成带覆盖统计的甲基化报告，对 WGBS 数据去重，生成用于基因组浏览器可视化的 bedGraph 文件，并量化不同基因组上下文的全局甲基化模式。

- **[deepTools](https://deeptools.readthedocs.io/)** `Ramírez Lab`

  > 用于深度测序数据探索与可视化的综合工具集，提供 BAM 文件处理、归一化、热图生成与质量控制，覆盖 ChIP-seq、ATAC-seq 与 RNA-seq 实验。包含 multiBamSummary、plotHeatmap、computeMatrix 等组件，可生成发表级图形。AI 智能体可使用 deepTools 生成样本间相关性图、在基因组特征（TSS、基因体、峰）周围绘制信号热图、计算不同归一化方法（RPKM、CPM、RPGC）的覆盖轨道、评估片段长度分布、进行 GC 偏差校正，并用可定制配色可视化全基因组信号模式。

- **[ATACseqQC](https://bioconductor.org/packages/ATACseqQC/)** `Jianhong Ou, Julie Zhu`

  > 面向 ATAC-seq 数据质量控制与分析的 R/Bioconductor 包，评估片段长度分布、转录起始位点富集、核小体定位与文库复杂度，并提供诊断图用于排查实验问题。AI 智能体可执行 ATACseqQC 通过检查片段长度周期性（核小体梯度）评估质量，计算 TSS 富集分数，展示插入片段长度分布，评估启动子/增强子富集，检测线粒体污染，识别需要重测的低质量文库，并生成包含标准化指标的综合 QC 报告。

- **[ChromHMM](http://compbio.mit.edu/ChromHMM/)** `Ernst & Kellis Lab`

  > 基于隐马尔可夫模型的染色质状态发现与表征方法，利用组蛋白修饰 ChIP-seq 数据学习并注释全基因组的组合染色质状态（启动子、增强子、绝缘子、异染色质等）。输出可直接用于浏览器的轨道以及发射/转移参数。AI 智能体可调用 ChromHMM 从多种组蛋白标记学习状态模型，自动将基因组分割为功能状态，比较不同细胞类型或条件下的染色质景观，识别分化过程中的状态转换，根据染色质特征注释增强子/启动子，并生成带生物学解释的预测调控元件轨道。

### 多组学整合

- **[MOFA+: Multi-Omics Factor Analysis](https://biofam.github.io/MOFA2/)** `Ricard Argelaguet, Britta Velten`

  > 基于组因子分析的多组学无监督整合统计框架，识别跨转录组、表观基因组、蛋白组等分子层的协同变化所对应的潜在因子。支持缺失数据并可进行多组比较。AI 智能体可执行 MOFA+ 整合多模态单细胞数据，识别组学层之间共享与特异的变异来源，进行方差分解量化各因子贡献，基于潜在因子对样本聚类，跨不完整数据集填补缺失值，并可视化驱动生物过程的协同分子变化。

- **[Seurat V5](https://satijalab.org/seurat/)** `Satija Lab`

  > Seurat 的最新版本，提供可扩展的多模态整合能力，支持通过 bridge integration 与 sketch-based 分析处理百万级细胞数据，并可同时分析 RNA、ATAC、蛋白与空间数据。引入磁盘级数据存储与更精简的整合流程。AI 智能体可调用 Seurat V5 使用 bridge integration anchors 跨技术整合数据集，在超大数据集（>1M 细胞）上进行 sketch 分析，使用加权最近邻（WNN）图分析 CITE-seq 数据，将查询数据集映射到参考图谱，整合空间与单细胞数据，并利用 BPCells 进行内存高效处理。

- **[MultiVI](https://docs.scvi-tools.org/en/stable/user_guide/models/multivi.html)** `Gayoso, Steier et al.`

  > scvi-tools 中用于单细胞 RNA-seq 与 ATAC-seq 联合分析的深度生成模型，学习统一的潜在表示以同时捕获基因表达与染色质可及性，并考虑技术噪声与批次效应。采用摊还推断以提升可扩展性。AI 智能体可使用 MultiVI 整合配对或不配对的 scRNA-seq 与 scATAC-seq 数据集，推断同时包含两种模态的细胞嵌入，填补缺失模态（从 ATAC 预测基因表达或反之），在保留生物变异的同时去除批次效应，联合进行可及性与表达差异分析，并跨模态迁移细胞类型注释。

- **[totalVI](https://docs.scvi-tools.org/en/stable/user_guide/models/totalvi.html)** `Gayoso, Steier et al.`

  > 用于 CITE-seq（RNA+表面蛋白）联合分析的概率模型，基于变分自编码器建模两种模态的技术特性，包括蛋白背景与 RNA dropout。可实现去噪的蛋白定量与整合聚类。AI 智能体可执行 totalVI 联合分析 CITE-seq 的基因表达与蛋白丰度，去除蛋白背景噪声与环境 RNA 污染，生成去噪蛋白表达矩阵，使用两种模态进行整合聚类，同时对基因与蛋白进行差异分析，并在缺少 ADT 数据的情况下填补蛋白测量值。

- **[LIGER: Linked Inference of Genomic Experimental Relationships](https://github.com/welch-lab/liger)** `Joshua Welch Lab`

  > 基于整合型非负矩阵分解（iNMF）的框架，用于在多模态单细胞数据集中识别共享与数据集特异特征，特别适合整合 scRNA-seq、scATAC-seq、空间转录组与 DNA 甲基化数据。在去除批次效应的同时保留生物变异。AI 智能体可调用 LIGER 使用 iNMF 整合多种单细胞模态，识别共享的元基因程序与数据集特异因子，对不同技术或物种的数据集进行对齐，进行多数据集轨迹推断，整合空间与非空间数据，量化基因载荷在各因子中的贡献，并使用联合 UMAP 嵌入可视化整合结果。

- **[Scissor](https://github.com/sunduanchen/Scissor)** `Duan Chen Sun`

  > 通过正则化回归将 bulk 组织表型（生存、药物反应、临床结局）与单细胞表达谱相关联，从而识别与表型关联的单细胞亚群的方法。连接 bulk 组学与单细胞数据以识别疾病相关细胞群。AI 智能体可执行 Scissor 识别与患者生存相关的细胞亚群，将单细胞状态与 bulk 肿瘤表型关联，从治疗反应数据中发现耐受治疗的细胞群，关联细胞状态与连续临床变量，基于表型关联为治疗靶向优先排序细胞类型，并将 TCGA bulk 数据与单细胞图谱整合以获得临床洞见。

### 特定技术工具

- **[OpenMS](https://www.openms.de/)** `OpenMS Team`

  > 面向质谱数据分析的综合开源框架，提供峰识别、特征检测、肽段鉴定、蛋白定量与代谢组学工作流工具。支持多种 MS 平台与格式（mzML、mzXML），并通过 TOPP 工具进行命令行处理。AI 智能体可执行 OpenMS 流水线处理原始 MS/MS 数据，进行无标记定量，识别翻译后修饰，基于 SRM/MRM 数据开展靶向蛋白组学分析，与数据库搜索引擎（Mascot、X!Tandem）集成，并生成标准化输出用于下游统计分析。

- **[MaxQuant](https://www.maxquant.org/)** `Jürgen Cox, Max Planck Institute`

  > 常用的定量蛋白组学平台，基于 Andromeda 搜索引擎分析大规模 MS 数据，支持无标记定量（LFQ）、同位素标签（TMT/iTRAQ）与 match-between-runs 以提升肽段鉴定。包含 Perseus 用于统计分析。AI 智能体可调用 MaxQuant 处理 Thermo、Bruker 与 Sciex 原始文件，在 FDR 控制下进行肽段鉴定，使用 LFQ 或 TMT 进行跨样本蛋白定量，识别蛋白组与同工型，进行 SILAC 定量，并将结果导出至 Perseus 进行差异分析与通路富集。

- **[ProteoWizard](http://proteowizard.sourceforge.net/)** `Spielberg Family Center for Applied Proteomics`

  > 质谱数据转换与分析的开源工具套件，包含 msConvert 用于将厂商专有格式转换为开放标准（mzML、mzXML），以及用于数据过滤、峰提取与质控的工具。支持 30+ 仪器厂商。AI 智能体可使用 ProteoWizard 将 RAW、WIFF、.d 等专有格式转换为开放标准，在转换过程中应用谱图过滤与质心化，提取特定扫描范围或 MS 层级，批量转换大型数据集，为 OpenMS/MaxQuant 的下游分析准备数据，并确保跨蛋白组学平台的数据互操作性。

- **[QIIME2: Quantitative Insights Into Microbial Ecology](https://qiime2.org/)** `Caporaso Lab`

  > 综合性的微生物组分析平台，用于处理扩增子测序数据（16S/18S/ITS），采用插件化架构，提供质控、DADA2/Deblur 去噪、分类学注释、多样性分析与可视化。支持带有产物溯源跟踪的可复现工作流。AI 智能体可执行 QIIME2 流水线将扩增子序列去噪为 ASV，使用训练好的分类器（SILVA、Greengenes2）进行物种注释，计算 α/β 多样性指标，使用 ANCOM-BC 进行差异丰度分析，生成交互式可视化，进行组分数据分析，并整合元数据用于微生物组-表型关联的统计检验。

- **[MetaPhlAn: Metagenomic Phylogenetic Analysis](https://github.com/biobakery/MetaPhlAn)** `Huttenhower Lab`

  > 通过类群特异标记基因从宏基因组 shotgun 测序数据中剖析微生物群落组成的计算工具，无需组装即可提供物种层级丰度。最新 mpa_vJan21 数据库包含来自 100,000+ 基因组的 100 万+ 标记基因。AI 智能体可调用 MetaPhlAn 快速获得 WGS 宏基因组的分类组成，定量细菌、古菌、病毒与真核微生物的相对丰度，检测菌株层级变异，合并多样本谱系用于比较分析，与 HUMAnN 集成进行功能剖析，并生成用于统计分析的丰度表。

- **[Kraken2](https://github.com/DerrickWood/kraken2)** `Derrick Wood & Steven Salzberg`

  > 使用与参考数据库的精确 k-mer 匹配对宏基因组序列进行分类的超高速分类器，在保持高准确性的同时比以往方法快 100 倍以上。支持基于 RefSeq/GenBank 构建自定义数据库。AI 智能体可执行 Kraken2 在分钟内分类数百万读段，为特定环境或病原体构建定制数据库，检测测序样本污染，在临床样本中识别病原体，结合 Bracken 量化分类丰度，并从宏基因组数据中过滤宿主来源读段。

- **[HUMAnN: HMP Unified Metabolic Analysis Network](https://huttenhower.sph.harvard.edu/humann/)** `Huttenhower Lab`

  > 用于宏基因组测序微生物群落功能剖析的流程，基于 UniRef 与 MetaCyc 数据库定量基因家族、通路与代谢潜力，并与 MetaPhlAn 集成实现物种特异的功能分析。AI 智能体可调用 HUMAnN 分析代谢通路与基因家族丰度，按物种分层功能贡献，识别条件间差异通路，映射至 KEGG/MetaCyc/GO 数据库，按测序深度与基因长度进行归一化，并生成用于多组学整合的通路丰度表。

- **[NanoPlot](https://github.com/wdecoster/NanoPlot)** `Wouter De Coster`

  > 用于 Oxford Nanopore 与 PacBio 长读长测序数据质控的可视化工具，可生成读长分布、质量分数与产量统计等综合图表。支持 FASTQ、BAM 与测序汇总文件。AI 智能体可执行 NanoPlot 评估长读长测序运行质量，展示读长 N50 与分布直方图，监测测序过程中质量变化，识别失效孔/通道，比较多次运行或条形码，并生成发表级 QC 报告以评估建库与测序性能。

- **[Medaka](https://github.com/nanoporetech/medaka)** `Oxford Nanopore Technologies`

  > 基于神经网络的共识抛光工具，用于纠正 Oxford Nanopore 读段组装中的系统性错误，提高碱基级准确度。使用针对特定 basecaller 版本与 flowcell 类型训练的循环神经网络。AI 智能体可在 Flye/Canu 之后调用 Medaka 抛光草图组装，将细菌基因组共识准确度提升至 >99.9%，从长读段比对中进行变异检测，按 basecaller 版本（Guppy/Dorado）选择模型，进行迭代抛光，并为下游注释或比较基因组学准备组装结果。

- **[Racon](https://github.com/lbcb-sci/racon)** `Vaser et al.`

  > 使用长读段进行基因组组装抛光的快速共识模块，采用部分序列排列（POA）图纠正噪声长读段导致的草图组装错误。速度快但精度略低，可与 Medaka 互补。AI 智能体可执行 Racon 进行初步快速抛光，进行多轮迭代提升准确度，与 minimap2 结合进行基于比对的抛光，高效处理大型真核基因组，并与 Medaka 组合形成混合抛光策略，为下游变异检测或结构分析准备组装结果。

- **[Clair3](https://github.com/HKU-BAL/Clair3)** `Luo et al.`

  > 面向长读长测序（ONT、PacBio HiFi）的小变异检测深度学习工具，结合 pileup 与全比对网络以实现 SNP 与 indel 的高精度与高召回。支持胚系与体细胞变异调用，并可根据测序平台选择模型。AI 智能体可调用 Clair3 从长读段 BAM 文件中检测 SNP/indel，自动选择平台特异模型（ONT R9/R10、PacBio HiFi），进行三联体变异检测（含父母基因型），在肿瘤样本中调用体细胞突变，生成带置信度评分的高质量 VCF，并与短读段数据结合形成混合变异检测策略。

- **[miRDeep2](https://github.com/rajewsky-lab/mirdeep2)** `Friedländer Lab`

  > 基于概率模型的算法，通过分析读段深度模式与 Dicer 处理的二级结构一致性，从小 RNA 测序数据中发现新 microRNA。可在样本间定量已知与新 miRNA 的表达。AI 智能体可执行 miRDeep2 从小 RNA-seq 数据识别新 miRNA，定量 miRBase 中已知 miRNA 的表达，预测前体结构与成熟序列，基于 Dicer 处理特征对候选进行打分，使用概率模型过滤假阳性，并生成高置信度新 miRNA 列表以供实验验证。

- **[sRNAbench](https://bioinfo2.ugr.es/srnatoolbox/srnabench/)** `University of Granada`

  > 面向小 RNA-seq 分析的综合在线与独立工具，提供读段处理、与多数据库（miRBase、piRNABank、tRNAs）比对注释、差异表达分析与 isomiR 检测。支持多物种与自定义参考库。AI 智能体可调用 sRNAbench 处理与比对小 RNA 读段，注释不同 RNA 生物类型（miRNA、piRNA、tRNA 片段、snoRNA），识别 isomiR 与 RNA 修饰，进行条件间差异表达分析，预测新 miRNA，并生成跨 RNA 类别的表达谱综合报告。

- **[rMATS: replicate Multivariate Analysis of Transcript Splicing](http://rnaseq-mats.sourceforge.net/)** `Manabu Shen Lab`

  > 用于从 RNA-seq 数据中检测差异可变剪接的计算工具，识别并量化五类主要剪接事件（SE、MXE、A5SS、A3SS、RI），并在生物重复间进行显著性检验。支持成对与非成对样本比较。AI 智能体可执行 rMATS 从 STAR 比对的 BAM 中检测可变剪接事件，量化每种事件的包含水平（PSI），进行条件间差异剪接统计检验，按覆盖度与 FDR 阈值过滤事件，通过 sashimi 图可视化剪接模式，并识别与疾病或发育转变相关的剪接变化。

- **[SUPPA: Super-fast Pipeline for Alternative Splicing](https://github.com/comprna/SUPPA)** `Eduardo Eyras Lab`

  > 从转录本定量（Salmon、Kallisto）进行可变剪接分析的轻量级工具，无需比对文件即可计算 PSI 并检测条件间差异剪接。支持局部事件与转录本层级分析。AI 智能体可调用 SUPPA 基于 GTF 注释生成剪接事件库，从转录本 TPM 估计计算 PSI，在数百样本上进行快速差异剪接分析，按剪接特征聚类样本，识别剪接异常值，并同时分析局部事件与全局转录本使用变化。

- **[LeafCutter](https://davidaknowles.github.io/leafcutter/)** `David Knowles & Jonathan Pritchard`

  > 一种无注释的 RNA-seq 内含子切除事件检测与定量方法，通过聚类共享剪接位点的内含子发现新的复杂剪接模式，并使用线性混合模型进行差异剪接分析。AI 智能体可执行 LeafCutter 在无需 GTF 注释的情况下从剪接连接读段中发现内含子簇，量化样本间的内含子切除比例，检测条件间差异内含子使用，识别隐匿剪接事件与新外显子，进行剪接变异的 QTL 映射（sQTL），并通过 leafviz 浏览器可视化复杂剪接模式。

### AI/ML基础模型

- **[AlphaFold](https://alphafold.ebi.ac.uk/)** `DeepMind / Google`

  > 革命性的蛋白结构预测深度学习系统，利用 Transformer 架构与多序列比对中的进化信息，实现接近实验水平的准确度。AlphaFold2 数据库包含 2 亿+ 预测结构，覆盖大多数已知蛋白。AI 智能体可调用 AlphaFold 从氨基酸序列预测 3D 结构，访问数据库中的预计算结构，使用 pLDDT 评分评估置信度，识别本征无序区域，使用 AlphaFold-Multimer 建模蛋白复合体，并将预测结构集成到药物发现或蛋白工程流程中。

- **[ESMFold](https://esmatlas.com/)** `Meta AI`

  > 基于语言模型的蛋白结构预测系统，训练于 2.5 亿+ 蛋白序列且无需 MSA，使预测速度比 AlphaFold 快约 60 倍且保持具有竞争力的准确度。使用 ESM-2 蛋白语言模型嵌入进行结构生成。AI 智能体可执行 ESMFold 快速预测缺乏同源的孤儿蛋白结构、生成宏基因组序列结构、高效批处理数千蛋白、访问含 6 亿+ 预测结构的 ESM Metagenomic Atlas、预测设计或突变序列结构，并与需要快速迭代的蛋白设计流程集成。

- **[RoseTTAFold](https://github.com/RosettaCommons/RoseTTAFold)** `David Baker Lab`

  > 结合 1D 序列、2D 距离图与 3D 坐标表示的三轨神经网络蛋白结构预测模型，采用注意力机制进行融合。包含 RoseTTAFold All-Atom，可预测包含小分子与修饰残基的结构。AI 智能体可调用 RoseTTAFold 在 MSA 深度有限时预测结构，建模蛋白-配体复合体，预测含翻译后修饰的结构，进行功能位点预测，与 Rosetta 套件集成进行结构精修，并处理含非标准氨基酸或辅因子的蛋白。

- **[xTrimo](https://github.com/biomap-research/xTrimo)** `BioMap Research`

  > 预训练于基因组序列、RNA 二级结构与功能注释的多模态基础模型，支持变异效应预测、调控元件识别、RNA 结构预测与基因表达预测等任务。采用 10 亿+ 参数的 Transformer 架构。AI 智能体可调用 xTrimo 预测遗传变异的致病性，识别非编码区调控元件，从序列预测基因表达变化，预测 RNA 二级结构，对新基因组任务进行零样本迁移，并将序列预测与实验数据结合进行变异优先排序。

- **[Nucleotide Transformer](https://github.com/instadeepai/nucleotide-transformer)** `InstaDeep`

  > 由自监督学习在 3,202 个多样基因组上预训练的基因组语言模型集合，为 DNA 序列提供包含进化与功能约束的嵌入表示。模型规模从 50M 到 2.5B 参数，最长上下文可达 1000 bp。AI 智能体可使用 Nucleotide Transformer 生成上下文化序列嵌入，预测调控元件与启动子，识别功能性变异，在小样本数据上进行小样本学习，跨物种迁移知识，针对特定基因组预测任务微调，并为下游机器学习模型提取特征。

- **[DNABERT](https://github.com/jerryji1993/DNABERT)** `Ji et al.`

  > 基于 BERT 的 DNA 序列预训练模型，采用 k-mer 分词（k=3/4/5/6），通过双向 Transformer 捕捉序列模式与基序。预训练于人类参考基因组，用于基因组理解任务。AI 智能体可执行 DNABERT 预测启动子与转录因子结合位点，识别剪接位点与多腺苷酸化信号，分类调控元件，通过注意力可视化进行基序发现，对特定注释任务微调，并生成用于变异效应预测的序列表示。

- **[Geneformer](https://huggingface.co/ctheodoris/Geneformer)** `Gladstone Institutes / Christina Theodoris`

  > 基于 Transformer 的基础模型，预训练于来自多组织与多细胞类型的 3000 万单细胞转录组，学习上下文特异的基因网络动态。采用基于排名的分词与注意力机制捕捉基因-基因关系。AI 智能体可调用 Geneformer 进行 in silico 扰动预测，识别疾病相关细胞状态，预测细胞命运转换，提取体现功能关系的基因嵌入，进行小样本细胞类型注释，预测转录因子靶点，并从表达数据构建基因调控网络。

- **[scFoundation](https://github.com/biomap-research/scFoundation)** `BioMap Research`

  > 预训练于多物种多组织 5000 万+ 细胞的单细胞生物学基础模型，采用 masked cell modeling，提供通用细胞表示，支持细胞类型注释、药物反应预测与扰动建模等多种下游任务。AI 智能体可执行 scFoundation 进行零样本细胞类型注释，预测遗传或化学扰动下的细胞反应，生成用于聚类与可视化的细胞嵌入，进行跨物种细胞类型映射，识别疾病相关细胞状态，并整合多模态单细胞数据。

- **[UCE: Universal Cell Embeddings](https://github.com/snap-stanford/UCE)** `Stanford SNAP Lab`

  > 通过在人类与小鼠组织的 3600 万细胞上预训练，为单细胞提供通用表示的基础模型，可在不同数据集间实现稳健的细胞类型识别与生物学发现。采用对比学习与 masked cell prediction。AI 智能体可调用 UCE 生成高质量细胞嵌入，进行无参考细胞类型注释，识别新细胞状态，跨批次与技术整合数据集，预测细胞-细胞关系，构建具有一致嵌入的细胞图谱，并支持稀有细胞类型的小样本学习。

- **[DiffDock](https://github.com/gcorso/DiffDock)** `Corso et al. / MIT`

  > 基于扩散模型的分子对接方法，利用几何深度学习预测蛋白-配体结合构象，达到最先进精度同时比传统对接快约 1000 倍。可生成多样化结合构象并给出置信度估计。AI 智能体可执行 DiffDock 进行药物发现中的配体构象预测，快速筛选虚拟化合物库，生成多种结合模式假设，在无需昂贵打分的情况下估计结合置信度，与分子动力学结合进行构象精修，并为实验验证优先排序化合物。

- **[EquiBind](https://github.com/HannesStark/EquiBind)** `Stärk et al. / MIT`

  > 基于几何深度学习的快速准确“盲对接”框架，使用等变图神经网络直接预测结合构象，无需事先指定口袋或对接打分函数，并提供预测不确定性量化。AI 智能体可调用 EquiBind 在无预定义结合位点的情况下进行快速配体对接，高效筛选大型化合物库，为柔性配体预测结合构象，生成分子动力学初始构象，与下游亲和力预测集成，并支持高通量虚拟筛选流程。

- **[RFdiffusion](https://github.com/RosettaCommons/RFdiffusion)** `David Baker Lab`

  > 用于从头蛋白设计的扩散式生成模型，基于蛋白结构训练的去噪扩散概率模型生成具有指定形状、功能或结合性质的蛋白骨架，可用于设计结合蛋白、酶与支架。AI 智能体可执行 RFdiffusion 设计特定几何的蛋白，为目标蛋白生成结合体，构建期望活性位点的酶支架，设计对称蛋白装配体，生成基序支架蛋白，在保留功能的同时对蛋白区域进行修补（inpainting），并与 ProteinMPNN 集成进行序列设计以产生新功能蛋白。

### 可视化和探索

- **[IGV: Integrative Genomics Viewer](https://igv.org/)** `Broad Institute`

  > 高性能基因组浏览器，用于交互式可视化多种基因组数据类型，包括比对结果（BAM/CRAM）、变异（VCF）、覆盖度轨道、基因注释与 ChIP-seq 峰。支持跨参考基因组的实时导航与多轨同步视图。AI 智能体可调用 IGV 目视检查变异调用与比对质量，验证结构变异与剪接位点，查看读深与覆盖模式，可视化表观修饰与调控元件，生成发表级基因组区域截图，整合多轨数据进行全面变异解读，并进行批处理自动生成快照。

- **[Loupe Browser](https://www.10xgenomics.com/support/software/loupe-browser)** `10X Genomics`

  > 用于探索 10X Genomics 平台单细胞与空间转录组数据的交互式桌面应用，提供对聚类、基因表达与组织空间结构的直观可视化。内置差异表达、通路富集与细胞类型注释工具。AI 智能体可引导用户在 Loupe 中探索 Cell Ranger 输出，交互式定义细胞群与子群，针对 Visium 数据在组织图像上叠加基因表达，实时进行差异表达分析，使用自定义标记注释细胞类型，导出出版级高清图像，并比较不同空间区域或实验条件下的表达模式。

- **[cellxgene](https://cellxgene.cziscience.com/)** `Chan Zuckerberg Initiative`

  > 基于网页的单细胞转录组交互式浏览器，提供动态可视化、基因表达查询与细胞子集选择的直观界面。既是数据门户（CZ CELLxGENE Discover，50M+ 细胞），也是本地可视化工具。AI 智能体可部署 cellxgene 为协作者提供交互式数据探索，使用 UMAP/t-SNE 可视化 AnnData 对象，按基因表达或元数据动态着色，选择并导出细胞子集用于再分析，与计算笔记本集成，托管数据集用于发表共享，并让研究者无需编程即可探索单细胞图谱。

- **[Napari](https://napari.org/)** `Napari Community`

  > Python 端快速的多维图像查看器，面向显微成像、空间转录组成像与体积数据等大型生物影像的可视化与分析。具备 GPU 加速渲染与可扩展插件架构。AI 智能体可调用 Napari 在基因表达旁可视化空间转录组 H&E 图像，用自定义色图展示多通道荧光显微图像，进行细胞/细胞核的手动标注与分割，集成深度学习模型进行自动图像分析，创建体积影像的 3D 可视化，交互式原型化图像处理流程，并开发面向特定成像任务的自定义插件。

### 工具总结表

| 工具                       | 副标题                                                     | 组织                        | 类别                              | 链接                                                          |
| -------------------------- | ------------------------------------------------------------ | ------------------------------------ | ------------------------------------- | ------------------------------------------------------------ |
| **FastQC**                 | 高通量测序数据质量控制工具     | Babraham Bioinformatics              | 核心 NGS 管道                     | https://www.bioinformatics.babraham.ac.uk/projects/fastqc/   |
| **Trimmomatic**            | 灵活的 Illumina NGS 数据读取修剪工具            | Usadel Lab                           | 核心 NGS 管道                     | http://www.usadellab.org/cms/?page=trimmomatic               |
| **BWA**                    | Burrows-Wheeler 比对器                                      | Heng Li Lab                          | 核心 NGS 管道                     | http://bio-bwa.sourceforge.net/                              |
| **STAR**                   | 拼接转录本到参考基因组的比对                 | Alexander Dobin                      | 核心 NGS 管道                     | https://github.com/alexdobin/STAR                            |
| **Minimap2**               | 长读长测序通用比对工具                                   | Heng Li                              | 核心 NGS 管道                     | https://github.com/lh3/minimap2                              |
| **Samtools**               | SAM/BAM/CRAM 操作工具套件                               | Genome Research Ltd                  | 核心 NGS 管道                     | http://www.htslib.org/                                       |
| **BEDTools**               | 基因组区间算术工具集                                  | Quinlan Lab                          | 核心 NGS 管道                     | https://bedtools.readthedocs.io/                             |
| **Picard**                 | 高通量测序数据处理工具集                              | Broad Institute                      | 核心 NGS 管道                     | https://broadinstitute.github.io/picard/                     |
| **SPAdes**                 | 圣彼得堡基因组组装器                                  | Center for Algorithmic Biotechnology | 基因组组装和变异分析    | https://github.com/ablab/spades                              |
| **Flye**                   | 长读长 de novo 组装器                                | Kolmogorov Lab                       | 基因组组装和变异分析    | https://github.com/fenderglass/Flye                          |
| **Canu**                   | 长读长组装工具包                                     | Koren & Walenz Labs                  | 基因组组装和变异分析    | https://github.com/marbl/canu                                |
| **QUAST**                  | 基因组组装质量评估工具                               | Center for Algorithmic Biotechnology | 基因组组装和变异分析    | https://github.com/ablab/quast                               |
| **Bandage**                | 组装图导航可视化工具                                | Ryan Wick                            | 基因组组装和变异分析    | https://github.com/rrwick/Bandage                            |
| **GATK**                   | 基因组分析工具包                                     | Broad Institute                      | 基因组组装和变异分析    | https://gatk.broadinstitute.org/                             |
| **bcftools**               | VCF/BCF 操作与变异调用工具集                         | Genome Research Ltd                  | 基因组组装和变异分析    | http://samtools.github.io/bcftools/                          |
| **Manta**                  | 结构变异检测器                                       | Illumina                             | 基因组组装和变异分析    | https://github.com/Illumina/manta                            |
| **FreeBayes**              | 贝叶斯遗传变异检测器                                 | Erik Garrison                        | 基因组组装和变异分析    | https://github.com/freebayes/freebayes                       |
| **Pindel**                 | 断点检测的模式生长方法                               | Wellcome Trust Sanger Institute      | 基因组组装和变异分析    | https://github.com/genome/pindel                             |
| **VEP**                    | 变异效应预测器                                       | EMBL-EBI / Ensembl                   | 基因组组装和变异分析    | https://www.ensembl.org/vep                                  |
| **SnpEff**                 | 变异注释与功能效应预测                               | Pablo Cingolani                      | 基因组组装和变异分析    | https://pcingola.github.io/SnpEff/                           |
| **ANNOVAR**                | 通用变异注释工具                                     | Kai Wang Lab                         | 基因组组装和变异分析    | https://annovar.openbioinformatics.org/                      |
| **DESeq2**                 | 基于计数数据的差异表达分析                           | Love, Anders, Huber                  | 转录组学和表达分析 | https://bioconductor.org/packages/DESeq2/                    |
| **edgeR**                  | 基于经验贝叶斯的差异表达分析                         | Gordon Smyth Lab                     | 转录组学和表达分析 | https://bioconductor.org/packages/edgeR/                     |
| **StringTie**              | 转录本组装与定量                                     | Johns Hopkins University CCB         | 转录组学和表达分析 | https://ccb.jhu.edu/software/stringtie/                      |
| **Salmon**                 | 超快速转录本定量                                     | Rob Patro Lab                        | 转录组学和表达分析 | https://combine-lab.github.io/salmon/                        |
| **HTSeq**                  | 高通量测序数据处理框架                               | Simon Anders Lab                     | 转录组学和表达分析 | https://htseq.readthedocs.io/                                |
| **Scanpy**                 | 单细胞 RNA-seq 分析工具包                           | Theis Lab                            | 转录组学和表达分析 | https://scanpy.readthedocs.io/                               |
| **Seurat**                 | 单细胞 RNA-seq 分析工具包                           | Satija Lab                           | 转录组学和表达分析 | https://satijalab.org/seurat/                                |
| **Cell Ranger**            | 10X Genomics 数据分析流水线                          | 10X Genomics                         | 转录组学和表达分析 | https://support.10xgenomics.com/single-cell-gene-expression/software/pipelines/latest/what-is-cell-ranger |
| **scVI**                   | 单细胞变分推断                                       | Yosef Lab                            | 转录组学和表达分析 | https://scvi-tools.org/                                      |
| **scGPT**                  | 单细胞生物学基础模型                                 | Cui Lab                              | 转录组学和表达分析 | https://scgpt.readthedocs.io/                                |
| **Squidpy**                | 空间分子数据分析工具包                               | Theis Lab                            | 转录组学和表达分析 | https://squidpy.readthedocs.io/                              |
| **Tangram**                | 单细胞到空间映射的深度学习                           | Regev Lab                            | 转录组学和表达分析 | https://tangram-sc.readthedocs.io/                           |
| **STUtility**              | 空间转录组分析与可视化                               | Lundeberg Lab                        | 转录组学和表达分析 | https://ludvigla.github.io/STUtility_web_site/               |
| **SPATA2**                 | 空间转录组分析框架                                   | Kuppe Lab                            | 转录组学和表达分析 | https://themilolab.github.io/SPATA2/                         |
| **Giotto**                 | 空间与多重成像数据分析工具箱                         | Yuan Lab                             | 转录组学和表达分析 | https://giottosuite.readthedocs.io/                          |
| **MACS2**                  | ChIP-seq 的模型化峰调用                             | Tao Liu Lab                          | 表观基因组学和调控分析     | https://github.com/macs3-project/MACS                        |
| **HOMER**                  | 基序富集的超几何优化                                | Christopher Benner                   | 表观基因组学和调控分析     | http://homer.ucsd.edu/homer/                                 |
| **MEME Suite**             | 基序发现与分析工具集                                 | Timothy Bailey Lab                   | 表观基因组学和调控分析     | https://meme-suite.org/                                      |
| **Bismark**                | 亚硫酸氢盐测序比对器                                | Babraham Bioinformatics              | 表观基因组学和调控分析     | https://www.bioinformatics.babraham.ac.uk/projects/bismark/  |
| **deepTools**              | 深度测序数据分析工具集                               | Ramírez Lab                          | 表观基因组学和调控分析     | https://deeptools.readthedocs.io/                            |
| **ATACseqQC**              | ATAC-seq 质控与分析                                  | Jianhong Ou, Julie Zhu               | 表观基因组学和调控分析     | https://bioconductor.org/packages/ATACseqQC/                 |
| **ChromHMM**               | 基于组蛋白修饰的染色质状态发现                       | Ernst & Kellis Lab                   | 表观基因组学和调控分析     | http://compbio.mit.edu/ChromHMM/                             |
| **MOFA+**                  | 多组学因子分析                                       | Ricard Argelaguet, Britta Velten     | 多组学整合               | https://biofam.github.io/MOFA2/                              |
| **Seurat V5**              | 支持多模态整合的最新 Seurat                          | Satija Lab                           | 多组学整合               | https://satijalab.org/seurat/                                |
| **MultiVI**                | 联合 RNA-seq 与 ATAC-seq 的深度模型                  | Gayoso, Steier et al.                | 多组学整合               | https://docs.scvi-tools.org/en/stable/user_guide/models/multivi.html |
| **totalVI**                | CITE-seq 概率模型                                    | Gayoso, Steier et al.                | 多组学整合               | https://docs.scvi-tools.org/en/stable/user_guide/models/totalvi.html |
| **LIGER**                  | 基因组实验关系的联结推断                             | Joshua Welch Lab                     | 多组学整合               | https://github.com/welch-lab/liger                           |
| **Scissor**                | 表型相关单细胞亚群识别                               | Duan Chen Sun                        | 多组学整合               | https://github.com/sunduanchen/Scissor                       |
| **OpenMS**                 | 质谱数据分析框架                                     | OpenMS Team                          | 特定技术工具             | https://www.openms.de/                                       |
| **MaxQuant**               | 定量蛋白组学软件平台                                 | Jürgen Cox, Max Planck Institute     | 特定技术工具             | https://www.maxquant.org/                                    |
| **ProteoWizard**           | 质谱数据转换工具集                                   | Spielberg Family Center              | 特定技术工具             | http://proteowizard.sourceforge.net/                         |
| **QIIME2**                 | 微生物生态定量分析                                   | Caporaso Lab                         | 特定技术工具             | https://qiime2.org/                                          |
| **MetaPhlAn**              | 宏基因组系统发育分析                                 | Huttenhower Lab                      | 特定技术工具             | https://github.com/biobakery/MetaPhlAn                       |
| **Kraken2**                | 宏基因组超高速分类器                                 | Derrick Wood & Steven Salzberg       | 特定技术工具             | https://github.com/DerrickWood/kraken2                       |
| **HUMAnN**                 | HMP 统一代谢分析流程                                 | Huttenhower Lab                      | 特定技术工具             | https://huttenhower.sph.harvard.edu/humann/                  |
| **NanoPlot**               | 长读长测序 QC 可视化工具                              | Wouter De Coster                     | 特定技术工具             | https://github.com/wdecoster/NanoPlot                        |
| **Medaka**                 | 基于神经网络的 Nanopore 共识修正                      | Oxford Nanopore Technologies         | 特定技术工具             | https://github.com/nanoporetech/medaka                       |
| **Racon**                  | 组装抛光的快速共识模块                               | Vaser et al.                         | 特定技术工具             | https://github.com/lbcb-sci/racon                            |
| **Clair3**                 | 长读段小变异检测深度学习模型                         | Luo et al.                           | 特定技术工具             | https://github.com/HKU-BAL/Clair3                            |
| **miRDeep2**               | microRNA 发现概率算法                                 | Friedländer Lab                      | 特定技术工具             | https://github.com/rajewsky-lab/mirdeep2                     |
| **sRNAbench**              | 小 RNA-seq 综合分析工具                               | University of Granada                | 特定技术工具             | https://bioinfo2.ugr.es/srnatoolbox/srnabench/               |
| **rMATS**                  | 转录本剪接的复合统计分析                              | Manabu Shen Lab                      | 特定技术工具             | http://rnaseq-mats.sourceforge.net/                          |
| **SUPPA**                  | 超快速可变剪接流程                                   | Eduardo Eyras Lab                    | 特定技术工具             | https://github.com/comprna/SUPPA                             |
| **LeafCutter**             | 无注释内含子切除检测方法                             | David Knowles & Jonathan Pritchard   | 特定技术工具             | https://davidaknowles.github.io/leafcutter/                  |
| **AlphaFold**              | 蛋白结构预测深度学习系统                             | DeepMind / Google                    | AI/ML 基础模型               | https://alphafold.ebi.ac.uk/                                 |
| **ESMFold**                | 基于语言模型的蛋白结构预测                           | Meta AI                              | AI/ML 基础模型               | https://esmatlas.com/                                        |
| **RoseTTAFold**            | 三轨结构预测网络                                     | David Baker Lab                      | AI/ML 基础模型               | https://github.com/RosettaCommons/RoseTTAFold                |
| **xTrimo**                 | 基因组多模态基础模型                                 | BioMap Research                      | AI/ML 基础模型               | https://github.com/biomap-research/xTrimo                    |
| **Nucleotide Transformer** | 多基因组预训练语言模型                               | InstaDeep                            | AI/ML 基础模型               | https://github.com/instadeepai/nucleotide-transformer        |
| **DNABERT**                | DNA 序列 BERT 预训练模型                              | Ji et al.                            | AI/ML 基础模型               | https://github.com/jerryji1993/DNABERT                       |
| **Geneformer**             | 单细胞 Transformer 基础模型                           | Gladstone Institutes                 | AI/ML 基础模型               | https://huggingface.co/ctheodoris/Geneformer                 |
| **scFoundation**           | 单细胞生物学基础模型                                 | BioMap Research                      | AI/ML 基础模型               | https://github.com/biomap-research/scFoundation              |
| **UCE**                    | 通用细胞嵌入                                          | Stanford SNAP Lab                    | AI/ML 基础模型               | https://github.com/snap-stanford/UCE                         |
| **DiffDock**               | 扩散式分子对接模型                                   | Corso et al. / MIT                   | AI/ML 基础模型               | https://github.com/gcorso/DiffDock                           |
| **EquiBind**               | 蛋白-配体对接的几何深度学习                           | Stärk et al. / MIT                   | AI/ML 基础模型               | https://github.com/HannesStark/EquiBind                      |
| **RFdiffusion**            | 蛋白设计的扩散式生成模型                             | David Baker Lab                      | AI/ML 基础模型               | https://github.com/RosettaCommons/RFdiffusion                |
| **IGV**                    | 整合基因组浏览器                                     | Broad Institute                      | 可视化和探索           | https://igv.org/                                             |
| **Loupe Browser**          | 10X Genomics 交互式浏览器                             | 10X Genomics                         | 可视化和探索           | https://www.10xgenomics.com/support/software/loupe-browser   |
| **cellxgene**              | 单细胞数据 Web 交互浏览器                              | Chan Zuckerberg Initiative           | 可视化和探索           | https://cellxgene.cziscience.com/                            |
| **Napari**                 | 生物影像多维查看器                                   | Napari Community                     | 可视化和探索           | https://napari.org/                                          |



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
