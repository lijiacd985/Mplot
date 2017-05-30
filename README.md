# practice

Requirements:

DeepTools
matplotlib



Installation

mdepth.py

This script will plot the Mean CpG methylation ratio and number of CpG sites under a series depth for multiple samples. The input file is the output file (*stat.txt) from mcall (MOABS).

Meth2ChIP.py

This script will plot the average ChIP-seq signals at certain methylation ratio range (5% intervals);the input files are methylation ratio file (*.G.bed from mcall MOABS) and the ChIP-seq signals intensity file.

multiBw2bed.py / multiBw2multiBed.py

This script generate the curve plot with multi-bigwig singal files against interested regions (bed file). Input files are multiple bigwig files and one bed (or multiple bed files) file.

horizonalHeatmap.py

This script will use bigwig and bed files as input and plot multiple types of signals distribution on interested locations (up/dnstream xxx bp) as a horizonal heatmap.


multiTracks.py

This script will use bigwig and bed files as input and output pictures of multi-bigwig signals for each loci in the bedfiles. (similar with UCSC visualization tracks but can generated many automatically) 

Example command:
python  multiTracks.py -bs 100 -f regions.txt -b H3K4me3_m24.merge.bw H3K27me3_m24.merge.bw KO-K4m3.norm.bw KO-K27m3.norm.bw  -labels m_H3K4me3 m_H3K4me3 KO_H3K4me3 KO_H3K27me3 -out testRegions1.npz testRegions2.npz testRegions3.npz testRegions4.npz testRegions5.npz -outRawCounts testRegions1.tab testRegions2.tab testRegions3.tab testRegions4.tab testRegions5.tab -c r g b black yellow

regions.txt:
chr4:82878750:82888151	geneName1
chr14:56255857:56265260	geneName2
chr7:44809255:44818658	geneName3
chr7:45915022:45924426	geneName4
chr8:85068756:85078161	geneName5
