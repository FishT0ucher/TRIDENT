# TRIDENT: Enhancing Large Language Model Safety with Tri-Dimensional Diversified Red-Teaming Data Synthesis

Large Language Models (LLMs) excel in various natural language processing tasks but remain vulnerable to generating harmful content or being exploited for malicious purposes. 
Although safety alignment datasets have been introduced to mitigate such risks through supervised fine-tuning (SFT), these datasets often lack comprehensive risk coverage. 
Most existing datasets focus primarily on lexical diversity while neglecting other critical dimensions. 
To address this limitation, we propose a novel analysis framework to systematically measure the risk coverage of alignment datasets across three essential dimensions: **Lexical Diversity**, **Malicious Intent**, and **Jailbreak Tactics**. 
We further introduce \trident, an automated pipeline that leverages persona-based, zero-shot LLM generation to produce diverse and comprehensive instructions spanning these dimensions. 
Each harmful instruction is paired with an ethically aligned response, resulting in two datasets: \tridentCore, comprising 26,311 examples, and \tridentEdge, with 18,773 examples. 
Fine-tuning \llamathreeeight on \tridentEdge demonstrates substantial improvements, achieving an average 14.29% reduction in Harm Score, and a 20% decrease in Attack Success Rate compared to the best-performing baseline model fine-tuned on the \wildjailbreak dataset.
