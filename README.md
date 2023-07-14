###**Solution**

Evaluate the urgency of patient's illness based on measuring distress levels from the preconsultation evaluation of the patient, where the patient tells the model its current illness. Through that, the model will be able to tell how much distress the patient is in based on the way the patient has explained it. This will be meaningful during pandemic periods where everyone has similar symptoms but with varying severity. Through the evaluation, the model can decide how urgent the patient is in need to see the doctor, which becomes a factor in the queueing order of the telemedcine app to consider.

###**Process**
Using a derivative of Bidirectional Encoder Representations from Transformers (BERT), RoBERTta, a model in HuggingFace, to evaluate the emotions of the speaker based on the content of the speech. Throug evaluating the emotions, we can better understand the emotional distress, a product of their physical symptoms, to better prioritise patients in high distress for teleconsultation during overwhelming periods.

HuggingFace Page: https://huggingface.co/arpanghoshal/EmoRoBERTa

The dataset that the solution will be using to showcase will be a conversation of the patient consultation with the doctor, where the patient's side of the conversation will be extracted and evaluated line by line. I understand that tone and intonation can also be used to tell emotions, but in this context it will be purely focused on the textual content of the conversation.

Dataset Link: https://www.nature.com/articles/s41597-022-01423-1#Sec3

The dataset has both audio and text transcripted from the audio. For ease of access, as the text transcription was also by an AI model, I have decided not to reinvent the wheel and uses the text version, but the audio files are still kept as reference.



