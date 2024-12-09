# Data-Science-Project

## Overview

K’iche’ is an indigenous Mayan language spoken by ~2 million speakers in the highlands of Guatemala and parts of Mexico. K’iche’ is the second most spoken language in Guatemala after Spanish. It originates from an ancestral Proto-Mayan language about 4,000 years ago, and is best known from the Popol Vuh. 

![Idiomasmap_Guatemala svg](https://github.com/user-attachments/assets/7b0f3ac3-4519-43b8-ac29-fa0bfeccb861)

## Research Problem

There is very little accessible data for K’iche’ language. One issue regarding access to K’iche’ grammar and vocabulary lies in the various regional dialects. While different dialects may be understood by K’iche’ speakers, these differences pose challenges to non-K’iche’ speakers who have limited access to learning material. Additionally, published dictionaries or grammatical instructions often neglect regional variations or contain antiquated information from ancient texts. 

<img width="907" alt="Screenshot 2024-12-05 at 3 08 33 PM" src="https://github.com/user-attachments/assets/833e2f85-25bf-4a10-8e13-f6e08a92fb72">

Picture of Nawalja', "The Birthplace of Water"


K’iche’ has a limited amount of learning materials and a lack of online presence. In addition, K’iche’ resources accessible to the public and open source AI are largely unrevised, incorrect, or outdated. Much of the published work on K’iche’ is written for a linguistic audience, and does not convey grammatical rules or translations to a general audience. This poses an issue for large language models, such as ChatGPT and Claude ai, because they cannot be sufficiently trained on K’iche’ language. Accessible information is either unreliable, or does not provide enough data to train NLPs. 
 

### Data and Evaluation

I will be evaluating the performance of these models using datasets and assessments that I have created. I have been studying K’iche’ as a part of my graduate research, and have been assessed as a high intermediate speaker. I am providing material that is specific to the regional dialect of Nawalja’, which is more inaccessible than other dialects of K’iche’ throughout the Western Highlands of Guatemala. 

# Approach 

I address this problem by investigating the capabilities of AI models to learn indigenous language without prior training. The learning material data will be provided in two different ways to determine which approach yields better performance of the models. I will input data through descriptive prompting or in-context learning to determine 1) which type of data allows the models to score more accurately on assessments, 2) which type of data LLMs are more receptive of, and 3) which type of data suggests model learning.   

### Data

1. Descriptive Prompting: Four variations of descriptive prompting. Some variations are more complex and detailed, while some only provide the basic foundations for grammatical concepts in K'iche'.
- Prompt 1: Detail oriented. Paragraph form. Provides the most examples. 
- Prompt 2: Most concise. Bullet points, more labeled section headings. Emphasis on different rules. 
- Prompt 3: Most explanatory. Written with more natural language. Contains more descriptive structural detail: Numbered steps for verb construction and explanation of exceptions. 
- Prompt 4: Most technical. Formatted as a technical ML training specification. Includes detailed hierarchical organization using markdown headings, code blocks, and systematic categorization of language features. 
  
2. In-context learning
- Trial 1: Slightly less descriptive, contained tables to demonstrate verb conjugations and exceptions
- Trial 2: Detail oriented, utilized explanatory paragraphs to demonstrate exceptions and conjugations. 

### Forms of evaluation 

1. Accuracy
- Number of accurate responses for each question across prompts 
   
2. Receptivity
- Assessments 2 and 4 include vocabulary that is not give to the model in the inital prompt. How does the model respond to this, and how does this effect inital accuracy?
- Assessment 2 prompt: "Conjugate these verbs into 1st person with the non-completive aspect. Determine whether or not the phrase final marker (ik) is needed. You are not required to translate words, but you can if you recognize them."
- Assessment 4 prompt: "First identify each verb within the conjugated phrase. Then, translate the K’iche’ phrases into English. If you do not recognize a verb, ask for the translation."

3. Learning ability
- Determine whether or not accuracy increases without corrections
- Determine whether or not accuracy increases with corrections
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

<img width="494" alt="Screenshot 2024-12-09 at 1 52 29 AM" src="https://github.com/user-attachments/assets/da23be81-aa9c-4777-99e3-4dc58026d695">

### Patterns and consistency 

- For Assessment 2, both models consistently did not attempt translations or request definitions, with one exception: ChatGPT's in-context learning Trial 2, where it unexpectedly provided translations.
- Claude.ai never attempted to translate Assessment 2 across all trials.
- ChatGPT tended to attempt translations even when uncertain, leading to incorrect translations and occasionally expressing doubt
- When a verb was provided (e.g., Prompt 1, Assessment 4, item 3), both models could use it appropriately
  
# Evaluation 

### Performance trends  

Descriptive Prompting: Claude.ai

- Claude.ai consistently outperformed ChatGPT across all prompts
- Rarely missed Q1 across all assessments and prompts
- Assessment 3 was the most challenging across all prompts

Prompt-Specific Patterns:
- Claude.ai maintained an average accuracy above 60% for all prompt types
- Prompt 2 has a slightly higher accuracy
- Prompt 3 had a slightly lower accuracy rate than the other prompts

Descriptive Prompting: ChatGPT
- Assessment 2 showed best performance (especially in Prompts 1 and 4)
- Assessment 4 typically showed better performance than other assessments
- Assessment 5 showed worst performance across all prompts

Prompt-Specific Patterns
- Prompt 1: Most consistent partial success
- Prompt 2: High failure rate with one strong assessment
- Prompt 3: Nearly complete failure across all assessments
- Prompt 4: Most polarized (either complete success or complete failure)

### Comparison 

1. Accuracy

Descriptive Prompting

- ChatGPT had more complete assessment failures
- ChatGPT had a higher frequency of missing multiple questions in same assessment comapred to Claude
- ChatGPT had a more consistent pattern of Q4 success (opposite of Claude.ai's pattern)
- ChatGPT had a greater variance between assessments within same prompt in comparison to Claude
- ChatGPT had a more dramatic performance differences between prompts in comparison to Claude

In-Context Learning 
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
- Inconsistent pattern of improvement

2. Response to lack of information
   
Claude.ai

- Demonstrated a more conservative approach, consistently requesting translations when information was missing
- Requested fewer translations with in-context learning
- Never provided an incorrect translation

ChatGPT

- Showed more willingness to attempt translations even with uncertainty, leading to both correct and incorrect results
- Only requested one translation with in-context learning
- Variable in behavior and accuracy

3. Learning potential
- Claude.ai projects for in-context learning 

## Overall
- Claude performed marginally better with in-context learning. There was less variability in the accuracy of scores.
-  ChapGPT performed marginally better with descriptive prompting
- Pattern recognition or learning? 
  
# Critical Analysis 

## Impact

This project revealed that AI models such as Claude or ChatGPT do have the ability to learn and apply language rules that they weren't initially trained on.  

## Model Card
Claude 3.5 Sonnet






