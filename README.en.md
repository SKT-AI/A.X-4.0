<div align="center">
  <img src="./A.X_logo.png" alt="A.X Logo" width="300"/>
</div>
<br>
<p align="center"> <a href="https://huggingface.co/collections/skt/ax-4-68637ebaa63b9cc51925e886">🤗 Models</a>   |   <a href="https://sktax.chat/chat">💬 Chat</a>   |   <a href="https://github.com/SKT-AI/A.X-4.0">🖥️ Github</a> </p>

# A.X 4.0: Foundation Model Specialized in Korean, Optimized for Enterprise Applications

[**🇰🇷 View Korean README**](README.md)

SK Telecom released **A.X 4.0** (pronounced "A dot X"), a large language model (LLM) optimized for Korean-language understanding and enterprise deployment, on April 30, 2025. Built on the open-source [Qwen2.5](https://huggingface.co/collections/Qwen/qwen25-66e81a666513e518adb90d9e) model, A.X 4.0 has been further trained with large-scale Korean datasets to deliver outstanding performance in real-world business environments.

## What Sets A.X 4.0 Apart?

- **Superior Korean Proficiency**: Achieved a score of 78.3 on [KMMLU](https://huggingface.co/datasets/HAERAE-HUB/KMMLU), the leading benchmark for Korean-language evaluation and a Korean-specific adaptation of MMLU, outperforming GPT-4o (72.5).
- **Deep Cultural Understanding**: Scored 83.5 on [CLIcK](https://huggingface.co/datasets/EunsuKim/CLIcK), a benchmark for Korean cultural and contextual comprehension, surpassing GPT-4o (80.2).
- **Efficient Token Usage**: A.X 4.0 uses approximately 33% fewer tokens than GPT-4o for the same Korean input, enabling more cost-effective and efficient processing.
- **Long Context Handling**: Supports up to 131,072 tokens, allowing comprehension of lengthy documents and conversations.
- **Domain Adaptability**: Enhanced capabilities for technical domains such as coding and manufacturing.
- **Deployment Flexibility**: Offered in both a 72B-parameter standard model and a 7B lightweight version, with on-premises installation supported for data-sensitive enterprises.

## Key Technologies

### Korean-Optimized Tokenizer

A.X 4.0 uses a tokenizer designed to capture the linguistic nuances of Korean. Internal tests show it is 33.3% more token-efficient than GPT-4o for the same Korean sentence.

Benefits in real-world application:

- Handling \~1.5x more Korean content under the same token budget
- Up to 34% cost savings in token-based billing
- Advantageous in token-based pricing or time-sensitive environment

In the enterprise deployment environment that usually treats long-form tasks like summarization and RAG, token-efficient model contributes to save management cost.

### High-Quality Korean Training Data

A.X 4.0 is trained with:

- **Large-scale, high-quality Korean corpora**: High-quality Web data, professional books, technical publications, synthetic data
- **Domain-balanced datasets**: Curated for a wide range of enterprise scenarios
- **Balanced language mix**: 42% Korean, 51% English, 7% other languages and code

This allows the model to grasp subtle expressions and context in Korean with high fidelity.

### Efficient Training Process

The training pipeline includes:

- **Tokenizer Aligning**: Replaced original tokenizer with Korean-optimized version
- **Continued Pre-Training (CPT)**: Improved Korean comprehension and overall language understanding  with large-scale Korean corpora
- **Supervised Fine-Tuning (SFT)**: Enhanced accuracy in responding to various instructions or questions using task-specific high-quality Korean datasets
- **Reinforcement Learning from Human Feedback (RLHF)**: Further tuned using human preference data from users' feedback

This approach enables efficient resource use and domain-focused performance improvements by intensively utilizing Korean data.

## Benchmark Comparison

A.X 4.1 is a reasoning model that is being developed alongside A.X 4.0. Here is a brief comparison of the key benchmark results of A.X 4.0 and A.X 4.1.

### A.X 4.0 (Knowledge-Oriented Model)

| Metric        | Task                             | A.X-4.0 (72B) | GPT-4o   | Qwen3 (235B MoE) |
| ------------- | -------------------------------- | ------------- | -------- | ---------------- |
| **KMMLU**     | Professional knowledge in Korean | 78.3          | 72.5     | 70.6             |
| **CLIcK**     | Korean culture                   | 83.5          | 80.2     | 77.9             |
| **Ko-IFEval** | Instruction following            | 78.0          | 75.4     | 77.7             |
| **Average**   |                                  | **79.9**      | **76.0** | **75.4**         |

### A.X 4.1 (Reasoning-Oriented Model)

| **Metric**    | **Task**                         | **A.X-4.1 (72B)** | **DeepSeek-R1 (671B MoE)** | **DeepSeek-R1-0528 (671B MoE)** |
| ------------- | -------------------------------- | ----------------- | -------------------------- | ------------------------------- |
| **MMLU**      | Professional knowledge           | 88.0              | 90.8                       | 92.0                            |
| **KMMLU**     | Professional knowledge in Korean | 73.3              | 76.1                       | 70.4                            |
| **Ko-IFEval** | Instruction following            | 77.0              | 77.4                       | 74.5                            |
| **CLIcK**     | Korean culture                   | 79.9              | 85.3                       | 81.5                            |
| **MATH500**   | Math & logic                     | 96.5              | 97.3                       | 98.3                            |
| **GPQA**      | Graduate-level QA                | 67.5              | 71.5                       | 81.0                            |
| **Average**   |                                  | **80.4**          | **83.1**                   | **83.0**                        |

## Use Cases

A.X 4.0 can be integrated into various enterprise applications:

- Korean document drafting support
- Summarization and search over large internal corpora written in Korean
- On-premises deployment for secure environments

## Deployment Options

- **API Service**

  - Usage-based pricing
  - SDKs and code samples for common programming languages

- **On-Premises Installation**

  - Ideal for security-sensitive industries
  - Quantized model variants for efficient deployment

- **Hybrid Model**

  - Combined API and on-premises support
  - Custom deployments through enterprise consultation

## Technical Support

- **Inquiry channels** for usage questions
- **Deployment guides** tailored to enterprise needs
- **Developer resources** including documentation and code examples
- **Regular updates** and performance enhancements

## Roadmap

SK Telecom will continue developing the A.X series. Research is underway, especially with the support of code writing in a Korean language environment in mind. The ability to understand comments or documents written in Korean and generate code optimized for the domestic corporate environment will greatly improve the productivity of domestic developers.

- **A.X 4.1 (H1 2025)**: Reasoning-oriented model

  - Stronger capabilities in math and programming by thinking through several steps
  - Developer-centric features trained on vive-coding data&#x20;

- **Future Plans (H2 2025 and beyond)**:

  - Deeper domain expertise (e.g., manufacturing, finance) and coding capability
  - Integration with agents and MCP (Model Context Protocol)
  - Efficient large-scale inference using MoE (Mixture of Experts)

## Conclusion

A.X 4.0 is SK Telecom’s enterprise-ready LLM, combining powerful Korean language proficiency with deployment flexibility and token efficiency. It enables Korean companies to leverage AI securely and effectively in their internal workflows.

For inquiries, please contact: **[a.x@sk.com](mailto\:a.x@sk.com)**

