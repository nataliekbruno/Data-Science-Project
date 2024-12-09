# Indigenous Language Learning Abilities of LLMs

## Overview

Are LLMs able to learn languages that they have not been trained on when provided with limited data?  

K’iche’ is an indigenous Mayan language spoken by ~2 million speakers in the highlands of Guatemala and parts of Mexico. K’iche’ is the second most spoken language in Guatemala after Spanish. It originates from an ancestral Proto-Mayan language about 4,000 years ago, and is popularly known from an ancient Maya document, the Popol Vuh. 

![Idiomasmap_Guatemala svg](https://github.com/user-attachments/assets/7b0f3ac3-4519-43b8-ac29-fa0bfeccb861)

## Research Problem

There is very little accessible data for K’iche’ language. K’iche’ has a limited amount of learning materials and a lack of online presence. In addition, K’iche’ resources accessible to the public and open source AI are largely unrevised, incorrect, or outdated. This poses an issue for large language models, such as ChatGPT and Claude ai, because they cannot be sufficiently trained on K’iche’ language. Accessible information is either unreliable, or does not provide enough data to train LLMs. 

Another issue regarding access to K’iche’ grammar and vocabulary lies in the various regional dialects. While different dialects may be understood by K’iche’ speakers, these differences pose challenges to non-K’iche’ speakers with limited access to learning material.  

<img width="907" alt="Screenshot 2024-12-05 at 3 08 33 PM" src="https://github.com/user-attachments/assets/833e2f85-25bf-4a10-8e13-f6e08a92fb72">

Picture of Nawalja', "The Birthplace of Water"

I address this question by investigating the capabilities of AI models to learn the indigenous language K'iche' without prior training or extensive resources. 


# Approach 

The learning material data will be provided in two different ways to determine which approach yields better performance of the models. I will input data through descriptive prompting and in-context learning to determine 1) which type of data allows the models to score more accurately on assessments, 2) which type of data LLMs are more receptive of, and 3) which type of data suggests model learning. 

Following this analysis, I will also assess the performance of each model to determine which is better at learning K'iche'. 

## Data

I will be evaluating the performance of these models using datasets and assessments that I have created. I am providing material that is specific to the regional dialect of Nawalja’, which is less accessible than other dialects of K’iche’ throughout the Western Highlands of Guatemala. 

### Types of Data: 

1. Descriptive Prompting: Four variations of descriptive prompting. Some variations are more complex and detailed, while some only provide the basic foundations for grammatical concepts in K'iche'.
- Prompt 1: Detail oriented. Paragraph form. Provides the most examples. 
- Prompt 2: Most concise. Bullet points, more labeled section headings. Emphasis on different rules. 
- Prompt 3: Most explanatory. Written with more natural language. Contains more descriptive structural detail: Numbered steps for verb construction and explanation of exceptions. 
- Prompt 4: Most technical. Formatted as a technical ML training specification. Includes detailed hierarchical organization using markdown headings, code blocks, and systematic categorization of language features. 
  
2. In-context learning
- Trial 1: Slightly less descriptive, contained tables to demonstrate verb conjugations and exceptions
- Trial 2: Detail oriented, utilized explanatory paragraphs to demonstrate exceptions and conjugations. 

Assessments:
- 4 assessments, each with 5 questions
- All assessments are able to be answered with prompt and data set information

## Forms of evaluation 

### 1. Accuracy
- Number of accurate responses for each question across prompts
- Can score 1, 0.5, or 0
   
### 2. Response to lack of information/Receptivity
- Assessments 2 and 4 include vocabulary that is not give to the model in the inital prompt. How does the model respond to this, and how does this effect inital accuracy?
- Assessment 2 prompt: "Conjugate these verbs into 1st person with the non-completive aspect. Determine whether or not the phrase final marker (ik) is needed. You are not required to translate words, but you can if you recognize them."
- Assessment 4 prompt: "First identify each verb within the conjugated phrase. Then, translate the K’iche’ phrases into English. If you do not recognize a verb, ask for the translation."

### 3. Learning ability
- Determine whether or not accuracy increases with more assessments and corrections
- Determine whether or not accuracy increases without prior assessments and corrections
- Give a final assessment after giving the model correct answers
  
# Results

## 1. Accuracy of Models

### Claude.ai Overall Performance 

<img width="657" alt="Screenshot 2024-12-08 at 11 26 44 PM" src="https://github.com/user-attachments/assets/7fb73444-6c06-4f6a-9552-9f84fc25be18">

### ChatGPT Overall Performance 

<img width="633" alt="Screenshot 2024-12-08 at 11 30 15 PM" src="https://github.com/user-attachments/assets/dacf2b4c-a411-42d1-aca9-34ef9bd77392">

### Claude.ai and ChaptGPT Performance: Descriptive prompting 

<img width="626" alt="Screenshot 2024-12-08 at 11 41 39 PM" src="https://github.com/user-attachments/assets/17972506-ea21-4321-9484-3af6aef323d8">

### Claude.ai and ChatGPT Performance: In-Context learning

<img width="779" alt="Screenshot 2024-12-08 at 11 36 55 PM" src="https://github.com/user-attachments/assets/56743aee-4533-4edc-9c9d-a353a7ba2605">

## 2. Response to lack of information

### Claude vs. ChatGPT

<img width="494" alt="Screenshot 2024-12-09 at 1 52 29 AM" src="https://github.com/user-attachments/assets/da23be81-aa9c-4777-99e3-4dc58026d695">

### Patterns and Consistency in Responses

- For Assessment 2, both models consistently did not attempt translations or request definitions, with one exception: ChatGPT's in-context learning Trial 2, where it unexpectedly provided translations.
- Claude.ai never attempted to translate Assessment 2 across all trials.
- ChatGPT tended to attempt translations even when uncertain, leading to incorrect translations and occasionally expressing doubt
- When a verb was provided (e.g., Prompt 1, Assessment 4, item 3), both models could use it appropriately

## 3. Learning abilities 

K'iche' translation accuracy for Assessments 6-8, with prior assessments and correct answers vs. without prior assessments and answers

<img width="561" alt="Screenshot 2024-12-09 at 1 24 13 PM" src="https://github.com/user-attachments/assets/feafcdc5-e2ed-42bc-825e-bc7b2609021d">

Assessment 6: Both scored 100% accuracy
Assessment 7: Both scored 80% accuracy
Assessment 7 revision with provided vocab: Both scored 90% accuracy
Assessment 8: Both scored 80% accuracy 

# Evaluation 

## Performance Trends across Descriptive Prompting: Prompts 1-4

Descriptive Prompting: Claude

- Claude consistently outperformed ChatGPT across all prompts
- Rarely missed Q1 across all assessments and prompts
- Assessment 3 was the most challenging across all prompts

Prompt-Specific Patterns:
- Claude maintained an average accuracy above 60% for all prompt types
- Prompt 2 has a slightly higher accuracy
- Prompt 3 had a slightly lower accuracy rate than the other prompts

Descriptive Prompting: ChatGPT
- Assessment 2 showed best performance (especially in Prompts 1 and 4)
- Assessment 4 typically showed better performance than other assessments
- Assessment 5 showed worst performance across all prompts

Prompt-Specific Patterns:
- Prompt 1: Most consistent partial success
- Prompt 2: High failure rate with one strong assessment
- Prompt 3: Nearly complete failure across all assessments
- Prompt 4: Most polarized (either complete success or complete failure)

## Performance Trends across in-context learning: Trials 1 and 2

In-context learning: Claude
- Performed slightly better with Trial 1 data set
- Slightly less variability in responses

In-context learning: ChatGPT
- Performed slightly better with Trial 2
- Both trials showed inconsistent results and complete failure on entire assessments

## Comparison 

### 1. Accuracy

Descriptive Prompting

- ChatGPT had more complete assessment failures
- ChatGPT had a higher frequency of missing multiple questions in same assessment comapred to Claude
- ChatGPT had a more consistent pattern of Q4 success (opposite of Claude.ai's pattern)
- ChatGPT had a greater variance between assessments within same prompt in comparison to Claude
- ChatGPT had a more dramatic performance differences between prompts in comparison to Claude

In-context Learning 

Trial 1: Claude.ai
- Claude.ai showed exceptional performance:
- Near-perfect scores across all assessments
- Showed consistent improvement

Trial 1: ChatGPT 
- Lower overall scores
- Inconsistent performance across assessments

Trial 2: Claude.ai
- Claude.ai maintained strong performance:
- Started lower in Assessment 1 but quickly improved
- Showed some variation in Assessment 3
- Maintained high accuracy overall

Trial 2: ChatGPT
- ChatGPT showed more variability:
- Had one strong performance (Assessment 2)
- Significant decline in final assessment
- Performed better on trial 2 than trial 1

### 2. Response to lack of information
   
Claude.ai:

- Demonstrated a more conservative approach, consistently requesting translations when information was missing
- Requested fewer translations with in-context learning
- Never provided an incorrect translation

ChatGPT:

- Showed more willingness to attempt translations even with uncertainty, leading to both correct and incorrect results
- Only requested one translation with in-context learning
- Variable in behavior and accuracy

### 3. Learning potential (Claude only)

- Claude did not show significant differences with more context
- Accuracy scores remained the same, with Assessment 7 having different questions answered incorrectly 

## Demonstration: Claude 

Assessment 9: Translate into K'iche'

1. I am able to talk to her
2. I am making it
3. We are giving you the huipil 
4. The men removed the cat
5. He wrote his book

Answers 

1. Kinkowinik kinch’ab’ej. 
2. Kinb’ano
3. Katqaya’ le po’t
4. Xkelesaj le me’s le achijab’
5. Xutz’ib’aj awuj. 

## Overall

- Claude performed marginally better with in-context learning. There was less variability in the accuracy of scores.
-  ChapGPT performed marginally better with in-context learning 
- Claude seems to have a more holistic approach, including information from both the prompts/data and correct responses at times
- ChatGPT seems to randomize answers, demonstrating a less systematic approach
  
# Critical Analysis 

## Impact

This project revealed that AI models such as Claude or ChatGPT do have the ability to learn and apply language rules that they weren't initially trained on. However, the ability to consistently apply all information correctly seems to vary at times. 

In-context learning seems to support better model performance for learning K'iche' language. 

### Next Steps

- More-indepth investigation of descriptive prompt and model performance: How can we optimize descriptive prompts for AI in order to produce more accurate results?
- Assess Claude or ChatGPT's performance with increased rounds of questioning
- Issues with chat length and memory storage: Claude projects allows for a large amount of project knowledge in the form of text files, but requires new chats more frequently than ChatGPT. 

## Model Card

1. Claude 3.5 Sonnet, released by Anthropic in October 2024 as part of the Claude 3 model family. claude.ai

2. ChatGPT 4o, released by OpenAI in 2024. chat.openai.com

## Resource links

1. Using AI in educational and writing context:
   
Albadarin, Y., Saqr, M., Pope, N. et al. A systematic literature review of empirical research on ChatGPT in education. Discov Educ 3, 60 (2024). https://doi.org/10.1007/s44217-024-00138-2

2. AI case studies: Translation abilities

Ferrag, F., & Bentounsi, I. A. (2024). The use of artificial intelligence in academic translation tasks: Case study of Chat GPT, Claude, and Gemini. Ziglôbitha, Revue des Arts, Linguistique, Littérature & Civilisations, 2(11), 173–192. https://doi.org/10.60632/ziglobitha.n011.11.vol.2.2024

3. Assesses Claude's performance on low resource languages 

Enis, M., & Hopkins, M. (2024). From LLM to NMT: Advancing Low-Resource Machine Translation with Claude. arXiv. https://doi.org/10.48550/arXiv.2404.13813

4. Descriptions of Claude's different abilities and models

https://www.machinetranslation.com/blog/claude-ai-3-5?utm_source=chatgpt.com 

5. Assessing ChatGPT's performance with descriptive prompting 

He, S. (2024). Prompting ChatGPT for Translation: A Comparative Analysis of Translation Brief and Persona Prompts. Proceedings of the 25th Annual Conference of the European Association for Machine Translation (Volume 1), 316–326. European Association for Machine Translation (EAMT). https://aclanthology.org/2024.eamt-1.27




