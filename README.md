### Solution

Evaluate the urgency of a patient's illness based on measuring distress levels from the preconsultation evaluation of the patient, where the patient tells the model its current illness. Through that, the model will be able to tell how much distress the patient is in based on the way the patient has explained it. This will be meaningful during pandemic periods where everyone has similar symptoms but with varying severity. Through the evaluation, the model can decide how urgent the patient is in need to see the doctor, which becomes a factor in the queueing order of the telemedicine app to consider.

### Process

Using a derivative of Bidirectional Encoder Representations from Transformers (BERT), RoBERTa, a model in HuggingFace, to evaluate the emotions of the speaker based on the content of the speech. Through evaluating the emotions, we can better understand the emotional distress, a product of their physical symptoms, to better prioritize patients in high distress for teleconsultation during overwhelming periods.

HuggingFace Page: [https://huggingface.co/arpanghoshal/EmoRoBERTa](https://huggingface.co/arpanghoshal/EmoRoBERTa)

The dataset that the solution will be using to showcase will be a conversation of the patient consultation with the doctor, where the patient's side of the conversation will be extracted and evaluated line by line. I understand that tone and intonation can also be used to tell emotions, but in this context, it will be purely focused on the textual content of the conversation.

Dataset Link: [https://www.nature.com/articles/s41597-022-01423-1#Sec3](https://www.nature.com/articles/s41597-022-01423-1#Sec3)

The dataset has both audio and text transcribed from the audio. For ease of access, as the text transcription was also by an AI model, I have decided not to reinvent the wheel and use the text version, but the audio files are still kept as a reference.


## User Personas

### Dr. Mai Too Liao
- **Name:** Dr. Mai Too Liao
- **Age:** 38
- **Location:** Yishun, Singapore
- **Specialty:** Family Medicine

**Background:**
Dr. Mai Too Liao is an experienced internal medicine physician who has been practicing for over 10 years. She has a passion for providing patient-centered care and has always been an early adopter of technology to improve her practice. With the rise in telemedicine and the Covid-19 pandemic, she has transitioned her practice to primarily focus on teleconsultations.

**Frustrations:**
- Managing a high volume of patients while ensuring quality care
- Assessing the severity of a patient's condition through teleconsultation, especially for those presenting with ARI symptoms
- Adapting to the constantly evolving healthcare landscape during the pandemic
- Balancing the need for patient privacy and data security with the convenience of telemedicine platforms

**Needs:**
- Provide efficient and effective healthcare solutions to her patients in a timely manner
- Keep up with the increasing demand for telemedicine services
- Maintain a work-life balance despite the challenges of the Covid-19 pandemic
- Continuously learn about new technologies and strategies to improve her teleconsultation practice


### Severely Ill Patient with Covid-19
- **Name:** Emily Buay Ta Han
- **Age:** 32
- **Location:** Yishun, Singapore

**Background:**
Emily is a 32-year-old professional working in a corporate job. She lives alone in a one-bedroom apartment in a busy city. Recently, she tested positive for Covid-19 using a personal test kit.

**Frustrations:**
- Emily is struggling with severe Covid-19 symptoms, making it difficult for her to handle daily tasks.
- The high demand for healthcare services during the pandemic has led to long wait times for appointments.
- She is worried about her condition worsening and not being able to access medical help in time.

**Needs:**
- To receive medical attention and medication without leaving her home.
- Reliable teleconsultation service that connects her to a healthcare professional quickly.
- An efficient prescription and medication delivery system.
- A way to track her symptoms and receive personalized advice to manage her condition.
