<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")


github to submit to: [https://github.com/Zhong-Lab-UCSD/BENG183_2023Fall_Applied-Genomic-Technologies](https://github.com/Zhong-Lab-UCSD/BENG183_2023Fall_Applied-Genomic-Technologies) 

example format: [https://zhonglab.gitbook.io/3dgenome/chapter1-why-we-care-about-3d-genome/3d-nuclear-structure](https://zhonglab.gitbook.io/3dgenome/chapter1-why-we-care-about-3d-genome/3d-nuclear-structure) 




## Hi-C Technology and Application

Group 27: Jessica Yu, Cici Bu, Lorenzo Olmo Marchal



1. 3D Genome
    1. Genome Folding
    2. TAD
2. Hi-C Process
    3. Background
    4. Step-by-Step Process
3. Hi-C Output Analysis
    5. Main Steps
    6. Specific technology: Hi-C pro
4. Hi-C Application in Tracing Cancer Evolution 
    7. Case Study
        1. Patient 1: Primary Melamoma v.s. Subsequent metastasis
        2. Patient 2: Melanoma 1 v.s. Melanoma 2 v.s. Subsequent metastasis
    8. Future Directions
5. Sources Used


### I. 3D Genome

**Genome Folding **



<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image2.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image2.png "image_tooltip")


If the human genome were to be measured it would be around 2 meters long due to its size of 3 billion nucleotides but somehow it fits into a nucleus that is 5-10 μm in diameter. DNA is immensely folded inside this small pocket, resulting in the formation of complex 3D structures as well as facilitating essential biological processes such as replication, transcription, and gene expression. This is known as the **3D genome **and the study of the chromatin organization in the nucleus sheds light on the spatial aspects of gene regulation and genome stability.[^1]

**TAD (Topologically Associating Domains) **

	An example of a 3D genome structure are TADs which are regions of around 15 million base pairs that contribute to the regulation of gene expression by restricting interaction between cis-regulatory sequences and their target. TADs create somewhat insulated domains of genomic material. 



<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image3.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image3.png "image_tooltip")


Some of the components TAD boundaries are enriched for are:[^2]** ** 



* insulator proteins: CTCF 
* H3K4me3 and H3K36me3
* housekeeping genes
* repeat elements


### II. Hi-C Process 

**Background**

	Hi-C is a form of chromosome conformation capture (3C) used to obtain and examine genome-wide data. Hi-C explores the complexities of how the genome is stored and what it means for the function of the genetic information. Hi-C and related methods are still being refined and applied to explore the complexities of the 3D human genome. 

What information can Hi-C provide: 



* Chromatin conformation: loops and long range interactions
* Topological domains
* Nuclear architecture: reveals spatial arrangement
* Comparative genomics: compare data across different cell types and tissues 

**Hi-C Step-by-Step Process**



<p id="gdcalert4" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image4.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert5">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image4.png "image_tooltip")




1. Cells are cross-linked with formaldehyde which results in covalent links between spatially adjacent chromatin segments (DNA fragments shown in dark blue and red)
2. DNA is digested with a restriction enzyme (HindIII) that leaves a 5’ overhang (as seen in the blue)
3. The 5’ overhangs are filled with nucleotides and marked with biotin (purple dots)
4. The resulting fragments are ligated under dilute conditions and now the DNA sample contains ligation products marked with biotin at the junction.
5. A Hi-C library is created by shearing the DNA and purifying the sample so only the biotin-containing fragments remain.
6. The library is analyzed by using parallel DNA sequencing, producing a catalog of interacting fragments.[^3]

### **III. Hi-C Output Analysis **

**A. Overview**

There are 4 general key steps when it comes to the analysis of Hi-C outputs:



1. Alignment
2. Duplicate Removal
3. Creation of Contact Matrix and Contact Map
4. Feature Annotation

**Alignment**

As mentioned previously, the last step when obtaining Hi-C analysis data is to sequence the sheared DNA using paired-ends. After obtaining these short-sequence reads, we need to align them in order to map our Hi-C sequence library to known sequences within the genome. Without aligning and mapping the sequences to known genome locations, we would not be able 

to obtain the necessary context to understand the spatial organization of the genome and the interactions within it. [^4]

**Duplicate Removal**

As part of our preprocessing steps , it is essential to remove any duplicate sequences that were found during alignment and other quality checks. An important part of Hi-C data analysis is its usage of different statistical methods (such as PCA and log transformations) in order to create a contact map and matrix of the different chromatin interactions and topological structures within the genome. However, having a high number of reads can lead to skewing of statistics and biased results. <sup>4</sup>

**Creation of Contact Matrix and Map**

Within the context of Hi-C data, a contact matrix is a n by n dimensional representation of oh our outputs, representing the interaction frequency (IF) within a specific chromosome or with other chromosomes. These fragments are obtained from our sequencing and alignment, with a defined bp length. 

A contact matrix represents the number of fragments (rows) that have been found tied to a specific loci in a chromosome or chromosome in the genome (columns). Each entry within the matrix consists of the representation of count read pairs from two interacting chromatin regions found in the Hi-C experiment. To obtain this matrix several different statistical analyses and transformations are applied. Some of the most popular statistical techniques are Principal Component Analysis (PCA), log transformation, count scaling, eigenspace analysis, and poisson regressions. [^5]



<p id="gdcalert5" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image5.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert6">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image5.png "image_tooltip")


Much of the analysis that is done on Hi-C data focuses on:


     \
1. Finding significance of interactions occurring through distributions and contact-based methods (e.g Poisson distribution, eigenspace analysis).


    2. Finding probabilities for said interactions.


    3. Reducing the dimensionality of our data, in order to better interpret it.

One way to better visualize the contact matrix is to then create a contact map, which displays the different topological structures and chromatin interactions found. <sup>5</sup>

**Feature Annotation**

In this step of the Hi-C output analysis we annotate the actual topological features that were found within the contact map, whose visual representation makes it easy to analyze. [^6]



Overall, for the two different topological structures that we have been discussing, TADs and loops, they are incredibly recognizable in contact maps due the formations that they naturally form within these maps. <sup>6</sup>

TADs                                                                         Loops    



<p id="gdcalert6" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image6.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert7">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image6.png "image_tooltip")




<p id="gdcalert7" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline drawings not supported directly from Docs. You may want to copy the inline drawing to a standalone drawing and export by reference. See <a href="https://github.com/evbacher/gd2md-html/wiki/Google-Drawings-by-reference">Google Drawings by reference</a> for details. The img URL below is a placeholder. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert8">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![drawing](https://docs.google.com/drawings/d/12345/export/png)

**B. Technologies for HI-C analysis: Hi-C pro **



<p id="gdcalert8" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image7.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert9">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image7.png "image_tooltip")


There are many different available libraries and packages available for the Hi-C output analysis pipeline, however out of all of them HiC-pro is one of the most recently made technologies, and one that encapsulates the most features. 

Overall, HiC-pro is a set of flexible bioinformatics tools that was created to allow bioinformatics researchers to have a hub of Hi-C analysis tools at their disposal. 

**IV. Hi-C Application in Tracing Cancer Evolution **

“Cancer progression is driven by ongoing selection for mutations” and the endless duplication of certain genes due to mutations. To better study cancer, it is extremely important for us to know the mechanisms behind it and to identify the mutation site, the progression of the mutation along cancer development, and the genes and chromosomes correlated with the mutation. Hi-C is proven to be one of the most useful tools to study cancer development and trace the development of mutation as cancer cells progress. 

To better understand and visualize it, let’s take a look at 2 examples from 2 patients:



1. **Patient 1**



<p id="gdcalert9" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image8.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert10">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image8.png "image_tooltip")



    Patient 1 has been diagnosed with Melanoma for several years. Scientists took samples from the patient’s primary melanoma cells and their metastasis cells progressed several years after the primary melanoma cells, and ran them under Hi-C.


    The left Hi-C map in graph (a) is generated from the primary melanoma cells. From the squares that are zoomed in, we can see dense and concentrated blue dots with a loop identified between chromosome 2 and chromosome 10, scattered dense blue dots with a loop identified between chromosomes 5 and 10, no loop identified between chromosomes 11 and 17, and a short loop identified between chromosome 1 and chromosome 13. 


    The right Hi-C map in graph (a) is generated from the metastasis cells. From the squares that are zoomed in, compared with what we saw from the primary melanoma cell, we can see that the loop between chromosomes 2 and 10 becomes lighter with the blue dots becoming more sparse, the loop between chromosomes 5 and 10 increased its range, loops are generated between chromosomes 7 and 11, and the loop between 1 and 13 increased in range and decreased in intensity.  


    From the comparison between the Hi-C maps, we can identify several sites of obvious loop change between the melanoma cells and the metastasis cells, which clearly tells us how the primary cancer cells mutated and progressed to the new cells that may generate new abilities to move to the other part of the patient’s body. 



2. **Patient 2 **

    

<p id="gdcalert10" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image9.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert11">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image9.png "image_tooltip")



From the 2 examples we studied above, we can see that Hi-C plays an important role in providing an overview map of chromosome interactions within the entire cell, which helps us to identify the differentiation and overall mutation development from a bird view perspective.  

**Future Directions**

**V. Sources Used**



1. ..
2. ..
3. ..
4. Erdmann-Pham, D.D., Batra, S.S., Turkalo, T.K. _et al._ Tracing cancer evolution and heterogeneity using Hi-C. _Nat Commun_ 14, 7111 (2023). [https://doi.org/10.1038/s41467-023-42651-2](https://doi.org/10.1038/s41467-023-42651-2)
5. Liu, N., Low, W.Y., Alinejad-Rokny, H. _et al._ Seeing the forest through the trees: prioritising potentially functional interactions from Hi-C. _Epigenetics & Chromatin_ 14, 41 (2021). [https://doi.org/10.1186/s13072-021-00417-4](https://doi.org/10.1186/s13072-021-00417-4)

<!-- Footnotes themselves at the bottom. -->
## Notes

[^1]:
     Hi-C: A comprehensive technique to capture the conformation of genomes [https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3874846/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3874846/) 

[^2]:
     3dgenome [https://zhonglab.gitbook.io/3dgenome/chapter1-why-we-care-about-3d-genome/3d-nuclear-structure](https://zhonglab.gitbook.io/3dgenome/chapter1-why-we-care-about-3d-genome/3d-nuclear-structure) 

[^3]:

     Lecture 8 Genome interaction Hi-C - Zhong

[^4]:
    <sup> Pal, K., Forcato, M. & Ferrari, F. Hi-C analysis: from data generation to integration. <em>Biophys Rev</em> <strong>11</strong>, 67–78 (2019). https://doi.org/10.1007/s12551-018-0489-1</sup>

[^5]:
     Oluwadare, O., Highsmith, M. & Cheng, J. An Overview of Methods for Reconstructing 3-D Chromosome and Genome Structures from Hi-C Data. Biol Proced Online 21, 7 (2019). https://doi.org/10.1186/s12575-019-0094-0

[^6]:
     Durand NC, Shamim MS, Machol I, Rao SS, Huntley MH, Lander ES, Aiden EL. Juicer Provides a One-Click System for Analyzing Loop-Resolution Hi-C Experiments. Cell Syst. 2016 Jul;3(1):95-8. doi: 10.1016/j.cels.2016.07.002. PMID: 27467249; PMCID: PMC5846465.
