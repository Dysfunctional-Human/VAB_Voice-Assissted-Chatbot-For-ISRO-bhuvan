 Hello fellow developers. This is my very first Github project.
 And so, I present to you:
## VAB - Voice Assissted Chatbot for ISRO Bhuvan
You can find the tutorial video for the model as "model.mp4"

###This project was initially made for the IISF Space Innovation Festival Hackathon 2023.
The chatbot uses prompt engineering on Gemini LLM to give the users a seamless chatting experience for the bhuvan portal.
This repository consists of 2 different models in the sam.ipynb notebook-

#1. Speech to Text

This notebook utilizes speech to text to take even voice input in addition to the obvious chat input.
This project makes use of the open-source AI4BHARAT's IndicWav2Vec model for speech to text transcription.
The model has been trained on the common voice dataset and specializes in various Indian languages, and provides transcriptions in very little time.
This model outperforms Whisper API's HuggingFace version's tiny, small and base models for Hindi to English transcription. For the medium Whisper model, the results are relatively same but whisper takes much longer to transcribe than Wav2Vec.
Eg. For recording 9, in the rec folder of this repository, the transcription took an average of 4.5 seconds each time by Wav2Vec while Whisper's medium version (the version that had good accuracy) took over 10 seconds.
the documentation for the mdoel is can be accessed here
https://ai4bharat.iitm.ac.in/areas/speech-recognition/

#2. Text Generation

Since I wanted to make this project open-source, instead of going for paid LLMs like gpt-4, I decided to opt for Google Gemini LLM. The api-key can be accessed just via a free google account.
In this project, I used the Langchain library to make a LLM chain that can help in passing system prompts along with user question to the LLM.
Prompt engineering was made use of to personalise the gemini LLM.
The documentation for langchain can be found below.
https://python.langchain.com/docs/get_started/introduction

At last, I have also incorporated google translator to give back the answer in english since gemini LLM generates answer in the same language as the input message, but that might not always be what the user wants
So, this makes sure that the user gets the answer in both, the language they gave the input in and also its english translation




