# Lab 2 - Interventional experiments in cells

*Large scale cell painting assay visualizes effects of drugs and knockouts*

## Learning Objectives
- Understand cell painting assays and high-content screening principles
- Learn to process and analyze large-scale phenomics datasets
- Apply dimensionality reduction and batch correction techniques
- Search for drug-gene interactions
- Interpret biological significance of computational results


## Glossary

- **Phenomics**: Large-scale study of phenotypes (observable characteristics) and their changes due to genetic or environmental factors
- **Cell Painting**: High-content screening assay using fluorescent dyes to visualize multiple cellular components simultaneously
- **High-Content Screening (HCS)**: Automated microscopy technique that captures detailed cellular images for drug discovery and biological research
- **HUVEC**: Human Umbilical Vein Endothelial Cells - commonly used cell line for vascular biology research
- **CRISPR/Cas9**: Gene editing technology used to create targeted gene knockouts
- **Perturbation**: Experimental intervention (genetic knockout or chemical treatment) that alters cellular state
- **Plates & wells**: Standardized laboratory containers where plates contain multiple wells (typically 96, 384, or 1536 wells) arranged in a grid format. Each well serves as an individual sample.
- **Biological replicate**: Independent experimental samples that undergo the same treatment conditions but are processed separately from the beginning (different cell cultures, different days, etc.). Biological replicates help assess the reproducibility and statistical significance of biological effects. For example, the same drug treatment applied to cells from different passages of the same cell line.
- **Technical replicate**: Multiple measurements or observations taken from the same biological unit under identical conditions. Technical replicates help assess measurement precision and reduce random noise, but do not account for biological variation. For example, applying the same treatment to multiple wells containing cells from the same culture flask on the same day.
- **Batch (experimental)**: A group of samples processed together at the same time under the same experimental conditions (same day, same reagent lots, same equipment). Experimental batches can introduce systematic technical variations.
- **Batch (machine learning)**: Asubset of the dataset processed together in a single iteration of model training
- **Small Molecule**: Low molecular weight organic compound, typically a potential drug candidate
- **Cell morphology**: The shape and structure of a cell
- **Batch Effects**: Systematic technical variations between experimental runs that can confound biological signals
- **Embeddings**: High-dimensional numerical representations of images learned by machine learning models
- **Feature Extraction**: Process of converting raw data (images) into measurable numerical features
- **Vision Transformer (ViT)**: Deep learning architecture that applies transformer models to image analysis
- **Center-Scaling**: Normalization technique that subtracts the mean and divides by standard deviation within each batch (aka. z-score normalization)
- **PCA (Principal Component Analysis)**: Dimensionality reduction technique that identifies major sources of variation
- **Euclidean Distance**: The straight-line distance between two points in multi-dimensional space, calculated as the square root of the sum of squared differences between corresponding coordinates: $d_{euclidean}(x,y) = \sqrt{\sum_{i=1}^{n}(x_i - y_i)^2}$
- **Cosine Distance**: A measure of dissimilarity based on the angle between two vectors, independent of their magnitudes. Calculated as one minus the cosine similarity: $d_{cosine}(x,y) = 1 - \frac{x \cdot y}{||x|| \cdot ||y||} = 1 - \frac{\sum_{i=1}^{n}x_i y_i}{\sqrt{\sum_{i=1}^{n}x_i^2}\sqrt{\sum_{i=1}^{n}y_i^2}}$
