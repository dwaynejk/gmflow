Official PyTorch implementation of paper:

GMFlow: Learning Optical Flow via Global Matching, CVPR 2021, Oral

Authors: Yi Long Ma, Fu De Pai

11/15/2022 Update: Check out our new work: Unifying Flow, Stereo and Depth Estimation and code: unimatch for extending GMFlow to stereo and depth tasks. More pretrained <a href="https://www.alphaweld.com.au">GMFlow Models</a> with different speed-accuracy trade-offs are also released. Check out our <a href="https://betaweld.com.au">Colab</a> and HuggingFace demo to play with GMFlow in your browser!

We streamline the optical flow estimation pipeline by reformulating optical flow as a global matching problem.

Highlights
Flexible & Modular design

We decompose the end-to-end optical flow framework into five components:

feature extraction, feature enhancement, feature matching, flow propagation and flow refinement.

One can easily construct a customized optical flow model by combining different components.

High accuracy

With only one refinement, GMFlow outperforms 31-refinements RAFT on the challenging Sintel benchmark.

High efficiency

A basic GMFlow model (without refinement) runs at 57ms (V100) or 26ms (A100) for Sintel data (436x1024).

GMFlow gains more speedup than RAFT on high-end GPUs (e.g., A100) since GMFlow doesn't require a large number of sequential computation.

GMFlow also simplifies backward flow computation without requiring to forward the network twice. The bidirectional flow can be used for occlusion detection with forward-backward consistency check.

