# Bushmeat Barcoading

## Introduction

   Bushmeat is meat from wildlife species hunted for human consumption. It is common in tropical areas of South America, Central Africa, and Asia (Fig. 1)[1]. Bushmeat is a critical nutritional and economic resource, however over exploitation has led to sharp declines in the populations of many endangered reptile and mammal species. The international bushmeat trade is estimated to be worth over $60 billion/year. $15 billion of this revenue is estimated to be generated illegally [2]. This could include sale of illegal species, underground markets, or products that have crossed borders illegally. International laws and conventions protect endangered wildlife from bushmeat hunting, but these regulations depend on the ability to reliably identify morphologically ambiguous animal products. 
                                                                
![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Map.PNG "Map.PNG") 

   COX1 is a highly conserved mitochondrial gene that encodes a protein essential to respiration. It is an established standard for DNA barcoding with reliable applications for species identification. Thus, COX1 has promising potential as a bushmeat barcoding tool [3]. My project is based off a 2010 study by Eaton et al. [2] that collected tissue samples from different commonly hunted mammal and reptile species (Fig. 2) in various South American and Central African locations. The study sequenced the COX1 gene from all their samples and built three phylogenetic trees to identify the different crocodile, alligator, and duiker species based on this DNA barcode. Since this study was published in 2010, a wealth of new bioinformatic data and has become publicly available. This includes COX1 reference sequences for the majority of the species studied in the paper. 
   
![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Croc.PNG "Croc.PNG")
   
   The goal of this project was to 1) use the COX1 sequences that Eaton et _al._ deposited on NCBI to recreate their crocodile, alligator and duiker phylogenetic trees using different RAxML versions for comparison. Then 2) add reference COX1 genes from each species that had them available on NCBI to see where they fall on the tree. Because Eaton et _al._ achieved high confidence for their species identifications, it was hypothesized that the NCBI reference COX1 genes would fall closely within the expected species on the trees. 

## Methods

1) Downloaded FASTAs for Eaton et _al._'s 2010 173 COX1 gene sequences from NCBI along with 12 NCBI reference COX1 genes for the various species in the paper's phylograms.

2) Alignment and phylogenetic reconstructions were performed on a laptop using the function "build" of ETE3 v3.1.1 CLUSTALW as implemented on the GenomeNet (https://www.genome.jp/tools/ete/). CLUSTALW was selected for consistency with Eaton et _al._'s alignment procedure. To visualize the alignment files the Jalview application was installed on the laptop (Fig. 3,5,7). 

3) ML trees were inferred using RAxML v8.1.20 ran with model GTRGAMMA and default parameters. Branch supports were computed out of 100 bootstrapped trees. This was different from Eaton et _al._ whose ML trees were inferred using RAxML 7.0.4 ran with model GTRGAMMA and node support out of 100 rapid bootstrap replicates.

## Findings

**Central African Crocodiles**

![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Crocodiles_Alignment_vis.PNG "Crocodiles_Alignment_vis.PNG")
Figure 3. CLUSTALW alignment snapshot for Eaton et al. and NCBI reference crocodile COX1 genes. Visualized with Jalview.


![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Crocodile_trees.png "Crocodile_trees.png")

- _A. mississippienis_, and alligator species whose habitat spans the southern states of the USA, was used as the outgroup.
- The reconstructed tree (Fig. 4A) showed the same species relationships as the tree made by Eaton et al. (Fig. 4B) with upside down orientation. (The sequence for 1USFWS in Fig. 4B, a crocodile skin handbag of unknown origins which Eaton et al. determined to be C. nilotictus, was not deposited on NCBI and therefore was not included in Fig. 4A. 
- All the NCBI reference COX1 sequences fell closely within the same clade as their expected species except for _M. cataphractus_ (purple).
- This sequence branched of before the Eaton et al. _M. cataphractus_ sequences at a node with a relatively low bootstrap value of 0.048.
- The paper collected the majority of their _C. niloticus_ samples from Gabon. However, the one _C. nilotictus_ sample that was collected from the Congo ( _C. nilotictus_ (Congo)) was significantly different from the Gabon samples. Interestingly, the two types of _C. nilotictus_ specimens fell similarly on the reconstructed tree, and the NCBI _C. nilotictus_ COX1 reference sequence fell closer to the Gabon samples. 

Overall, the species relationships on the reconstructed tree fell similarly to the Eaton et _al._ tree. It is important to note that the reference COX1 genes (roughly 1,590 bp) were on average longer than the Eaton et al. sequences (roughly 645 bp). This could have skewed the branch lengths on the reconstructed trees to be different than the Eaton et _al._ trees. Discrepancy in the reference  _M. cataphractus_ COX1 gene placement could be due to differences in the RAxML versions used to build the tree (Eaton et al. used RAxML 7.0.4. while this study used RAxML v8.1.20 from the online CLUSTALW tool. Discrepancies could also be due to species sampling location. Eaton et _al._ only collected samples from Gabon and Congo while the natural habitat of _M. cataphractus_ spans from Senegal to the Democratic Republic of the Congo. This means that the NCBI reference could have potentially been built from a much wider geographical range than the sequences collected in the paper. It is also important to note that there is a large temporal gap between the collection of the specimens in the paper and the publishing of the _M. cataphractus_ reference COX1 sequence. The majority of the Eaton et _al_. samples were collected before 1990 while the NCBI reference was published in 2021, thus it is possible that this roughly 30-year gap could also contribute to the _M. cataphractus_ discrepancy. 

**South American Alligators**

![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Alligator_alignment_vis.PNG "Alligator_alignment_vis.PNG")
Figure 5. CLUSTALW alignment snapshot for Eaton et al. and NCBI reference alligator COX1 genes. Visualized with Jalview.


![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Alligator_trees.png "Alligator_trees.png")

- Similarly to the crocodile tree, _A. mississippiens_, was used as the outgroup.
- The paper reported that one alligator sample (_M. niger25_) that was previously thought to be from _M. niger_, was actually a misidentified _C. yacare_ sample. The reconstructed tree was in concurrence with this identification.
- Unlike the crocodile tree, there was a fundamental relationship difference between the reconstructed (Fig. 6A) and Eaton et _al._ (Fig. 6B) phylograms for the alligators.
-  While the reconstructed tree placed the P. _trigonatus_/_P. palpebrosus_ (yellow/purple)  closer to the _C. yacare_/_C.c. chiapasius_ group (pink/dark green), the Eaton et _al._ tree placed the _P. trigonatus_/ _P. palpebrosus_ group more closely related to _M. niger_/_C. latirostris_ group (orange/blue). 
-  Only two of the alligator species in the tree have NCBI reference COX1 genes available (_P. trigonatus_ and _P. palpebrossus_) (yellow and purple respectively). Both NCBI references fell closely within the expected species with bootstrap values of 100.

The Eaton et _al._ tree did not include a bootstrapping value for the node where their _P. trigonatus_/ _P. palpebrosus_ grouping diverged from the rest of the species (circled in red), however the reconstructed tree has a bootstrapping value of 100 at this same position where the trees differ. Interestingly, the bootstrap value that corresponds to the split between the _C. yacare_/_C.c. chiapasius_ group and the  _M. niger_/_C. latirostris_ group on the Eaton et _al._ tree is relatively low (80). This structural difference between the two trees could be due to the different versions of RAxML used. 

**Central African Duikers**

![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Deer_Alignment_vis.PNG "Deer_Alignment_vis.PNG")
Figure 7. CLUSTALW alignment snapshot for Eaton et al. and NCBI reference deer COX1 genes. Visualized with Jalview.

![alt text](https://github.com/vgp1003/Bushmeat_Barcoading/blob/main/Figures/Deer_trees.png "Deer_trees.png")

- _T. eurycerus_, a species of bongo native to Central Africa was used as the outgroup. 
- Eaton et _al._ did not deposit their unidentified sample sequences (Uniden11, Uniden10, and Uniden 15) to NCBI, thus, they were not included on the reconstructed  tree (Fig. 8A). 
- The paper reported that one duiker sample (_C.callpygus_ YF42) that was previously thought to be from _C.callpygus_, was actually a misidentified _C. dorsalis_ sample. The reconstructed tree was in concurrence with this identification.
- There were multiple fundamental relationship differences between the reconstructed and Eaton et _al._ (Fig. 8B) phylograms for the duikers.
- While the Eaton et _al._ tree split the _C. leucogaster_ (green) samples into two distantly related branches, the reconstructed tree did not.
- The reconstructed tree showed some of the _C. leucogaster_ samples to be closely related to _C. nigifirons_ (purple) in a clade that was not present on the Eaton et _al._ tree. The _C. nigifrons_ sequences on the Eaton et al. tree were more closely related to _C. dorsalis_ (yellow) than _C. leucogaster_.
- The reconstructed tree also showed the _C. dorsalis_ sequences so branch off from the rest of the species very early on, with a bootstrapping value of 100 at the diverging node. This was not the case for the Eaton et al. tree where _C. dorsalis_ branched off from _C. callpygus/C.monticola_ (orange/blue) much later.
- There were NCBI reference COX1 sequences for all duiker species on the tree except for _C. monticola_. All NCBI reference COX1 genes fell closely within the expected species of the reconstructed tree.  

These structural differences between the  reconstructed and Eaton et _al._ trees are again could be attributed to the different RAxML versions used to infer the phylograms. It is also possible that the omission of the three unidentified samaples could have changed some of the species relationships on the reconstructed tree. Interestingly, there is no bootstrap value for the node where the two _C. leucogaster_ groupings diverge on the Eaton et _al._ tree. There is no in depth discussion in the paper about why the species is split in two on the phylogram, but it is an unusual finding that may have effected the placement of other species relationships on their tree. 

## References

[1] Ripple WJ, Abernethy K, Betts MG, Chapron G, Dirzo R, Galetti M, Levi T, Lindsey PA, Macdonald DW, Machovina B, Newsome TM, Peres CA, Wallach AD, Wolf C, Young H. Bushmeat hunting and extinction risk to the world's mammals. R Soc Open Sci. 2016 Oct 19;3(10):160498. doi: 10.1098/rsos.160498. PMID: 27853564; PMCID: PMC5098989.

[2] Eaton, M.J., Meyers, G.L., Kolokotronis, SO. et al. Barcoding bushmeat: molecular identification of Central African and South American harvested vertebrates. Conserv Genet 11, 1389–1404 (2010). https://doi.org/10.1007/s10592-009-9967-0

[3] New Zealand Ministry of Education. (2009). The ideal barcoding gene. Science Learning Hub. Retrieved May 10, 2022, from https://www.sciencelearn.org.nz/resources/1937-the-ideal-barcoding-gene 
