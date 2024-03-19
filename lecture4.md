# Antmicro 19.03
Intro: ..., Possible internships in AI, back-end, front-end, Open Source...
## Neural network deployment
| preparing model architecture / analyzing, splitting and preprocessing dataset | -> | model training | <-> | model evaluation |
Additional steps in the last 2 years.
... <-> Model optimization and compilation -> deployment on hardware
## Why running NN on IOT?
- cloud independence
- security and privacy : no potentially sensitive data is sent to a remote location
- latency : passing data to the Cloud significantly increases processing time
- Reliability : the network communication is unreliable
- scalability : in the long run, IoT-based machine learning solutions are far more scalable than centrilized could solutions
## Why can it be difficult?
- high memory demand
- high computational demand
- there are not too many models fitting as is into IoT devices
- models that does actually fir into the device may not be sufficient for a given task
- frameworks for NN development are not optimized for edge use cases
## Why optimize?
- reduction of memory footprint
- less computational demand
- etc.
## Model compression algorythms
- size comes from:
    - high-precision weights
    - it's easier to limit large model than scaling up a small model
- possible improvements:
    - ...
- what can we expect from compression algorithms
    - smaller storage size
    - smaller size of the model during runtime
    - smaller inference time during runtime
    - worse quality of predictions (we sacrifice precision in exchange for smaller model)
## Quantization - motivation
Quantization is the process of reducing the number of bits used to represent weights in the neural network
We can quantize weights, and activations
*Example of targeting weight's types (?)*
We target into smaller  weights.
*FP32 -> FP16 -> Int8 -> Int4 -> ...
## Uniform vs Non-uniform quantization
in uniform quantization, all quantized values are uniformly spaced.
in non-uniform quantizatino, discrete quantization...
It got interesting, and typing distracts me so I'm stopping :D
Some of the variables can be pre-computed during quantization, and some cannot.
## Layerwise vs channelwise quantization
... vs more configurability but momre resources are needed
## Post-training quantization
Post-trainiing quantization is the process of computing quantization parameters
