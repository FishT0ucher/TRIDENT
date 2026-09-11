# TRIDENT: Enhancing Large Language Model Safety with Tri-Dimensional Diversified Red-Teaming Data Synthesis

**Abstract:** Large Language Models (LLMs) excel in various natural language processing tasks but remain vulnerable to generating harmful content or being exploited for malicious purposes. 
Although safety alignment datasets have been introduced to mitigate such risks through supervised fine-tuning (SFT), these datasets often lack comprehensive risk coverage. 
Most existing datasets focus primarily on lexical diversity while neglecting other critical dimensions. 
To address this limitation, we propose a novel analysis framework to systematically measure the risk coverage of alignment datasets across three essential dimensions: **Lexical Diversity**, **Malicious Intent**, and **Jailbreak Tactics**. 
We further introduce **TRIDENT**, an automated pipeline that leverages persona-based, zero-shot LLM generation to produce diverse and comprehensive instructions spanning these dimensions. 
Each harmful instruction is paired with an ethically aligned response, resulting in two datasets: **TRIDENT-Core**, comprising **26,311** examples, and **TRIDENT-Edge**, with **18,773** examples. 
Fine-tuning **Llama3.1-8B** on **TRIDENT-Edge** demonstrates substantial improvements, achieving an average **14.29%** reduction in Harm Score, and a **20%** decrease in Attack Success Rate compared to the best-performing baseline model fine-tuned on the **WildJailbreak**.


![image](https://github.com/FishT0ucher/TRIDENT/blob/master/unbalance.png)
Instruction classification in six **baseline** red-teaming datasets and **TRIDENT-Core** using **Llama-Guard** reveals a heavily skewed distribution, with most instructions concentrated in domains like Violent Crimes, Non-Violent Crimes and Sexual Content.

![image](https://github.com/FishT0ucher/TRIDENT/blob/master/Pipeline%20.png)
Illustration of our **data generation pipeline** for building **TRIDENT**


## 📝 Citation

If you find this dataset useful, please cite our **ACL 2025** paper:

```bibtex
@inproceedings{wu-etal-2025-trident,
    title = "{TRIDENT}: Enhancing Large Language Model Safety with Tri-Dimensional Diversified Red-Teaming Data Synthesis",
    author = "Wu, Xiaorui  and
      Mao, Xiaofeng  and
      Li, Fei  and
      Zhang, Xin  and
      Li, Xuanhong  and
      Teng, Chong  and
      Ji, Donghong  and
      Li, Zhuang",
    editor = "Che, Wanxiang  and
      Nabende, Joyce  and
      Shutova, Ekaterina  and
      Pilehvar, Mohammad Taher",
    booktitle = "Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (Volume 1: Long Papers)",
    month = jul,
    year = "2025",
    address = "Vienna, Austria",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.acl-long.733/",
    doi = "10.18653/v1/2025.acl-long.733",
    pages = "15077--15099",
    ISBN = "979-8-89176-251-0",
```
