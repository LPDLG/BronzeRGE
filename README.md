# BronzeRGE

## Project Profile

This repository is used for the research project **BronzeRGE**, an attribute-controllable native 3D PBR material generation framework for bronze ware assets. The project focuses on generating and editing physically based rendering (PBR) material properties of bronze artifacts under structured attribute control. In addition to image-based visual evidence, the framework introduces explicit material-related attributes such as dominant color, patina type, corrosion state, roughness, metallic appearance, surface wear, and decorative texture. These attributes are used as editable control variables for studying how native 3D generation models can respond to fine-grained material instructions while preserving the visual identity of the input artifact.

## BronzeRGE

Recent native 3D generation models have achieved impressive progress in single-image 3D asset generation, especially in geometry reconstruction, textured mesh generation, and structured latent representation. However, most existing methods are still primarily driven by image conditions. The image condition usually entangles geometry, texture, illumination, camera viewpoint, and material appearance into a single visual representation, making it difficult to explicitly control fine-grained PBR attributes. For bronze ware generation, this limitation is especially important because material appearance is closely related to historical aging, patina formation, corrosion patterns, surface roughness, and decorative motifs.

To address this problem, we propose **BronzeRGE**, an attribute-controllable native 3D PBR material generation framework for bronze ware assets. Instead of treating material appearance as an implicit by-product of image-to-3D generation, BronzeRGE represents material properties as structured and editable attribute fields. These fields are transformed into attribute conditions and injected into the native 3D generation process together with image features. The goal is to make the generation process not only visually plausible, but also controllable at the material-attribute level.

The current framework mainly contains two technical components. First, a structured PBR attribute conditioning mechanism is designed to convert material-related information into explicit control signals, including material category, dominant color, patina state, corrosion pattern, roughness level, and surface texture description. Second, an attribute-bound latent training strategy is introduced to encourage the generated latent representation to preserve and respond to the structured attributes, instead of relying only on the strong image condition. The training strategy includes conservative residual injection, independent condition dropout, and attribute-level alignment or feedback constraints.

For evaluation, we adopt a paired controllability protocol. Given the same input image, random seed, sampling steps, camera setting, and post-processing parameters, only one structured attribute field is modified at a time. This setting is designed to isolate the effect of the target attribute from stochastic sampling variance. The expected evaluation includes attribute gap, attribute consistency, directional correctness, PBR material consistency, visual quality, and user preference studies.

## Dataset

The project is built around bronze ware 3D assets and rendered views, with additional structured material annotations. The planned dataset construction includes bronze ware image collection, geometry-texture alignment, PBR material standardization, and structured attribute labeling. The attribute fields are designed to describe both visible material appearance and editable semantic properties of bronze artifacts.

The dataset is currently being curated and standardized. A subset of examples, annotations, and evaluation splits will be released when the project reaches a stable stage.

## Code

The training code, inference scripts, controllability evaluation tools, and dataset processing utilities will be uploaded after the method and experiments are finalized. The repository will include scripts for:

- structured PBR attribute annotation and normalization;
- native 3D PBR generation with attribute conditions;
- paired fixed-seed attribute editing experiments;
- attribute gap and attribute consistency evaluation;
- qualitative visualization of material editing results.

## Citation

If you find this project useful, please cite our work after the paper is released.

```bibtex
@article{BronzeRGE,
  title   = {BronzeRGE: Attribute-Controllable Bronze Ware PBR Material Generation via Value-Contrastive Conditioning and Parallel Attribute Injection},
  author  = {Hu, Qiyao and Yang, Yubo and Yi, Qinrui and Peng, Xianlin and Peng, Jinye},
  journal = {ACM Transactions on Graphics},
  year    = {2026}
}
```

## Contact

For questions about the project, please contact the authors from the School of Electronic Information, Northwest University.
