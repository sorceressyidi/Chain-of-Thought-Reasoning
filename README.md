### README

#### **Inference with Chain of Thought (CoT) Based on LLM**

---

#### **Project Description**
This project explores methodologies to enhance the accuracy of inference in Large Language Models (LLMs) using the Chain of Thought (CoT) approach. It focuses on implementing and evaluating three primary methods: Multi-vote, LoRA fine-tuning, and Multi-path step-aware inference. These techniques aim to improve reasoning capabilities in LLMs, particularly for tasks requiring logical progression, such as algebraic problem-solving and reasoning benchmarks.

---

#### **Development Environment**
- **Platform**: Google Colab / Ubuntu 22.04
- **Framework**: PyTorch 2.3.0 (cu121)
- **Key Libraries**: 
  - `transformers 4.41.2`
  - `modelscope 1.15.0`

---

#### **Methods Implemented**
1. **Multi-vote**: Aggregates predictions from multiple reasoning paths to enhance prediction robustness using majority voting.
2. **LoRA Fine-tuning**: A parameter-efficient method that introduces low-rank matrix updates to fine-tune the LLM with minimal computational resources.
3. **Multi-path Step-aware Inference**: Inspired by DiVeRSe, this method uses diverse reasoning paths and a step-aware verifier to achieve higher accuracy in complex tasks.

---

#### **Dataset**
- **AQuA**: A dataset of algebraic word problems from [AQuA Dataset Repository](https://github.com/deepmind/AQuA).

---

#### **Key Contributions**
- Introduced novel enhancements to the CoT reasoning pipeline.
- Achieved improved accuracy metrics on reasoning benchmarks through iterative experimentation.
- Demonstrated the potential of efficient fine-tuning methods like LoRA in resource-constrained environments.

---

#### **Results**
- Multi-vote achieved 20% accuracy on a subset of AQuA.
- LoRA fine-tuning achieved 26% accuracy across 100 questions.
- Multi-path step-aware inference demonstrated 21% accuracy on 40 questions, showcasing potential for scaling.

---

#### **How to Run**
1. Install dependencies:
   ```bash
   pip install torch transformers modelscope
   ```
2. Run the Jupyter notebooks located in the `code/` directory:
   - `multi-vote.ipynb`
   - `lora_tune.ipynb`
   - `Step-Aware.ipynb`

---

#### **Future Improvements**
- Expand experiments with larger datasets and diverse hyperparameter settings.
- Explore additional prompts to capture richer reasoning paths.
- Optimize inference pipelines to improve stability and scalability.

---

#### **References**
1. Li, Yifei, et al. *"Making large language models better reasoners with step-aware verifier."* arXiv:2206.02336 (2022).
2. [Alpaca-CoT](https://github.com/PhoebusSi/Alpaca-CoT)


