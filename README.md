Jason's Thesis Landing Page

### [FlexLoc](https://arxiv.org/abs/2406.06796)

Localization is a critical technology for various applications ranging from navigation and surveillance to assisted living. Localization systems typically fuse information from sensors viewing the scene from different perspectives to estimate the target location while also employing multiple modalities for enhanced robustness and accuracy. Recently, such systems have employed end-to-end deep neural models trained on large datasets due to their superior performance and ability to handle data from diverse sensor modalities. However, such neural models are often trained on data collected from a particular set of sensor poses (i.e., locations and orientations). During real-world deployments, slight deviations from these sensor poses can result in extreme inaccuracies. To address this challenge, we introduce FlexLoc, which employs conditional neural networks to inject node perspective information to adapt the localization pipeline. Specifically, a small subset of model weights are derived from node poses at run time, enabling accurate generalization to unseen perspectives with minimal additional overhead. Our evaluations on a multimodal, multiview indoor tracking dataset showcase that FlexLoc improves the localization accuracy by almost 50% in the zero-shot case (no calibration data available) compared to the baselines.

The code repository for FlexLoc can be found [here](https://github.com/nesl/FlexLoc).

### [ADMN](https://arxiv.org/abs/2502.07862)

Multimodal deep learning systems are deployed in dynamic scenarios due to the robustness afforded by multiple sensing modalities. Nevertheless, they struggle with varying compute resource availability (due to multi-tenancy, device heterogeneity, etc.) and fluctuating quality of inputs (from sensor feed corruption, environmental noise, etc.). Statically provisioned multimodal systems cannot adapt when compute resources change over time, while existing dynamic networks struggle with strict compute budgets. Additionally, both systems often neglect the impact of variations in modality quality. Consequently, modalities suffering substantial corruption may needlessly consume resources better allocated towards other modalities. We propose ADMN, a layer-wise Adaptive Depth Multimodal Network capable of tackling both challenges: it adjusts the total number of active layers across all modalities to meet strict compute resource constraints and continually reallocates layers across input modalities according to their modality quality. Our evaluations showcase ADMN can match the accuracy of state-of-the-art networks while reducing up to 75% of their floating-point operations.

The code repository for ADMN can be found [here](https://github.com/nesl/ADMN).


### [SWAN](https://arxiv.org/abs/2604.26181)

Multimodal deep neural networks deployed in realistic environments must contend with runtime variations: changes in modality quality, overall input complexity, and available platform resources. Current networks struggle with such fluctuations -- adaptive networks cannot adhere to a strict compute budget, controller-based networks neglect to consider input complexity, and statically provisioned networks fail at all the above. Consequently, they do not extract maximum utility from the expended computational resources. We present SWAN (Sample and World-Aware Multimodal Network), the first adaptive multimodal network that accomplishes all three goals. SWAN employs a quality-aware controller to assign resources among modalities according to a variable user-specified maximum budget. Within this budget, an adaptive gating module further optimizes efficiency by scaling layer utilization according to sample complexity. For further gains, SWAN also employs a token dropping module that masks semantically irrelevant multimodal features before performing detections. We evaluate SWAN in the domain of autonomous driving with complex multi-object 3D detection, reducing FLOPs by up to 49% with minimal degradation.

The code repository for SWAN can be found [here](https://github.com/nesl/SWAN).

