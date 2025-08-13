---
title: "Spatial Reasoning in Multimodal LLMs via CoT Distillation and Monte Carlo Tree Search for Dutch Facade-Element Detection"
excerpt: "Exploring spatial reasoning capabilities in state-of-the-art Multimodal LLMs for Dutch building renovation, introducing the DuTCh SpaCE framework to enhance reasoning and reduce hallucinations."
tags: [AI, MultimodalLLM, SpatialReasoning, CoT, MonteCarloTreeSearch, DutchArchitecture, BuildingRenovation, LoRA, KnowledgeDistillation]
collection: portfolio
---

## Abstract

In this exploratory work, we investigate the spatial reasoning capabilities of state-of-the-art Multimodal Large Language Models (MLLMs) in the context of building renovation. We evaluate models with different capacities, including GPT-4o, Qwen, Mulberry, and SpatialRGPT on a few-shot dataset of Dutch residential buildings, assessing their performance in visual reasoning tasks. To this end, we propose DuTCh Space, a novel application of Chain-of-Thought Distillation consisting of a Dual-Teacher Framework that leverages both step-by-step rationales and scene graph description augmentation to guide and assess student models' performance on spatial reasoning. This structured supervision enables iterative refinement of spatial reasoning through domain-task decomposition and scene understanding. Additionally, we integrate Monte Carlo Tree Search at inference time to improve reasoning-path selection under visual uncertainty. By combining distillation and MCTS, we observe a measurable reduction in hallucinations, with models generating more grounded and verifiable predictions. Our findings demonstrate that reasoning-enhanced models can compensate for limited visual grounding even without scene graph augmentation, offering a scalable path toward spatially-aware MLLMs in low-resource, domain-specific settings


---

## Thesis Presentation (PDF)

<iframe 
    src="files/Master_Thesis_Presentation_Riccardo_Campanella_8175721.pdf" 
    frameborder="0" 
    width="100%" 
    height="800px" 
    style="border: none;">
</iframe>

[Download Project Poster (PDF)](https://riccardocampanella.github.io/rc-homepage/files/Master_Thesis_Presentation_Riccardo_Campanella_8175721.pdf)

---

### Project Overview

This project investigates the potential of **state-of-the-art Multimodal Large Language Models (MLLMs)** to identify architectural features relevant to **energy-efficient building renovation** in Dutch residential facades.

We propose **DuTCh SpaCE** — a **Dual-Teacher Chain-of-Thought Distillation** framework combined with **Monte Carlo Tree Search (CoMCTS)** — to enhance **spatial reasoning** and **reduce hallucinations** in zero-shot and few-shot setups.

Our evaluation compares **reasoning-based** and **spatially-grounded** MLLM architectures, exploring their trade-offs in domain-specific visual tasks.

## Motivation

- **Problem**: Manual facade assessments are costly and slow.  
- **Gap**: Current vision models lack **domain-specific architectural knowledge**.  
- **Opportunity**: MLLMs can leverage **contextual reasoning** for **zero-shot** detection of renovation-relevant features.  

### Target Features
Grouped by reasoning complexity:
1. **Visual Recognition** — weep holes, chimneys, balconies.  
2. **Geometric Inference** — dormers, pitched roofs, window counts.  
3. **Semantic Understanding** — attics as living spaces, ventilation systems.  
4. **Context Analysis** — vegetation growth, photovoltaic panels.

---

## Research Questions

**Main RQ**  
Are SoTA Multimodal LLMs beneficial for identifying housing renovation concepts on Dutch building facades?

- **RQ1**: Compare CoT reasoning (Qwen) vs. 3D scene graph methods (SpatialRGPT) in zero-shot.  
  - Performance vs. GPT-4o.  
  - Bounding box guidance effects.  

- **RQ2**: How can CoT reasoning MLLMs be enhanced for spatial recognition?  
  - Scene graph augmentation.  
  - LoRA fine-tuning capabilities.  

---

## Contributions

1. **First systematic MLLM evaluation** on real Dutch facade data.  
2. **DuTCh SpaCE**: Dual-teacher CoT distillation to reduce hallucinations.  
3. **Reasoning vs. grounding** trade-off analysis.  
4. **LoRA + Distillation + Test-time Search** pipeline for low-data domains.  

---

## Methodology

- **Models under study**: GPT-4o, SpatialRGPT (base/bbox), Qwen2-7B-VL.  
- **Data**: 45 curated Dutch facade images with feature annotations (yes/no/unknown/count).  
- **Evaluation**: Zero-shot + LoRA fine-tuning, 10 runs per config, metrics: Accuracy, Balanced Accuracy, F1, MAE/MSE.  

---

## Key Findings

- GPT-4o leads across metrics.  
- Bounding box guidance improves SpatialRGPT by **~15%** in accuracy.  
- DuTCh SpaCE reduces hallucinations significantly.  
- LoRA fine-tuning narrows GPT-4o gap from 20% to 8%.  
- Scene graph augmentation yields no improvement for Qwen.  

---

## Limitations

- Small dataset (45 images).  
- Imbalanced feature presence. (Mitigated by Balanced Accuracy Metric in this study) 
- Scene graph integration underused by some architectures.  
- Limited test-time search iterations.  

---

## Future Work

- Scale dataset to **1000+ images** via scraping + filtering.  
- Fine-tune multimodal encoders for vision grounding.  
- Increase CoMCTS iterations and diversity.  
- Explore RLHF strategies, multi-adapter LoRA, grounded CoT, DoRA.

---

## Conclusion

MLLMs **are beneficial** for facade analysis when enhanced with reasoning frameworks like DuTCh SpaCE.  
**Reasoning can compensate** for limited visual grounding, and domain expertise can rival raw model scale.
