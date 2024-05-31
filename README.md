# **Dorado-basecalled reads improve old bacterial genome assembly**


### **M. Asaduzzaman Prodhan**


DPIRD Diagnostics and Laboratory Services, Department of Primary Industries and Regional Development; 3 Baron-Hay Court, South Perth, WA  6151, Australia. 

Correspondence: Asad.Prodhan@dpird.wa.gov.au



## **Abstract**


Oxford Nanopore Technology (ONT) sequencing platforms produce electric signals called squiggles as raw data. These squiggles are converted into nucleotide sequences by an algorithm called basecaller. ONT has recently released a new basecaller, Dorado; which is expected to improve basecalled read quality. Here, I re-basecalled an old set of Nanopore squiggles and reconstructed the corresponding bacterial genomes. Results revealed that the Dorado-basecalled reads improved the previously assembled bacterial genomes that used previous ONT basecaller, Guppy. An improved bacterial genome assembly is crucial for a more complete and accurate representation of a bacterium. In turn, this improves accuracy in the downstream applications such as diagnosis, gene annotation, structural variation detection, understanding virulence factors or antibiotic resistance mechanisms. 


## **Methods**


The squiggles from an old Nanopore sequencing run (Kit: SQK LSK 109 and Flowcell: R9.4.1) were basecalled using Guppy1(version 6.0.1+652ffd179, High Accuracy mode) and Dorado2 (version 0.6.2+14a7067, Super Accuracy mode). The basecalled reads were subjected to quality-control (QC) analysis using FastQC3 followed by genome assembly using Flye (version 2.9)4. The assembled genomes were then quality-checked by QUAST (v5.2.0)5 and visualised by Bandage (version 0.8.1)6.


## **Results and Discussion**

The read QC stats showed that Dorado produced about 2000 more total sequences in all three samples compared to those from Guppy (Table 1). In contrast, Guppy produced about 300 Mbp more total bases compared to those from Dorado. None of the reads from either of the basecallers was flagged by FastQC as of poor quality. Dorado generated longest reads compared to Guppy while the GC percentages were similar between the basecallers (Table 1). However, per base sequence quality was greatly improved in the Dorado-basecalled reads (Fig. 1). Dorado-basecalled reads produced a complete circular genome for Barcode07 and closed the gap for Barcode08 (Fig. 2) comparing between the basecallers. Barcode12 genome assembly remained independent of the basecallers (Fig. 2). All the genome quality statistics were similar between Guppy and Dorado (Table 2). 


Taken together, these findings suggest that the choice of basecaller is important for the ONT raw data, and it is worth collecting and storing the squiggles from the ONT sequencing runs to be re-basecalled later with an improved version of basecallers, thus improving genome assemblies and their associated applications.       
