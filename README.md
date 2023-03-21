## A Chemoinformatic Analysis on Natural Glycosides with Respect to Biological Origin and Structural Class

In the current study, we provide a highlight on the occurrence of nature glycosides, especially the varied distribution in different biological sources and structural types of glycosides. The results are obtained by chemoinformatic analysis of the Dictionary of Natural Products, which contains 264,071 records (CRC Press, v25.1). These findings could help us to interpret the preference of NPs’ glycosylation and to investigate how NP glycosylation could aid NP-based drug discovery.

### >>>Data Source:
The Dictionary of Natural Products (CRC Press, v25.1)

<h4>Of particular note, the original dataset (DNP) used in this study is distributed commercially and we cannot share it online. Processed data are available to the academic community upon request.</h4>

### >>>Software Versions:
① Python (Version 3.7.0) <br>
② RDKit (Version 2020.09.1.0) <br> 
③ Pipeline Pilot (Version 2016) <br>

### >>>Codes:
<h4> 1 Data Preprocessing </h4>

- Extraction and standardization of natural products in DNP database. 

<h4> 2 Biological Source and Structural Type </h4>

- Distribution of natural products from different biological sources or structure types.

<h4> 3 Removing Sugar </h4>

- The deglycosylation results of two different deglycosylated methods (removing only terminal sugars and removing all sugars) of SRU.<br>
The parameters were set as follows: 
```
Removing All Sugars
java -jar "SugarRemovalUtility-jar-with-dependencies.jar" -i "filename" -t "3" -remTerm "false" -presMode "1" -oxyAtomsThres "0.4"

Removing Terminal Sugars:
java -jar "SugarRemovalUtility-jar-with-dependencies.jar" -i "filename" -t "3" -remTerm "true" -presMode "1" -oxyAtomsThres "0.4"
```

-t "3": Circular and linear sugar moieties should be removed. <br>
-remTerm "false": Terminal and Non-terminal sugar moieties should be removed. <br>
(-remTerm "true": Only terminal sugar moieties should be removed.) <br>
-presMode "1": Remove disconnected structures that do not have enough heavy atoms (default 5 heavy atoms). <br>
-oxyAtomsThres "0.4": The minimum ratio of the exocyclic oxygen atoms of a circular sugar to the atoms in the sugar ring was set to 0.4. <br>

<h4> 4 Natural Glycosides Analysis </h4>

- Terminal and non-terminal sugar <br>
- Glycosidic bond types <br>
- Circular and linear sugar <br>
- Glycosyl substitution types <br>

<h4> 5 Biological Source and Glycosylation </h4>

- Glycosylation ratios and natural glycoside distribution in different biological sources.

<h4> 6 Structural Type and Glycosylation </h4>

- Glycosylation ratios and natural glycoside distribution in different structural types.

<h4> 7 Physicochemical Properties </h4>

- The physicochemical properties of glycosides, aglycones and non-glycosides.

<h4> 8 Murcko Scaffold Analysis </h4>

 - The murcko scaffolds of natural products with biological source.
 - The unique murcko scaffolds of aglycones and non-glycosides.
 - The glycosylation ratio of each murcko scaffold.
