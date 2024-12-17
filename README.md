# CS668-Image-caption-generation
## Author

Akhila Locan

## **Affiliation**

Pace University

## **Email**

akhilalocan16@gmail.com

## **Project Description**

The goal of this project is to develop a model using deep learning techniques to extract visual features from images and generate grammatically correct captions that accurately describe those features. The model leverages convolutional neural networks (CNNs) for feature extraction and Transformers for generating descriptive captions based on the visual data.

## **Abstract of the project**: 

* Many visually impaired individuals depend on textual descriptions to comprehend visual content, but creating these captions manually is often time-consuming and labor-intensive. Automating the generation of image captions significantly improves digital accessibility, particularly on platforms like social networking and photo-sharing sites. 
* By integrating Text-to-Speech (TTS) technology, these captions can be instantly converted into speech, providing real-time access to information.
* This project explores the development of an automated image caption generation system designed to address these challenges.

## **Research Question**:
* How accurately can an AI model describe complex scenes from images?
* What level of detail is necessary in the generated captions to be useful for users with visual impairments?
* How can context be incorporated to improve the relevance of captions?

## **Dataset**:

Flickr8k Dataset
	
 *  Size: The dataset contains 8,000 images, each paired with 5 human-written captions, resulting in a total of 40,000 captions.
 *  Image Content: Features a diverse range of everyday scenes, including people, animals, objects, and activities, sourced from the Flickr photo-sharing platform. The images vary in composition, lighting, and context, ensuring diversity.
 * Captions: Each image is paired with 5 unique, natural language descriptions written from different perspectives. This variability enhances the model’s ability to generate contextually rich captions.
 
The dataset is available here: https://academictorrents.com/details/9dea07ba660a722ae1008c4c8afdd303b6f6e53b

## **Methodology**: 

This project developed a pipeline integrating deep learning techniques for generating descriptive captions from images, with captions converted to audio for accessibility.
	
* Image Feature Extraction
    I used EfficientNetB0 for extracting the image features due to its efficiency and as it also has been proven to have superior performance in image-related tasks. Its lightweight architecture makes it ideal for extracting rich features while maintaining computational efficiency. 

* Caption Generation
    The core captioning component employs an Encoder-Decoder Transformer model, where the encoder processes the extracted image features into contextual embeddings, and the decoder predicts a sequence of words as captions. The Transformer Decoder Block incorporates a causal attention mechanism to ensure captions are generated in the correct order, with attention focused on both prior generated words and the encoded image features. This allows the model to construct meaningful and fluent captions.
   
* Model Training: The model was trained for 60 epochs achieving an accuracy of 40% to generate meaningful captions for images. A plot illustrating accuracy vs. epochs showcases the training performance and model convergence.

* Text-to-Speech (TTS): Generated captions were converted into audio using the pyttsx3 library. Pyttsx3 is a lightweight, offline text-to-speech library that provides reliable and efficient speech synthesis, making it a practical choice for applications combining image captioning and auditory feedback.

* The model’s performance was evaluated using BLEU scores, which measure alignment between generated and reference captions. BLEU-1 captures word accuracy, while BLEU-4 assesses contextual fluency. Strong scores highlight the model’s ability to generate meaningful and coherent descriptions.


![Picture1](https://github.com/user-attachments/assets/f3ffb325-a0f4-4b71-86b3-f5ea188e0a93)

![Picture2](https://github.com/user-attachments/assets/98582462-1bcb-4f73-b31c-921d60aa955f)

## **Results**: 

* The proposed methodology was evaluated on the Flickr8k dataset, focusing on the contextual relevance and quality of the generated captions. The results showcase the model's ability to generate descriptive and semantically rich captions, effectively capturing the essence of the images.
* The model successfully generates detailed and meaningful captions that capture the essential elements of the images.
* It performs well in recognizing key features, such as animals and colors, providing relevant and insightful descriptions.
* These results demonstrate the model’s potential for image understanding tasks, offering valuable insights into visual content.
* The model achieved 40% accuracy, but it’s important to note that accuracy isn’t always the best indicator for performance in image captioning tasks.
* The BLEU-4 score is a more accurate measure, focusing on how fluent and meaningful descriptions are. 
* The model's high BLEU-4 score implies that it can provide fluent and human-like descriptions as shown in the examples and chart.

![Poster](https://github.com/user-attachments/assets/89a9a637-3faf-4c55-b697-6b022b6ecd20)


