# cs668-Image-caption-generation
## Author

Akhila Locan

## **Affiliation**

Pace University

## **Email**

akhilalocan16@gmail.com

## **Project Description**

The goal of this project is to develop a model using deep learning techniques to extract visual features from images and generate grammatically correct captions that accurately describe those features. The model leverages convolutional neural networks (CNNs) for feature extraction and Transformers for generating descriptive captions based on the visual data.

## **Abstract of the project**: 

Many visually impaired individuals depend on textual descriptions to comprehend visual content, but creating these captions manually is often time-consuming and labor-intensive. Automating the generation of image captions significantly improves digital accessibility, particularly on platforms like social networking and photo-sharing sites. By integrating Text-to-Speech (TTS) technology, these captions can be instantly converted into speech, providing real-time access to information. This project explores the development of an automated image caption generation system designed to address these challenges. By combining computer vision and natural language processing, the system generates textual descriptions of images and converts them into speech, enabling visually impaired users to access and interact with visual content more independently. Using the Flickr8k dataset, this study evaluates and compares two neural network architectures—injecting image features into RNNs versus merging them later. The results demonstrate the effectiveness of this approach in fostering inclusivity and enhancing digital accessibility for visually impaired users.

## **Research Question**:
* How accurately can an AI model describe complex scenes from images?
* What level of detail is necessary in the generated captions to be useful for users with visual impairments?
* How can context be incorporated to improve the relevance of captions?

## **Dataset**:

Flickr8k Dataset
	
        •       Size: The dataset contains 8,000 images, each paired with 5 human-written captions, resulting in a total of 40,000 captions.
	
	•	Image Content: Features a diverse range of everyday scenes, including people, animals, objects, and activities, sourced from the Flickr photo-sharing platform. The images vary in composition, lighting, and context, ensuring diversity.
 
	•	Captions: Each image is paired with 5 unique, natural language descriptions written from different perspectives. This variability enhances the model’s ability to generate contextually rich captions.
 
The dataset is available here: https://academictorrents.com/details/9dea07ba660a722ae1008c4c8afdd303b6f6e53b

## **Methodology**: 

This project developed a pipeline integrating deep learning techniques for generating descriptive captions from images, with captions converted to audio for accessibility.
	
1. Image Feature Extraction
    I used EfficientNetB0 for extracting the image features due to its efficiency and as it also has been proven to have superior performance in image-related tasks. Its lightweight architecture makes it ideal for extracting rich features while maintaining computational efficiency. 

2. Caption Generation
    The core captioning component employs an Encoder-Decoder Transformer model, where the encoder processes the extracted image features into contextual embeddings, and the decoder predicts a sequence of words as captions. The Transformer Decoder Block incorporates a causal attention mechanism to ensure captions are generated in the correct order, with attention focused on both prior generated words and the encoded image features. This allows the model to construct meaningful and fluent captions.
   
3. Model Training: The model was trained for 60 epochs achieving an accuracy of 40% sufficient to generate meaningful captions for images. A plot illustrating accuracy vs. epochs showcases the training performance and model convergence.

4. Text-to-Speech (TTS): Generated captions were converted into audio using the pyttsx3 library. Pyttsx3 is a lightweight, offline text-to-speech library that provides reliable and efficient speech synthesis, making it a practical choice for applications combining image captioning and auditory feedback.

5. The model’s performance was evaluated using BLEU scores, which measure alignment between generated and reference captions. BLEU-1 captures word accuracy, while BLEU-4 assesses contextual fluency. Strong scores highlight the model’s ability to generate meaningful and coherent descriptions.


## **Results**: 

The proposed methodology was evaluated on the Flickr8k dataset, focusing on the contextual relevance and quality of the generated captions. The results showcase the model's ability to generate descriptive and semantically rich captions, effectively capturing the essence of the images. 

 Key observations from the evaluation include:
 
          • Strengths of the Model:The model performs well in recognizing prominent objects such as animals and identifying colors present in the images. This demonstrates its ability to understand visual elements and generate meaningful descriptions for diverse scenes.
          • Limitations:While the model excels at recognizing objects and colors, it currently struggles to identify genders, race, and the exact number of people/animals in images.

The results underscore the potential of the model for applications that require image understanding, with generated captions offering meaningful insights into visual content.



