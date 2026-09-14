# MSAR-UNet-A-Multi-Scale-Attention-Refinement-U-Net-Model-for-Microscopic-Medical-Image-Segmentation

Abstract. Automatic and accurate nuclei segmentation in histopathol-
ogy images is a fundamental task in computational pathology, yet it
remains highly challenging due to complex nuclear morphologies, vari-
ations in shape, size, and staining intensity, and frequent overlaps be-
tween nuclei. This paper proposes MSAR-UNet, a Multi-Scale Attention
Refinement U-Net, which couples two complementary modules within
a standard encoder–decoder backbone. A Multi-Scale Dilated Residual
Block (MSDRB) is embedded in the encoder to jointly capture local,
intermediate, and large-scale contextual information through parallel
standard and dilated convolutional branches with residual feature prop-
agation. A Channel-Spatial Skip Refinement Module (CSSRM) is in-
troduced along the skip connections to adaptively recalibrate encoder
features via complementary channel and spatial-attention maps, sup-
pressing less discriminative responses prior to decoder fusion. Extensive
experiments on four publicly available histopathology datasets, namely
MoNuSeg, TNBC, CoNSeP and DDT1, our model demonstrate consis-
tent improvements over the U-Net baselines and several state-of-the-art
methods. MSAR-UNet achieves Dice scores of 80.69%, 83.48%, 77.26%,
and 85.97%, with corresponding IoU scores of 67.66%, 71.65%, 62.94%,
and 75.58% on MoNuSeg, TNBC, CoNSeP, and DDT1, respectively. 




<img width="2000" height="1125" alt="overall_Final_v3-1" src="https://github.com/user-attachments/assets/02fa2fb4-c695-44b0-b481-9bdd10d479e3" />



