# Text Audio Embeddings Comparison

Code partially adapted from Jon Rawski's LING 165 Lab 1 and Payal Mohapatra's [Speech Disfluency Detection with Contextual Representation and Data Distillation](https://github.com/payalmohapatra/Speech-Disfluency-Detection-with-Contextual-Representation-and-Data-Distillation)

Reproduces part of English et al.'s paper on probing wav2vec embeddings, but only fits probes for the final hidden state of the encoder, as well as fitting probes for both wav2vec and whisper encoders. Uses [TIMITPhones'](https://github.com/IParraMartin/TIMITPhones/tree/main) map for convenience.

Additionally, attempts dimensionality reduction on the test sets for these encoders.

## Future Plans:
- attempt HDBSCAN on the reduced-dimension versions of the embeddings
- compare HDBSCAN classifications with results from the encoders
- attempt similar probe and dimensionality reduction over only the vowels, to see if vowel-specific acoustic features are still represented
- maybe? attempt similar things over the hidden layers of both of the encoders
- similar work, but for mockingjay

## Usage:
First! Run  `generate_embeddings.ipynb` to generate and save embeddings for both wav2vec and whisper.

- `probe_training.ipynb` fits probes for manner of articulation and renders their confusion matrices.
- `voicedness_probe_training.ipynb` does the same, but with voicedness as the variable to predict.


## References:
Cormac English, P., Kelleher, J.D. and Carson-Berndsen, J. (2022) ‘Domain-informed probing of wav2vec 2.0 embeddings for phonetic features’, *Proceedings of the 19th SIGMORPHON Workshop on Computational Research in Phonetics, Phonology, and Morphology*, pp. 83–91. doi:10.18653/v1/2022.sigmorphon-1.9. 

Shah, Jui, et al. "What all do audio transformer models hear? probing acoustic representations for language delivery and its structure." *arXiv preprint arXiv:2101.00387* (2021).

Dixit, Satvik, et al. "Explaining deep learning embeddings for speech emotion recognition by predicting interpretable acoustic features." *arXiv preprint arXiv:2409.09511* (2024).

Zhang, Alice, Edison Thomaz, and Lie Lu. "Transformation of audio embeddings into interpretable, concept-based representations." *2025 International Joint Conference on Neural Networks (IJCNN)*. IEEE, 2025.

Fiorio, Luan Vinícius, et al. "Unsupervised Variational Acoustic Clustering." *arXiv preprint arXiv:2503.18579* (2025).

Baevski, Alexei, et al. "wav2vec 2.0: A framework for self-supervised learning of speech representations." *Advances in neural information processing systems 33* (2020): 12449-12460.

Radford, Alec, et al. "Robust speech recognition via large-scale weak supervision." *International conference on machine learning*. PMLR, 2023.

https://github.com/IParraMartin/TIMITPhones/tree/main
