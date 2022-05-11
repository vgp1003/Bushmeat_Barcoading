# Bushmeat Barcoading

## Introduction

   Bushmeat is meat from wildlife species hunted for human consumption. It is common in tropical areas of South America, Central Africa, and Asia (Fig. 1)[1]. Bushmeat is a critical nutritional and economic resource, however over exploitation has lead to sharp declines in the populations of many endangered reptile and mammal species. The international bushmeat trade is estimated to be worth over $60 billion/year. $15 billion of this revenue is estimated to be generated illegally [2]. This caould include sale of illegal species, underground markets, or products that have crossed borders illegaly. International laws and conventions protect endangered wildlife from bushmeat hunting, but these regulations depends on the ability to reliably identify morphologically ambiguous animal products. 
                                                                
![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Map.PNG "Map.PNG") 

   COX1 is a highly conserved mitochondiral gene that encodes a protein essential to respiration. It is an established standard for DNA barcoding with relialble applications for species identification. Thus, COX1 has promising potential as a bushmeat barcoding tool [3]. My project is based off a 2010 study by Eaton et al. [2] that collected tissue samples from different commonoly hunted mammal and reptile species (Fig. 2) in various South American and Central African locations. The study sequenced the COX1 gene from all their samples and built three phylogenetic trees to identify the different crocodile, alligator, and deer species based on this DNA barcode. Since this study was published in 2010, a wealth of new bioinformatic data and has become publicly availible. This includes COX1 refrence sequences for the majority of the species studied in the paper. 
   
![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Croc.PNG "Croc.PNG")
   
   The goal of this project was to 1) use the COX1 sequences that Eaton et _al._ depostied on NCBI to recreate their crocodile, alligator and deer phylogenetic trees using different RAxML versions for comparison. Then 2) add refrence COX1 genes from each species that had them availible on NCBI to see where they fall on the tree. Because Eaton et al. achieved high confidence for their species identifications, it was hypothesized that the NCBI refrence COX1 genes would fall closely within the expected species on the trees. 

## Methods

1) Downloaded FASTAs for Eaton et al.'s 173 COX1 gene sequences from NCBI along with NCBI refrence COX1 genes for the various species in the paper.

2) Alignment and phylogenetic reconstructions were performed using the function "build" of ETE3 v3.1.1 CLUSTALW as implemented on the GenomeNet (https://www.genome.jp/tools/ete/). CLUSTALW was selected for consistancy with Eaton et al.'s alignment procedure. Alignment files were then visualized with Jalview (Fig. 3,4,5). 

3) ML trees were inferred using RAxML v8.1.20 ran with model GTRGAMMA and default parameters. Branch supports were computed out of 100 bootstrapped trees. This was different from Eaton et al. whose ML trees were inferred using RAxML 7.0.4 ran with model GTRGAMMA and node support out of 100 rapid bootstrap replicates.

## Results/Discussion

**Crocodiles**

![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Crocodiles_Alignment_vis.PNG "Crocodiles_Alignment_vis.PNG")
Figure 3. CLUSTALW alignment snapshot for Eaton et al. and NCBI reference crocodile COX1 genes. Visualized with Jalview.


![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Crocodile_trees.png "Crocodile_trees.png")

- A.mississippiens, and aligator species whose habitat spans the southern states of the USA, was used as the outgroup.
- The reconstructed tree (Fig. 4A) showed the same species relationships as the tree made by Eaton et al. (Fig. 4B) with upsidedown orientation. (The sequence for 1USFWS in Fig. 4B, a crocodile skin handbag of unknown origins which Eaton et al. determined to be C. nilotictus, was not depsited on NCBI and therefore was not included in Fig. 4A. 
- All the NCBI reference COX1 sequences fell closely within the same clade as their expected species except for the M. cataphractus.
- This sequence branched of before the Eaton et al. _M. cataphractus_ sequences at a node with a relatively low boostrap value of 0.048.

Discrepancy in _M. cataphractus_ placement could be due to differences in the RAxML versions used to build the tree (Eaton et al. used RAxML 7.0.4. while this study used RAxML v8.1.20 from the online CLUSTALW tool. Discrepancies could also be due to species sampling location. Eaton et _al._ only collected samples from Gabon and Congo while the natural habitat of _M. cataphractus_ spans from Senegal to the Democratic Republic of the Congo. This means that the NCBI refrence could have potentially been built from a much wider geographical range than the sequences collected in the paper. It is also important to note that there is a large temporal gap between the collecton of the specimines in the paper and the publishing of the _M. cataphractus_ reference COX1 sequence. The majority of the Eaton et _al_. samples were collected before 1990 while the NCBI refrence was published in 2021, thus it is possible that this rougly 30 year gap could also contribute to the _M. cataphractus_ discrepancy.  

**Aligators**

![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Alligator_alignment_vis.PNG "Alligator_alignment_vis.PNG")
Figure 5. CLUSTALW alignment snapshot for Eaton et al. and NCBI reference alligator COX1 genes. Visualized with Jalview.


![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Alligator_trees.png "Alligator_trees.png")

**Deer**

![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Deer_Alignment_vis.PNG "Deer_Alignment_vis.PNG")
Figure 7. CLUSTALW alignment snapshot for Eaton et al. and NCBI reference deer COX1 genes. Visualized with Jalview.

![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Deer_trees.png "Deer_trees.png")

## References

[1] Ripple WJ, Abernethy K, Betts MG, Chapron G, Dirzo R, Galetti M, Levi T, Lindsey PA, Macdonald DW, Machovina B, Newsome TM, Peres CA, Wallach AD, Wolf C, Young H. Bushmeat hunting and extinction risk to the world's mammals. R Soc Open Sci. 2016 Oct 19;3(10):160498. doi: 10.1098/rsos.160498. PMID: 27853564; PMCID: PMC5098989.

[2] Eaton, M.J., Meyers, G.L., Kolokotronis, SO. et al. Barcoding bushmeat: molecular identification of Central African and South American harvested vertebrates. Conserv Genet 11, 1389–1404 (2010). https://doi.org/10.1007/s10592-009-9967-0

[3] New Zealand Ministry of Education. (2009). The ideal barcoding gene. Science Learning Hub. Retrieved May 10, 2022, from https://www.sciencelearn.org.nz/resources/1937-the-ideal-barcoding-gene 
