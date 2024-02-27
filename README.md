# Chat-KCR-Your-AI-Interviewer-for-Technical-HR-Brilliance
AI INTERVIEWER CHATBOT has three initial features to begin with and also has a feedback feature: <br>
i) Technical Interview Session: The AI Interviewer chatbot tests the technical knowledge of a candidate based on the job description mentioned by them at the beginning of the session. For example, a question may be asked on object-oriented programming if the candidate mentions it. <br>

ii) Interpersonal Interview Session: The AI Interviewer chatbot tests the internal personal skills of an individual, like the ability to interact, collaborate, and lead, by asking situation-based questions. <br>

iii) Resume-Based Session: The AI Interviewer chatbot tests the candidate based on their resume, which may include work experience, projects, and the role they opted for at the beginning of the session. <br>

iv) Feedback Feature: This feature analyses the whole conversation between the AI interviewer chatbot and candidate, evaluates the performance of the individual, and suggests improvements. <br> 

![image](https://github.com/Kushal1306/Chat-KCR-Your-AI-Interviewer-for-Technical-HR-Brilliance/assets/95643826/ad398495-26c5-492c-917b-4eb2dd267040)

 Fig. 1:  Architecture of  Retreival & Conversation Chain <br>
 
>Implementation of the above features:

Prompt templates have been created for various professional roles and interpersonal roles, which will aid  in generating interview questions that will be helpful throughout the interview conversation. The answers given by individuals are reverted back with either a follow-up question or the chatbot rectifies the answer if it finds any error in it.

The text entered by the candidate using the Natural Language Toolkit Library and create their vector embeddings, which is a technique of representing words as numbers to feed them into the large language model and make them more technically accessible. Faiss (a Facebook AI similarity search technique that works on the similarity search concept) was used to generate interview questions based on the similarity between existing interview questions and candidate responses.

The retrieval chain aids in creating interview questions, and the conversation chain maintains the conversation. A history is maintained where every latest conversation is appended to that history. Conversations are appended to Langchain's memory buffer, which stores the conversation, which would be helpful during further questions to not repeat questions and to ask follow-up questions based on the last conversation. It will contain all the information, like work experience and candidate qualifications. 

A callback function is in place, which plays a vital role during the whole process to keep the interview session going. The number of tokens consumed during the whole interview session is tracked , so that it does not exceed the capacity of the large language model. <br>

![image](https://github.com/Kushal1306/Chat-KCR-Your-AI-Interviewer-for-Technical-HR-Brilliance/assets/95643826/5c157f02-bd23-4896-8540-323bf415bcc6)

 Fig 2: Data Flow Diagram Of Proposed System <br>
 
The feedback feature analyses the whole interview conversation and evaluates the performance with the help of the feedback template. OpenAI’s GPT 3.5 is opted as large language model, and its large language models are one of the best performing models in the current AI space.
