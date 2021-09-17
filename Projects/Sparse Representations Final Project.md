### Paper Summaries
Vocab to learn:
- underdetermined system
- compressive sampling
- Adam optimizer
- Parsimony and parsimonious modeling (https://ieeexplore.ieee.org/document/7010964)
- Persuit process
- demosaicing
- impainting
- bicubic interpolation
- learned iterative shrinkage and thresholding algorithm (LISTA)


Learned D-AMP: Principled neural network based compressive image recovery
		- Literally just a ton of jargon about a minor increase in Denoising images...
		- The amount of other methods mentioned in the paper make it essentially unreadable
Learning Efficient Sparse and Low Rank Models
		- A summary of multiple different approaches to sparse modeling, comparing the performance and runtimes for each
Robust single image super-resolution via deep networks with sparse prior
		- Somewhat interesting implementation of increasing resolution on a single image using information only from that image.
		- This is done by stringing together a Consecutive Sparse Coding Based Network (CSCN) using different Sparse Coding Networks tuned to different settings.
		
Supervised deep sparse coding networks
		- Strings together a series of layers that increase and decrease resolution, training a NN on the results.

Convolutional dictionary learning: Acceleration and convergence

First-and second-order methods for online convolutional dictionary learning

Joint spatial-angular sparse coding for dMRI with separable dictionaries

Learning sparsely used overcomplete dictionaries via alternating minimization

A clustering approach to learning sparsely used overcomplete dictionaries

Local identifiability of $l$ 1-minimization dictionary learning: a sufficient and almost necessary condition

Complete dictionary recovery over the sphere I: Overview and the geometric picture

Local identification of overcomplete dictionaries

Fast and robust tensor decomposition with applications to dictionary learning

Learning sparsifying transforms

A tale of two bases: Local-nonlocal regularization on image patches with convolution framelets

Synthesis versus analysis in patch-based image priors

Learning filter bank sparsifying transforms

Separable dictionary learning with global optimality and applications to diffusion MRI

Structured overcomplete sparsifying transform learning with convergence guarantees and applications

Tradeoffs between convergence speed and reconstruction accuracy in inverse problems

Signal recovery from Pooling Representations

A compressed sensing view of unsupervised text embeddings, bag-of-n-grams, and LSTMs

Moreau, Thomas, and Joan Bruna. "Understanding trainable sparse coding via matrix factorization." arXiv preprint arXiv:1609.00285 (2016).

Chen, Yubei, Dylan Paiton, and Bruno Olshausen. "The sparse manifold transform." Advances in Neural Information Processing Systems. 2018.

Arora, Sanjeev, and Andrej Risteski. "Provable benefits of representation learning." arXiv preprint arXiv:1706.04601 (2017).

Arora, Sanjeev, et al. "Computing a Nonnegative Matrix Factorization---Provably." SIAM Journal on Computing 45.4 (2016): 1582-1611.

Candes, Emmanuel, et al. "Panning for gold:‘model‐X’knockoffs for high dimensional controlled variable selection." Journal of the Royal Statistical Society: Series B (Statistical Methodology) 80.3 (2018): 551-577.

Candes, E. J., Eldar, Y. C., Strohmer, T., & Voroninski, V. (2015). Phase retrieval via matrix completion. SIAM review, 57(2), 225-251.

Gribonval, Rémi, et al. "Sample complexity of dictionary learning and other matrix factorizations." IEEE Transactions on Information Theory 61.6 (2015): 3469-3486.

Foygel Barber, Rina, et al. "Predictive inference with the jackknife+." arXiv preprint arXiv:1905.02928 (2019).

Ba, Demba. "Deeply-Sparse Signal rePresentations." arXiv preprint arXiv:1807.01958 (2018).

Bora, Ashish, et al. "Compressed sensing using generative models." Proceedings of the 34th International Conference on Machine Learning-Volume 70. JMLR. org, 2017.

Ghosh, Avishek, and Kannan Ramachandran. "Some Performance Guarantees of Global LASSO with Local Assumptions for Convolutional Sparse Design Matrices." 2020 IEEE International Symposium on Information Theory (ISIT). IEEE, 2020.

Neyshabur, Behnam. "Towards Learning Convolutions from Scratch." arXiv preprint arXiv:2007.13657 (2020).

Champion, Kathleen, et al. "Data-driven discovery of coordinates and governing equations." Proceedings of the National Academy of Sciences 116.45 (2019): 22445-22451.

Aberdam, Aviad, Alona Golts, and Michael Elad. "Ada-LISTA: Learned Solvers Adaptive to Varying Models." arXiv preprint arXiv:2001.08456 (2020).

Lin, Tsung-Han, and Ping Tak Peter Tang. "Sparse Dictionary Learning by Dynamical Neural Networks." International Conference on Learning Representations. 2018.

Barello, Gabriel, Adam S. Charles, and Jonathan W. Pillow. "Sparse-Coding Variational Auto-Encoders." bioRxiv (2018): 399246.

Tonolini, Francesco, Bjørn Sand Jensen, and Roderick Murray-Smith. "Variational sparse coding." Uncertainty in Artificial Intelligence. PMLR, 2020.

Aubin, Benjamin, et al. "The spiked matrix model with generative priors." Advances in Neural Information Processing Systems. 2019.

Sulam, Jeremias, Chong You, and Zhihui Zhu. "Recovery and Generalization in Over-Realized Dictionary Learning." arXiv preprint arXiv:2006.06179 (2020).

Gao, Yuan, Jiayi Ma, and Alan L. Yuille. "Semi-supervised sparse representation based classification for face recognition with insufficient labeled samples." IEEE Transactions on Image Processing 26.5 (2017): 2545-2560.

Barber, Rina Foygel, Matthew Reimherr, and Thomas Schill. "The function-on-scalar LASSO with applications to longitudinal GWAS." Electronic Journal of Statistics 11.1 (2017): 1351-1389.

Mensch, Arthur, et al. "Dictionary learning for massive matrix factorization." International Conference on Machine Learning. 2016.

Pehlevan, Cengiz, and Dmitri B. Chklovskii. "Neuroscience-inspired online unsupervised learning algorithms: Artificial neural networks." IEEE Signal Processing Magazine 36.6 (2019): 88-96.

Chodosh, Nathaniel, and Simon Lucey. "When to use Convolutional Neural Networks for Inverse Problems." Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2020.

Murdock, Calvin, and Simon Lucey. "Dataless Model Selection with the Deep Frame Potential." Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition. 2020.

G. Mishne and A. S. Charles, "Learning Spatially-correlated Temporal Dictionaries for Calcium Imaging," IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP), 2019, pp. 1065-1069

Chen, Fan, and Karl Rohe. "A new basis for sparse PCA." arXiv preprint arXiv:2007.00596 (2020).

“Sparsistency and agnostic inference in sparse PCA.”