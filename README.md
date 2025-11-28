# BitMark: Watermarking Bitwise Autoregressive Image Generative Models

**TL;DR:** We introduce BitMark, a radioactive watermark for bitwise image generative models and show that it remains robust against various attacks while preserving high image quality and generation speed. 

**Abstract**: State-of-the-art text-to-image models like Infinity generate photorealistic images
at an unprecedented speed. These models operate in a bitwise autoregressive
manner over a discrete set of tokens that is practically infinite in size. However,
their impressive generative power comes with a growing risk: as their outputs
increasingly populate the Internet, they are likely to be scraped and reused as
training data—potentially by the very same models. This phenomenon has been
shown to lead to model collapse, where repeated training on generated content,
especially from the models’ own previous versions, causes a gradual degradation
in performance. A promising mitigation strategy is watermarking, which embeds
human-imperceptible yet detectable signals into generated images—enabling the
identification of generated content. In this work, we introduce BitMark, a robust
bitwise watermarking framework. Our method embeds a watermark directly at
the bit level of the token stream during the image generation process. Our bitwise
watermark subtly influences the bits to preserve visual fidelity and generation speed
while remaining robust against a spectrum of removal techniques. Furthermore, it
exhibits high radioactivity, i.e., when watermarked generated images are used to
train another image generative model, this second model’s outputs will also carry
the watermark. The radioactive traces remain detectable even when only fine-tuning
diffusion or image autoregressive models on images watermarked with our BitMark.
Overall, our approach provides a principled step toward preventing model collapse
in image generative models by enabling reliable detection of generated outputs.
The code is available at [https://github.com/sprintml/BitMark](https://github.com/sprintml/BitMark).
