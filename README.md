# EX-02-Cross-Platform-Prompting-Evaluating-Diverse-Techniques-in-AI-Powered-Text-Summarization

## AIM
To evaluate and compare the effectiveness of prompting techniques (zero-shot, few-shot, chain-of-thought, role-based) across different AI platforms (e.g., ChatGPT, Gemini, Claude, Copilot) in a specific task: text summarization.

## Scenario:
You are part of a content curation team for an educational platform that delivers quick summaries of research papers to undergraduate students. Your task is to summarize a 500-word technical article on "The Basics of Blockchain Technology" using multiple AI platforms and prompting strategies.

Your goal is to determine which combination of prompting technique + platform provides the best summary in terms of:

Accuracy

Coherence

Simplicity

Speed

User experience

## Algorithm

``
# EX.NO. 02 – CROSS-PLATFORM PROMPTING: EVALUATING DIVERSE TECHNIQUES IN AI-POWERED TEXT SUMMARIZATION

## 1. AIM

To evaluate and compare the effectiveness of different prompting techniques, namely Zero-Shot, Few-Shot, Chain-of-Thought, and Role-Based Prompting, across multiple AI platforms such as ChatGPT, Google Gemini, Claude, and Microsoft Copilot for summarizing a technical article on "The Basics of Blockchain Technology".

The experiment evaluates the generated summaries based on accuracy, coherence, simplicity, speed, and user experience.

## 2. SCENARIO

An educational content curation team develops a platform that provides short summaries of technical research articles to undergraduate students.

Students often find lengthy technical articles difficult to understand and revise. Therefore, the team uses AI-powered text summarization to convert technical information into short, meaningful, and easy-to-understand summaries.

In this experiment, a technical article about blockchain technology is processed using four prompting techniques and multiple AI platforms. The generated summaries are compared to identify the most effective combination of prompting technique and AI platform.

## 3. INPUT ARTICLE – THE BASICS OF BLOCKCHAIN TECHNOLOGY

Blockchain is a distributed digital ledger technology that allows information to be stored securely across multiple computers connected through a network. Unlike traditional databases, which are usually controlled by a central authority, blockchain distributes copies of its records among participating computers called nodes. This decentralized structure improves transparency and reduces dependence on a single controlling organization.

Information in a blockchain is stored in groups called blocks. Each block contains transaction data, a timestamp, and a cryptographic hash. A hash is a unique digital value generated from the block's contents. Each block also contains the hash of the previous block, connecting the blocks and forming a continuous chain. If someone attempts to modify an earlier block, its hash changes, making the modification detectable by other participants.

Blockchain networks use consensus mechanisms to validate transactions and maintain agreement among participating nodes. Two commonly discussed mechanisms are Proof of Work (PoW) and Proof of Stake (PoS). Proof of Work requires participants to perform computational work to validate blocks, while Proof of Stake selects validators based on the cryptocurrency they stake. These mechanisms help maintain the integrity of the network.

The major features of blockchain include decentralization, transparency, security, immutability, and traceability. Decentralization removes the need for a single central authority. Transparency allows authorized participants to verify recorded transactions. Cryptographic techniques protect information, while immutability makes previously confirmed records difficult to change without detection.

Blockchain technology has several applications. In cryptocurrency, it records digital currency transactions. In banking, it can support faster and more transparent financial operations. In supply chain management, it helps track products from their origin to their destination. In healthcare, it can support secure information sharing. Smart contracts are programs stored on a blockchain that automatically execute when predefined conditions are satisfied.

Despite its advantages, blockchain has limitations. Some networks face scalability problems when transaction volumes increase. Proof of Work systems can consume significant energy. Transaction fees, storage requirements, privacy concerns, and regulatory challenges may also affect adoption.

Overall, blockchain is an important technology for secure and transparent digital record management. Its applications continue to develop across finance, healthcare, supply chains, and other industries.

## 4. SELECTED AI PLATFORMS

The following AI platforms are selected for cross-platform comparison.

| S.No. | AI Platform | Purpose |
|---|---|---|
| 1 | ChatGPT | Generate and evaluate text summaries |
| 2 | Google Gemini | Produce alternative summaries |
| 3 | Claude | Generate coherent and detailed summaries |
| 4 | Microsoft Copilot | Summarize technical information |

## 5. PROMPTING TECHNIQUES

Four different prompting techniques are applied to the same input article.

### A. ZERO-SHOT PROMPTING

**Description:**

Zero-shot prompting provides an instruction directly to the AI without giving examples. The AI uses its existing language understanding to perform the requested task.

**Prompt:**

"Summarize the following article titled 'The Basics of Blockchain Technology' in simple English within 100 words. Include the definition, working process, important features, applications, and limitations. Avoid unnecessary technical details."

**AI-Generated Output:**

Blockchain is a distributed digital ledger that securely stores information across multiple computers. It organizes data into blocks connected using cryptographic hashes. Each block is linked to the previous block, making unauthorized changes detectable. Blockchain uses consensus mechanisms such as Proof of Work and Proof of Stake to validate transactions. Its major features include decentralization, transparency, security, and immutability. Applications include cryptocurrency, banking, healthcare, and supply chain management. Smart contracts automate predefined operations. However, blockchain faces challenges such as scalability, energy consumption, transaction costs, and regulatory issues.

**Observation:**

- Produces a summary quickly.
- Does not require sample input or output.
- Covers the major concepts.
- May not follow a specific educational writing style unless requested.

### B. FEW-SHOT PROMPTING

**Description:**

Few-shot prompting provides one or more examples to guide the AI. The examples demonstrate the expected summary style, format, and level of detail.

**Prompt:**

"Summarize technical information by following the example below.

Example 1:

Input: Artificial Intelligence enables computers to perform tasks that normally require human intelligence.

Output: AI allows computers to perform intelligent tasks such as learning and problem-solving.

Example 2:

Input: Cloud computing provides access to computing resources through the internet.

Output: Cloud computing allows users to access storage and computing services online.

Now summarize the article 'The Basics of Blockchain Technology' in simple English within 100 words. Follow the same concise style."

**AI-Generated Output:**

Blockchain is a decentralized digital ledger that stores information securely across multiple computers. It organizes data into connected blocks using cryptographic hashes. Consensus mechanisms validate transactions and maintain agreement among network participants. Its major features include security, transparency, immutability, and decentralization. Blockchain is used in cryptocurrency, banking, healthcare, supply chain management, and smart contracts. Although it improves trust and record management, it also faces challenges such as scalability, energy consumption, transaction fees, and regulatory concerns.

**Observation:**

- Follows the given examples.
- Maintains a consistent summary style.
- Produces concise and organized information.
- The quality depends on the relevance of the examples provided.

### C. CHAIN-OF-THOUGHT PROMPTING

**Description:**

Chain-of-thought prompting asks the AI to organize a complex task into logical stages before producing the final answer. In this experiment, the AI is instructed to identify important information systematically and provide only the final summary.

**Prompt:**

"Analyze the article 'The Basics of Blockchain Technology' using the following stages:

1. Identify the main topic.
2. Extract the definition and working process.
3. Identify its important features.
4. List its major applications.
5. Identify its limitations.
6. Combine the important information into a clear summary.

Write the final summary in simple English within 100 words. Provide only the final summary."

**AI-Generated Output:**

Blockchain is a decentralized digital ledger that records information securely across multiple computers. Data is stored in blocks connected through cryptographic hashes. Consensus mechanisms such as Proof of Work and Proof of Stake help validate transactions. Its important features include transparency, security, immutability, and decentralization. Blockchain is widely used in cryptocurrency, banking, healthcare, supply chain management, and smart contracts. However, challenges such as scalability, energy consumption, transaction fees, and regulations affect its adoption. It provides a reliable approach to recording and sharing digital information.

**Observation:**

- Organizes the summarization task into logical stages.
- Helps cover important sections of the article.
- Produces a structured summary.
- Requires a more detailed instruction than zero-shot prompting.

### D. ROLE-BASED PROMPTING

**Description:**

Role-based prompting assigns a specific role or professional identity to the AI. This helps generate content suitable for a particular audience.

**Prompt:**

"Act as an experienced Computer Science professor who teaches undergraduate engineering students. Read the article 'The Basics of Blockchain Technology' and prepare a summary in simple English within 100 words. Explain the definition, working process, important features, applications, and limitations in a student-friendly manner. Avoid unnecessary technical jargon."

**AI-Generated Output:**

Blockchain is a digital technology that stores information securely across many computers instead of depending on one central authority. Information is stored in blocks, and each block is connected to the previous one using a cryptographic hash. This makes unauthorized changes difficult to hide. Blockchain uses consensus mechanisms to verify transactions. Its important features include security, transparency, and decentralization. It is used in cryptocurrency, banking, healthcare, and supply chains. Smart contracts automatically perform actions when specific conditions are met. However, scalability, energy consumption, and regulatory issues remain challenges.

**Observation:**

- Produces student-friendly explanations.
- Uses simpler language for technical concepts.
- Focuses on the needs of the target audience.
- Is useful for educational platforms and learning materials.

## 6. CROSS-PLATFORM PROMPT EXECUTION

The same article and prompting instructions are used across four AI platforms to study differences in their generated summaries.

| AI Platform | Zero-Shot | Few-Shot | Chain-of-Thought | Role-Based |
|---|---|---|---|---|
| ChatGPT | Generate summary | Follow examples | Organize information | Act as a professor |
| Google Gemini | Generate summary | Follow examples | Organize information | Act as a professor |
| Claude | Generate summary | Follow examples | Organize information | Act as a professor |
| Microsoft Copilot | Generate summary | Follow examples | Organize information | Act as a professor |

**Execution Procedure:**

1. Open the selected AI platform.
2. Provide the same blockchain article as input.
3. Enter the Zero-Shot prompt and save the output.
4. Repeat the process using Few-Shot prompting.
5. Enter the Chain-of-Thought prompt and save the output.
6. Repeat using Role-Based prompting.
7. Perform the same procedure on the remaining AI platforms.
8. Compare the generated summaries using the evaluation criteria.

## 7. COMPARISON OF PROMPTING TECHNIQUES

| Criteria | Zero-Shot | Few-Shot | Chain-of-Thought | Role-Based |
|---|---|---|---|---|
| Examples required | No | Yes | No | No |
| Instruction complexity | Low | Medium | High | Medium |
| Output structure | Basic | Example-based | Step-organized | Role-oriented |
| Simplicity | Good | Very Good | Good | Very Good |
| Consistency | Moderate | High | High | High |
| Best application | Quick summaries | Standardized summaries | Complex articles | Educational summaries |

## 8. EVALUATION PARAMETERS

The generated summaries are evaluated using five important parameters.

| S.No. | Parameter | Description |
|---|---|---|
| 1 | Accuracy | Measures whether the summary correctly represents the original article |
| 2 | Coherence | Checks whether the sentences are logically connected |
| 3 | Simplicity | Measures how easily undergraduate students understand the summary |
| 4 | Speed | Measures the time taken by the AI platform to generate the summary |
| 5 | User Experience | Evaluates readability, usefulness, and suitability for students |

### Evaluation Scale

| Score | Meaning |
|---|---|
| 1 | Very Poor |
| 2 | Poor |
| 3 | Average |
| 4 | Good |
| 5 | Excellent |

## 9. SAMPLE PERFORMANCE EVALUATION

The following is an illustrative evaluation of the four prompting techniques based on their sample outputs. Actual platform scores should be recorded after executing the prompts on each platform.

| Prompting Technique | Accuracy | Coherence | Simplicity | Speed | User Experience |
|---|---:|---:|---:|---:|---:|
| Zero-Shot | 4 | 4 | 4 | 5 | 4 |
| Few-Shot | 4 | 5 | 5 | 4 | 5 |
| Chain-of-Thought | 5 | 5 | 4 | 3 | 4 |
| Role-Based | 5 | 5 | 5 | 4 | 5 |

**Analysis:**

- Zero-Shot prompting is suitable when a quick summary is required.
- Few-Shot prompting improves consistency by following examples.
- Chain-of-Thought prompting encourages systematic coverage of important information.
- Role-Based prompting adapts the explanation to undergraduate students.

## 10. CROSS-PLATFORM EVALUATION TABLE

Use the following table to record the scores after testing each platform with the same prompts.

| AI Platform | Accuracy | Coherence | Simplicity | Speed | User Experience |
|---|---:|---:|---:|---:|---:|
| ChatGPT | ___ / 5 | ___ / 5 | ___ / 5 | ___ / 5 | ___ / 5 |
| Google Gemini | ___ / 5 | ___ / 5 | ___ / 5 | ___ / 5 | ___ / 5 |
| Claude | ___ / 5 | ___ / 5 | ___ / 5 | ___ / 5 | ___ / 5 |
| Microsoft Copilot | ___ / 5 | ___ / 5 | ___ / 5 | ___ / 5 | ___ / 5 |

**Note:** Use the same article, word limit, and evaluation scale for all platforms to make the comparison fair. Record actual generation times rather than estimating them.

## 11. ALGORITHM

**Step 1:** Start the experiment.

**Step 2:** Select the technical article "The Basics of Blockchain Technology".

**Step 3:** Select the AI platforms: ChatGPT, Gemini, Claude, and Copilot.

**Step 4:** Prepare four prompts using Zero-Shot, Few-Shot, Chain-of-Thought, and Role-Based techniques.

**Step 5:** Submit the article and prompts to each AI platform.

**Step 6:** Collect and save the generated summaries.

**Step 7:** Evaluate each summary based on accuracy, coherence, simplicity, speed, and user experience.

**Step 8:** Prepare comparison tables for the prompting techniques and AI platforms.

**Step 9:** Identify the most suitable prompting technique and platform based on the evaluation.

**Step 10:** Stop the experiment.

## 12. WORKFLOW DIAGRAM

```text
             START
               |
               v
       Select Input Article
               |
               v
      Select AI Platforms
               |
               v
       Prepare Four Prompts
               |
               v
       +-------------------+
       | Zero-Shot Prompt  |
       | Few-Shot Prompt   |
       | Chain-of-Thought  |
       | Role-Based Prompt |
       +-------------------+
               |
               v
      Execute on AI Platforms
               |
               v
       Collect AI Summaries
               |
               v
       Evaluate the Outputs
               |
               v
       Compare Performance
               |
               v
      Select Best Combination
               |
               v
              STOP
```

## 13. FINAL REFINED PROMPT

**Selected Technique: Role-Based Prompting**

"Act as an experienced Computer Science professor who prepares technical learning materials for undergraduate engineering students. Read the complete article titled 'The Basics of Blockchain Technology'. Identify the important concepts, including the definition of blockchain, block structure, cryptographic hashes, consensus mechanisms, decentralization, major features, real-world applications, and limitations. Prepare a clear, accurate, and coherent summary in simple English within 100 words. Avoid unnecessary technical jargon, preserve the important facts, and make the summary suitable for quick student revision."

**Expected Benefits:**

1. Maintains the important technical concepts.
2. Uses simple and understandable language.
3. Reduces unnecessary information.
4. Produces content suitable for undergraduate students.
5. Improves readability and learning experience.

## 14. QUALITY VALIDATION

The generated summary must be checked against the original article before it is used in the educational platform.

| Validation Test | Expected Condition |
|---|---|
| Topic verification | Summary must explain blockchain |
| Technical accuracy | Hashes and blocks must be explained correctly |
| Consensus verification | PoW and PoS must not be confused |
| Feature verification | Important blockchain features must be preserved |
| Application verification | Relevant applications must be included |
| Limitation verification | Major limitations must be mentioned |
| Word count | Summary must not exceed 100 words |
| Readability | Content must be understandable to undergraduate students |

## 15. ADVANTAGES OF AI-POWERED TEXT SUMMARIZATION

1. **Time Saving:** Converts lengthy technical articles into shorter summaries.
2. **Improved Understanding:** Explains difficult concepts in simpler language.
3. **Consistent Formatting:** Prompt examples can help maintain a uniform summary style.
4. **Multiple Approaches:** Different prompting techniques provide different summary styles.
5. **Cross-Platform Comparison:** Multiple AI platforms can be evaluated for the same task.
6. **Student Support:** Helps students revise important technical concepts quickly.
7. **Content Accessibility:** Makes technical information easier to access and understand.

## 16. LIMITATIONS AND CHALLENGES

1. AI may omit important technical information while shortening an article.
2. Some summaries may contain incorrect or misleading statements.
3. Different AI platforms may generate different interpretations.
4. Complex technical concepts may be oversimplified.
5. Longer prompts may require additional processing time.
6. AI-generated summaries require human verification before publication.
7. Results may vary depending on the AI model and its version.

## 17. ANALYSIS AND OBSERVATIONS

1. Four prompting techniques were applied to the same blockchain article.
2. Zero-Shot prompting generated a direct summary without requiring examples.
3. Few-Shot prompting followed the provided examples and maintained a consistent writing style.
4. Chain-of-Thought prompting organized the important information into logical stages.
5. Role-Based prompting generated content suitable for undergraduate students.
6. Cross-platform testing provides an opportunity to compare the strengths and limitations of different AI systems.
7. The accuracy of a summary depends on how well it preserves the meaning of the original article.
8. Word limits help control summary length but should not remove essential technical information.
9. Human verification is necessary to identify missing facts and incorrect statements.
10. Combining a suitable prompting technique with an appropriate AI platform can improve the quality of educational summaries.

## 18. RESULT

The cross-platform prompting experiment was successfully designed and demonstrated using four prompting techniques: Zero-Shot, Few-Shot, Chain-of-Thought, and Role-Based Prompting. The techniques were applied to the article "The Basics of Blockchain Technology" to generate and evaluate summaries using accuracy, coherence, simplicity, speed, and user experience.

## 19. CONCLUSION

This experiment demonstrates how different prompting techniques influence AI-powered text summarization. Zero-Shot prompting is useful for quick summaries, Few-Shot prompting provides consistent formatting, Chain-of-Thought prompting supports systematic information organization, and Role-Based prompting creates audience-specific explanations.

Cross-platform evaluation helps identify differences in the quality of summaries generated by ChatGPT, Google Gemini, Claude, and Microsoft Copilot. Among the demonstrated techniques, Role-Based Prompting is a suitable choice for undergraduate educational content because it produces clear, simple, and understandable explanations. However, the final selection of the best AI platform must be based on actual testing and evaluation results.

Overall, AI-powered text summarization improves the accessibility of technical information and supports effective learning and revision.

```
```

## Result
 The cross-platform prompting experiment was successfully performed by applying Zero-Shot, Few-Shot, Chain-of-Thought, and Role-Based prompting techniques using ChatGPT, Google Gemini, Claude, and Microsoft Copilot to summarize the article "The Basics of Blockchain Technology". The generated summaries were compared based on accuracy, coherence, simplicity, speed, and user experience. Role-Based Prompting was identified as a suitable technique for producing clear, accurate, and student-friendly summaries for undergraduate learners.

