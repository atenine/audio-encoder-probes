# Text Audio Embeddings Comparison

Code partially adapted from Jon Rawski's LING 165 Lab 1 and Payal Mohapatra's [Speech Disfluency Detection with Contextual Representation and Data Distillation](https://github.com/payalmohapatra/Speech-Disfluency-Detection-with-Contextual-Representation-and-Data-Distillation)

Reproduces part of English et al.'s paper on probing wav2vec embeddings, but only fits probes for the final hidden state of the encoder, as well as fitting probes for both wav2vec and whisper encoders.

## References:
Cormac English, P., Kelleher, J.D. and Carson-Berndsen, J. (2022) ‘Domain-informed probing of wav2vec 2.0 embeddings for phonetic features’, *Proceedings of the 19th SIGMORPHON Workshop on Computational Research in Phonetics, Phonology, and Morphology*, pp. 83–91. doi:10.18653/v1/2022.sigmorphon-1.9. 