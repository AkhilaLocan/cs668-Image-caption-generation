# cs668-Image-caption-generation
## Akhila Locan



**Abstract of the project**: 

Many visually impaired individuals depend on textual descriptions to comprehend visual content, but creating these captions manually is often time-consuming and labor-intensive. Automating the generation of image captions significantly improves digital accessibility, particularly on platforms like social networking and photo-sharing sites. By integrating Text-to-Speech (TTS) technology, these captions can be instantly converted into speech, providing real-time access to information. This project explores the development of an automated image caption generation system designed to address these challenges. By combining computer vision and natural language processing, the system generates textual descriptions of images and converts them into speech, enabling visually impaired users to access and interact with visual content more independently. Using the Flickr8k dataset, this study evaluates and compares two neural network architectures—injecting image features into RNNs versus merging them later. The results demonstrate the effectiveness of this approach in fostering inclusivity and enhancing digital accessibility for visually impaired users.

**Research Question**:
* How accurately can an AI model describe complex scenes from images?
* What level of detail is necessary in the generated captions to be useful for users with visual impairments?
* How can context be incorporated to improve the relevance of captions?



**Dataset**:

Flickr8k Dataset
	•	Size: The dataset contains 8,000 images, each paired with 5 human-written captions, resulting in a total of 40,000 captions.
	•	Image Content: Features a diverse range of everyday scenes, including people, animals, objects, and activities, sourced from the Flickr photo-sharing platform. The images vary in composition, lighting, and context, ensuring diversity.
	•	Captions: Each image is paired with 5 unique, natural language descriptions written from different perspectives. This variability enhances the model’s ability to generate contextually rich captions.
 
The dataset is available here: https://academictorrents.com/details/9dea07ba660a722ae1008c4c8afdd303b6f6e53b

**Methodology**: 

This project developed a pipeline integrating deep learning techniques for generating descriptive captions from images, with captions converted to audio for accessibility.
	
 1.	Image Feature Extraction
	•	Utilized EfficientNetB0, known for its lightweight yet powerful architecture, to extract rich image features efficiently. This model ensures optimal performance in handling diverse image content.
	
 2.	Caption Generation
	•	Deployed an Encoder-Decoder Transformer model:
	•	Encoder: Processes extracted image features into contextual embeddings.
	•	Decoder: Employs a causal attention mechanism to generate a sequence of words for captions, focusing on both prior outputs and encoded image features. This enables fluent and contextually accurate caption generation.
	
 3.	Model Training
	•	The model was trained for 5 epochs, achieving an accuracy of 38%, sufficient to produce meaningful captions.
	•	A training performance plot (accuracy vs. epochs) demonstrates steady convergence over the last 5 epochs.
	
 4.	Text-to-Speech (TTS)
	•	Integrated Tacotron 2 for converting generated captions into audio. Tacotron 2 is widely recognized for its high-quality, natural-sounding speech, ensuring accessible auditory feedback.

**Results**: 

The proposed methodology successfully generates descriptive and semantically rich captions for images, demonstrating strong performance in recognizing prominent objects, such as animals, and identifying colors, which highlights its ability to understand visual elements in diverse scenes. The integration of Text-to-Speech (TTS) technology further enhances accessibility by converting captions into natural-sounding audio, enabling visually impaired individuals to interact with visual content independently. Overall, this project showcases the potential of combining computer vision and natural language processing to create inclusive solutions for digital accessibility, laying a strong foundation for future advancements in automated image captioning systems.


