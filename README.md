<h1 align="center">Dorado-basecalled reads improve old bacterial genome assembly</h1>


<h3 align="center">M. Asaduzzaman Prodhan</h3>


<div align="center"><b> DPIRD Diagnostics and Laboratory Services </b></div>


<div align="center"><b> Department of Primary Industries and Regional Development </b></div>


<div align="center"><b> 3 Baron-Hay Court, South Perth, WA  6151, Australia </b></div>


<div align="center"><b> Correspondence: Asad.Prodhan@dpird.wa.gov.au </b></div>
 

<br />


<br />



## **Abstract**


Oxford Nanopore Technology (ONT) sequencing platforms produce electric signals called squiggles as raw data. These squiggles are converted into nucleotide sequences by an algorithm called basecaller. ONT has recently released a new basecaller, Dorado; which is expected to improve basecalled read quality. Here, I re-basecalled an old set of Nanopore squiggles and reconstructed the corresponding bacterial genomes. Results revealed that the Dorado-basecalled reads improved the previously assembled bacterial genomes that used previous ONT basecaller, Guppy. An improved bacterial genome assembly is crucial for a more complete and accurate representation of a bacterium. In turn, this improves accuracy in the downstream applications such as diagnosis, gene annotation, structural variation detection, understanding virulence factors or antibiotic resistance mechanisms. 


<br />


## **Methods**


The squiggles from an old Nanopore sequencing run (Kit: SQK LSK 109 and Flowcell: R9.4.1) were basecalled using Guppy[^Guppy] (version 6.0.1+652ffd179, High Accuracy mode) and Dorado[^Dorado] (version 0.6.2+14a7067, Super Accuracy mode). The basecalled reads were subjected to quality-control (QC) analysis using FastQC[^FastQC] followed by genome assembly using Flye[^Flye] (version 2.9). The assembled genomes were then quality-checked by QUAST[^QUAST] (v5.2.0) and visualised by Bandage[^Bandage] (version 0.8.1).


<br />


## **Results and Discussion**

The read QC stats showed that Dorado produced about 2000 more total sequences in all three samples compared to those from Guppy (Table 1). In contrast, Guppy produced about 300 Mbp more total bases compared to those from Dorado. None of the reads from either of the basecallers was flagged by FastQC as of poor quality. Dorado generated longest reads compared to Guppy while the GC percentages were similar between the basecallers (Table 1). However, per base sequence quality was greatly improved in the Dorado-basecalled reads (Fig. 1). Dorado-basecalled reads produced a complete circular genome for Barcode07 and closed the gap for Barcode08 (Fig. 2) comparing between the basecallers. Barcode12 genome assembly remained independent of the basecallers (Fig. 2). All the genome quality statistics were similar between Guppy and Dorado (Table 2). 


<br />


<h3 align="center">Table 1: Read quality statistics</h2>


<br />


<p align="center">
  <img 
    src="https://github.com/asadprodhan/Dorado-basecalled-reads-improve-old-bacterial-genome-assembly-/blob/main/Table_1_Read_QC.PNG"
 align="center" width=70% height=70% >   
</p>
<p align = center>

</p>

<br />


<br />


<h3 align="center">Per base sequence quality</h2>


<br />


<p align="center">
  <img 
    src="https://github.com/asadprodhan/Dorado-basecalled-reads-improve-old-bacterial-genome-assembly-/blob/main/Figure_1_Per_base_sequence_quality.png"
 align="center" width=70% height=70% >   
</p>
<p align = center>
Figure 1: Per base sequence quality.
</p>

<br />


<br />


<h3 align="center">Genome assembly graphs</h2>


<br />


<p align="center">
  <img 
    src="https://github.com/asadprodhan/Dorado-basecalled-reads-improve-old-bacterial-genome-assembly-/blob/main/DPI300_Figure_2_Genome_assembly_graphs.png"
 align="center" width=70% height=70% >   
</p>
<p align = center>
Figure 2: Genome assembly graphs.
</p>

<br />


<br />


<h3 align="center">Table 2: Genome quality statistics</h2>


<br />


<p align="center">
  <img 
    src="https://github.com/asadprodhan/Dorado-basecalled-reads-improve-old-bacterial-genome-assembly-/blob/main/Table_2_Genome_QC.PNG"
 align="center" width=70% height=70% >   
</p>
<p align = center>

</p>


<br />



<br />



Taken together, these findings suggest that the choice of basecaller is important for the ONT raw data, and it is worth collecting and storing the squiggles from the ONT sequencing runs to be re-basecalled later with an improved version of basecallers, thus improving genome assemblies and their associated applications.       


<br />


**Funding:** There was no specific funding for this study.


<br />


**Conflict of interest:** Author declares there is no conflict of intertest.


<br />


**Data availability:** The study was conducted on in-house unpublished data, which are currently not publicly available.


<br />


## **References**



[^Guppy]:	Guppy basecalling software. Oxford Nanopore Technologies. https://community.nanoporetech.com/protocols/Guppy-protocol/v/gpb_2003_v1_revax_14dec2018.


[^Dorado]: Dorado. Oxford Nanopore’s Basecaller. https://github.com/nanoporetech/dorado (2024).


[^FastQC]: Andrews, S. FastQC: A quality control tool for high throughput sequence data. https://www.bioinformatics.babraham.ac.uk/projects/fastqc/ (2010).


[^Flye]: Kolmogorov, M., Yuan, J., Lin, Y. & Pevzner, P. A. Assembly of long, error-prone reads using repeat graphs. Nat. Biotechnol. 37, 540–546 (2019).


[^QUAST]: Mikheenko, A., Prjibelski, A., Saveliev, V., Antipov, D. & Gurevich, A. Versatile genome assembly evaluation with QUAST-LG. Bioinformatics 34, i142–i150 (2018).


[^Bandage]: Wick, R. R., Schultz, M. B., Zobel, J. & Holt, K. E. Bandage: interactive visualization of de novo genome assemblies. Bioinformatics 31, 3350–3352 (2015).

