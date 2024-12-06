# Advanced Topics in Privacy and Security - Graph De-anonymization, Backdoor Poisoning, and Membership Inference

## Overview
This document provides an overview of three critical topics in privacy and security for machine learning and graph-based systems:
1. **Graph De-anonymization**  
2. **Backdoor Poisoning Attacks**  
3. **Membership Inference Attacks and Defenses**

Each section includes a brief explanation, attack methodology, implications, and common defenses.

---

## 1. Graph De-anonymization

### What is Graph De-anonymization?
Graph de-anonymization refers to the process of re-identifying nodes or entities in an anonymized graph by exploiting structural or external auxiliary information. This undermines efforts to maintain privacy in datasets such as social networks or transaction graphs.

### Attack Methodology
1. **Auxiliary Data**: Attackers use auxiliary datasets containing partial mappings between nodes in the anonymized graph and real-world identities.
2. **Structural Similarity**: Exploiting patterns, degree distributions, and neighborhood relationships to correlate nodes across graphs.
3. **Iterative Refinement**: Gradually aligning nodes using known mappings to infer additional matches.

### Implications
- Privacy breaches in social network data can expose sensitive user information.
- Anonymized medical or financial data can be linked to individuals, violating confidentiality.

### Defenses
- **Graph Perturbation**: Randomly adding or removing edges or nodes to obscure structural patterns.
- **Differential Privacy**: Injecting noise into graph statistics to provide formal privacy guarantees.
- **Subsampling**: Reducing the size of the graph released to limit re-identification opportunities.

---

## 2. Backdoor Poisoning Attacks

### What is a Backdoor Poisoning Attack?
Backdoor poisoning attacks occur when an adversary injects malicious data into the training dataset to create a hidden vulnerability in the trained model. The model behaves normally during standard use but produces attacker-controlled outputs when triggered by specific inputs.

### Attack Methodology
1. **Data Injection**: Inserting carefully crafted samples with a trigger pattern (e.g., watermark or pixel overlay).
2. **Training Phase Manipulation**: Poisoned data influences the model's decision boundaries.
3. **Trigger Activation**: During inference, inputs containing the trigger lead to attacker-defined predictions.

### Implications
- Compromised AI systems in critical applications (e.g., autonomous vehicles, medical diagnostics).
- Undetectable backdoors allow attackers to exploit the model without being identified.

### Defenses
- **Data Sanitization**: Identifying and removing suspicious samples from the training set.
- **Model Robustness**: Using robust training techniques such as adversarial training.
- **Trigger Detection**: Monitoring for anomalous patterns during inference.
- **Re-training or Fine-tuning**: Mitigating backdoors by re-training with verified data.

---

## 3. Membership Inference Attacks and Defenses

### What is a Membership Inference Attack?
Membership inference attacks determine whether a specific data point was included in the training dataset of a machine learning model. These attacks exploit overfitting or inconsistencies in model predictions.

### Attack Methodology
1. **Confidence Scores**: Analyzing confidence scores returned by the model to infer training membership.
2. **Overfitting Exploitation**: Identifying points that the model performs unusually well on as likely members.
3. **Shadow Models**: Training similar models to replicate the target model's behavior for inference.

### Implications
- Privacy risks for individuals whose data was used in training (e.g., medical or financial data).
- Potential regulatory violations (e.g., GDPR, HIPAA).

### Defenses
- **Differential Privacy**: Introducing noise into the training process to obscure individual contributions.
- **Regularization**: Techniques like dropout or L2 regularization to reduce overfitting.
- **Prediction Clipping**: Limiting the granularity of confidence scores returned by the model.
- **Ensemble Defenses**: Using multiple models and aggregating predictions to obscure single-model behavior.

---

## Summary Table

| **Attack**                  | **Key Feature**                             | **Impact**                                                   | **Defense Strategy**                                       |
|-----------------------------|---------------------------------------------|-------------------------------------------------------------|-----------------------------------------------------------|
| **Graph De-anonymization**  | Re-identifying nodes in anonymized graphs  | Privacy breaches in social, financial, and medical graphs   | Graph perturbation, differential privacy, subsampling     |
| **Backdoor Poisoning**      | Hidden triggers in model behavior          | Exploitation of AI systems for malicious purposes           | Data sanitization, robust training, trigger detection     |
| **Membership Inference**    | Identifying training data membership       | Privacy risks for sensitive training datasets               | Differential privacy, regularization, prediction clipping |

---

## References
1. Narayanan, A., & Shmatikov, V. "Robust De-anonymization of Large Sparse Datasets." IEEE S&P, 2008.
2. Gu, T., et al. "BadNets: Identifying Vulnerabilities in AI Systems." arXiv, 2017.
3. Shokri, R., et al. "Membership Inference Attacks Against Machine Learning Models." IEEE S&P, 2017.

---

## Contact
For questions or further details, please contact:  
**Name**: Salil Dinesh Apte 
**Email**: sapte2@student.gsu.edu  
**LinkedIn**: [https://www.linkedin.com/in/salil-apte1112/]  

---

