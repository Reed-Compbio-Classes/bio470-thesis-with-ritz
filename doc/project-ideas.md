---
title: Thesis Ideas
layout: default
nav_order: 4
---

# Thesis Project Ideas (2024-25)

This is a list of example thesis topics -- new ideas are welcome. If you want to get a broad sense of computational network biology, please read [Current and Future Directions in Network Biology](https://academic.oup.com/bioinformaticsadvances/article/4/1/vbae099/7732851). 

**You don't need to have computer science experience to do a computational thesis!** Some thesis students use this as an opportunity to learn new skills; others have taken deep dives into interpreting the results of current tools. I have also mentored expository/library theses, which synthesize big complex ideas, and meta-analyses, which collect data from multiple papers and statistically analyze the aggregate findings.

## PPI Networks and Signaling Pathways

Protein-protein interaction networks have been extremely useful for identifying and analyzing signaling pathways from experimental data. We model protein protein interactions as a graph, where nodes denote proteins and edges denote physical protein interactions. We have software to connect proteins of interest within this network in many different ways, but each method requires different interpretations of the connections. Many of these projects are inspired by the [Signaling Pathway Analysis Streamliner (SPRAS)](https://github.com/Reed-CompBio/spras/) Project, in collaboration with Tony Gitter at UW-Madison.

1. **Integrate disease data to identify signaling pathway disruption.**  We have existing algorithms to reconstruct signaling pathways.  How do we use cancer data (or other disease data) to identify dysregulated signaling?  
2. **Benchmark landmark papers with new methods/data.** A number of important papers in network biology have helped shape the field; however, we now have more complete datasets and different tools to apply to the problems. Do the findings of these landmark papers hold up in light of new information and methodologies?
3. **Investigate pathways involved in cell-cell fusion.** Cells fuse together as part of fundamental processes, yet we still don't know all of the proteins that regulate this process. This project will apply existing graph algorithms to study proteins that may regulate cell-cell fusion. (Collaboration with Derek Applewhite)
4. **Investigate regulators of manganese transport.** Maintaining a proper balance of metal ions is an extremely important cellular process. We have done some work to identify how manganese is regulated within bacterial cells through a combination of transcription factor binding motifs, network analysis, and transcriptomic analysis. Tommy Yoon '24 most recently worked on this project in the summer of 2023 and [wrote about it here](https://blogs.reed.edu/compbio/2023/10/19/finding-manganese-homeostasis-proteins/). Can we integrate these datasets to better understand potential proteins and mechanisms of regulation in *Bacillus subtillis*? (Collaboration with Shivani Ahuja).

## Adding Context to PPI Networks

We have recently done work to help researchers explore molecular networks, and provided additional information to place their questions in the context of physical and regulatory interactions. These projects are inspired by [ProteinWeaver](https://proteinweaver.reedcompbio.org/), a network visualization tool developed by post-bacs in the group. 

1. **Predict protein function from the Gene Ontology.** The Gene Ontology is a categorization of all protein function we know of; however, it is not complete. ProteinWeaver has connected the Gene Ontology to physical and regulatory interactions among proteins, and we have an initial method to predict a protein's function from this information. Can we add additional context (such as protein domain information, sequence similarity, predictd 3D structure) to improve these predictions? 
2. **Investigate the biological meaning behind network motifs.**  Motifs are small subgraphs that can be found within larger networks. We have found that [signaling pathways](https://psb.stanford.edu/psb-online/proceedings/psb22/rubel.pdf) and [disease modules](https://academic.oup.com/bioinformaticsadvances/article/3/1/vbad140/7288932) are enriched for certain subgraphs. More recently, we've categorized motifs that are comprised of both physical and regulatory interactions within ProteinWeaver. Do these enriched patterns have any biological interpretation? 
3. **Evaluate physical, regulatory, and combined interactions for protein context across taxa.** ProteinWeaver's network can be used as a PPI network, a gene regulatory network, or a combination of physical and regulatory interactions. How do these three networks affect the interpretation for a protein's relevance, and how does this change for different species?


## Graphs and Graph Generalizations
Some of these topics may be good for someone who has taken multiple CS courses.

1. **Define a mathematical objective function for signaling pathway reconstruction.** Many algorithms for signaling pathway reconstruction do not directly optimize a function of the graph; and those that do are missing a parameter to increase the size of the subnetwork. [We have developed a first attempt](https://www.liebertpub.com/doi/full/10.1089/cmb.2022.0376)  to define an objective function for signaling pathway reconstruction ([preprint](https://www.biorxiv.org/content/10.1101/2022.07.27.501737v3)), but can we improve it?
2. **Random walks on directed hypergraphs.** We have done work to develop [shortest path](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5810418/) and [connectivity algorithms](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1007384) on directed hypergraphs (where edges can capture many-to-many relationships). Random walks are useful for identifying node relevance within a graph structure; can we apply them to directed hypergraphs (where an edge captures many-to-many relationships)?  
3. **Applications for directed hypergraphs.** Directed hypergraphs have been useful for [signaling pathway representations](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4299695/), and they hold promise for other biological networks. This would be an excellent survey of potential use cases for hypergraphs and other graph generalizations for computational biology. 

## Other Types of Biological Networks

I have mentored theses on networks relevant for ecology, animal behavior, and neuroscience; I am open to talking about potential projects in these realms. We have also developed [Graphery](https://graphery.reedcompbio.org/), an interactive biological network tutorial with real-world examples across biological scales. Having an idea of the available data for thesis is especially important for these projects, which are outside my main area of expertise. 

