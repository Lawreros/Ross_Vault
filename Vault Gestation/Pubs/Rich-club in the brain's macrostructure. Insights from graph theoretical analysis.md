Article: Rich-club in the brain's macrostructure: Insights from graph theoretical analysis
tags: #manuscript 
backlinks:
Authors: Dae-Jin Kim, Byoung-Kyong Min
Journal: Computational and Structural Biotechnology Journal
Date Published: June 2020
DOI: 10.31887/DCNS.2018.20.2/agriffa
URL: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC7355726/

### Abstract
The brain is a complex network. Growing evidence supports the critical roles of a set of brain regions within the brain network, known as the brain’s cores or hubs. These regions require high energy cost but possess highly efficient neural information transfer in the brain’s network and are termed the [[rich-club]]. The rich-club of the brain network is essential as it directly regulates functional integration across multiple segregated regions and helps to optimize cognitive processes. Here, we review the recent advances in rich-club organization to address the fundamental roles of the rich-club in the brain and discuss how these core brain regions affect brain development and disorders. We describe the concepts of the rich-club behind network construction in the brain using graph theoretical analysis. We also highlight novel insights based on animal studies related to the rich-club and illustrate how human studies using neuroimaging techniques for brain development and psychiatric/neurological disorders may be relevant to the rich-club phenomenon in the brain network

### Introduction
 An early finding from the macroscopic brain network perspective was that the human brain is organized in a highly efficient manner for integrated information transfer, known as *small-world topology*. Two assumptions are postulated to form a small-world network:
 1) A subgroup of network elements should form dense, interconnected clusters to confirm local network segregation, as defined by a clustering coefficient. A higher clustering coefficient of each network element often leads to network communities or modules. 
 2) Lengths or distances between any pairs of network elements, often defined by the reciprocal of the connectivity strength, should be shorter for a greater degree of global integration, resulting in a lower _shortest path length_.
 
 The small-world topology designates networks in which the clustering coefficient is significantly larger than (and the shortest path length is similar to) those of randomly connected networks, defined as _small-worldness_. However, the existence of small-world topology provides limited information on network architecture and has several pitfalls in terms of its evaluation, utility, and interpretation. As such, more appropriate network measures such as _modularity_ have been proposed to characterize local and global network architecture. Network modules (i.e., communities or clusters) are defined by a set of network elements with a number of interconnections within each module and fewer connections among modules.

Several findings have suggested the following: (1) brain network modules possess a large number of relatively short connections among adjacent brain regions, and (2) these modules are interconnected via a limited set of network nodes termed _network hubs,_ which play central roles in neuronal information flow. Hub regions in brain network modules are defined by network nodes with a larger number of connections and have been identified in the cat, macaque, and human brain. Hubs are classified into two categories: _connector hubs_ corresponding to the interconnection among network modules and _provincial hubs_ within each network module. Damage to connector hub regions (e.g., lesions) causes larger disturbances across widespread brain networks.

### Methods
#### Construction of neuronal networks
As a suitable alternative to investigate macroscale neural networks, MRI has been used extensively to define whole brain wiring diagrams _in vivo_ for larger neural systems, enabling the comparison of network characteristics across species. Since the introduction of white matter fiber tractography, an MRI-based 3D reconstruction technique that visualizes neural tracts using water diffusivity in the brain predominantly with diffusion tensor imaging (DTI), noninvasive neuroimaging methods such as DTI have been utilized for macroscopic brain network analysis. Other methods for constructing complete whole-brain networks include functional modalities such as functional MRI (fMRI), electroencephalography (EEG), or magnetoencephalography (MEG), by computing the statistical interdependency as a measure of the network edge between spatial locations.

#### Detection of the rich-club
Rich-club elements are a set of highly interconnected nodes forming a tight subnetwork within a network. The mathematical description of the rich-club phenomenon is provided by the rich-club coefficient $\phi$ as follows: $$\phi (k) = \frac{2E_{>k}}{N_{>k}(N_{>k}-1)}$$ where $k$ represents the number of connections attached to each network node (the *degree*); $N_{>k}$ represents the number of nodes whose degree is larger than a given value $k$; and $E_{>k}$ represents the number of connections of a subnetwork comprising $N_{>k}$ nodes. It should be noted that the rich-club coefficient $\phi$ is a function of the degree $k$, because it corresponds to the measure of the density of the subnetwork comprising nodes with degree greater than $k$. 

Practically, the detection procedure involves the following steps:
1) For an $N$ × $N$ network matrix where $N$ is the number of all network nodes, the degree ($k$) is computed at each node
2) For each $k$ (where 1 ≤ $k$ < $N$), all nodes with degrees less than or equal to $k$ are removed to construct a new $N_{>k}$ × $N_{>k}$ subnetwork
3) The number of existing connections and possible maximum connections of the subnetwork are denoted by $E_{>k}$ and calculated by $N_{\geq k} (N_{\geq k} −1)/2$, respectively 
4) The rich-club coefficient $\phi(k)$ is computed as the ratio of $E_{>k}$ and $N_{\geq k} (N_{\geq k}−1)/2$.


Higher degree nodes in a randomly connected network (e.g., the Erdos-Renyi network, a random network with a Poisson degree distribution) tend to have a higher probability of being interconnected to each other by chance. Therefore, to evaluate the statistical significance of $\phi (k)$, the coefficient is typically normalized to the rich-club coefficient $\phi_{random(k)}$ computed from a set of random uncorrelated networks with preserved degree distribution: $$\phi_{normalized}(k) = \frac{\phi (k)}{\langle \phi_{random}(k)\rangle}$$ where $\langle \rangle$ represents the average. If the rich-club coefficient $\phi(k)$ of a network is larger than the average rich-club coefficient across randomized networks (i.e., $\phi(k)>\langle \phi_{random}(k)\rangle$ or $\phi_{normalized}(k)>1$), the density of the subnetwork for $k$ is considered to be higher than that of its randomized networks, and the network is considered to have a rich-club architecture.

For a weighted network, the weighted rich-club coefficient $\phi^w$ is calculated using the following equation: $$\phi^w(k) = \frac{W_{>k}}{\sum^{E_{>k}}_{l=1}w_l^{rank}}$$ where $W_{>k}$ represents the sum of weights in the $N_{>k}$ × $N_{>k}$ subnetwork, $w^{rank}_l \geq w^{rank}_{l+1}$ with $1\leq l \leq E$ represents the ranked weights of the links of the network, and the coefficient $\phi^w$ should be normalized over a set of random networks.

A unifying framework for the weighted network has been proposed by Alstott and colleagues. In addition to using a network structural attribute (e.g., network degree) to compute rich-club phenomenon, Cinelli recently suggested a generalized rich-club framework using non-structural information (e.g., social or technical attributes related to network nodes). In his work, instead of using only the network degree, any structural measures distinct to degree (e.g., node centrality measures) could also be used to evaluate rich-club ordering. Furthermore, when network nodes have a certain attribute which is not directly derived from the network structure itself (i.e., node metadata such as the wealth of each person in a social network), he suggested two types of network randomization:
$$\phi^{rewiring}_{normalized}(m) = \frac{\phi (m)}{\langle \phi^{rewiring}_{random}(m)\rangle}$$
$$\phi^{reshuffling}_{normalized}(m) = \frac{\phi (m)}{\langle \phi^{reshuffling}_{random}(m)\rangle}$$
where the value $m$ corresponds to the value of the node metadata, and $\phi^{rewiring}_{random}$ and $\phi^{reshuffling}_{random}$ represent rich-club coefficients with degree-preserving rewiring and metadata reshuffling, respectively.

### Results
#### Rich-club of Caenorhabditis elegans
The rich-club studies on _C. elegans_ are valuable as they contribute to deriving fundamental hypotheses on biological network formation. For example, an important aspect of network formation revealed by studies on _C. elegans_ is the minimization of network costs (i.e., biological networks are likely to have less connections with shorter paths to minimize the spending of neural resources). However, to reduce costs in a “global” network, revised connection strategies may be more beneficial to facilitate more efficient information propagation. A selected set of network nodes (e.g., rich-club) enables the network to rewire certain connections with increased topological paths and to consequently reduce overall connection costs. Rich-club neurons in _C. elegans_ are predominantly command interneurons related to locomotion, suggesting that the existence of rich-club members in a network is crucial to optimize the most important network function (e.g., movement in the case of _C. elegans_).

#### Rich-club of mammals
This manuscript summarizes findings involving rich-clubs found in:
- Cat
- Rat and mouse
- Macaque
- Humans
		- Adults exhibit greater functional rich-club organization compared to that in the younger population
		- Preterm neonates were reported to have reduced connectivity of rich-club regions, and children with longer gestation exhibit more efficient structural networks with higher rich-club connectivity when compared to children with shorter gestation.
		- Both structural and functional brain networks exhibit rich-club organization in schizophrenia, suggesting that the effects of altered brain connectivity are more concentrated in rich-club connections than in feeder or local connections in patients with schizophrenia.
		- Rich-club connections among rich-club nodes are lower in major depressive disorder (MDD) and late-life depression patients than in healthy controls, in which higher rich-club connectivity is associated with lower symptom severity score (i.e., Hamilton Depression Rating Scale) 
		-  ADHD and ASD children exhibit distinct patterns of rich-club and non-rich-club connections


### Discussion
Rich-club analysis and whole brain anatomical network analyses are often based on neuroimaging techniques such as DTI and fiber tractography. While technological advancements in these techniques are rapidly increasing, the intrinsic nature of neuroimaging remains an open question. First, fiber tractography is a deterministic approach which often provides one-to-one connections from a seed point that may miss crossing, splitting, and/or branching tracts. Although probabilistic algorithms have been applied as an alternative to resolve this issue, other false-positive connections may be detected. This approach may not comprehensively assess rich-club detection and connections because fiber tracts related to the rich-club are relatively insensitive to false-positive and false-negative tracts. However, feeder and local connections are highly dependent on the quality of fiber tractography and may have a larger impact on peripheral associations to rich-club regions. The development of better qualified tractography algorithms is required. Second, similar to conventional graph theoretical analysis, the rich-club organization is relatively dependent on the definition of structural connectivity derived from DTI...