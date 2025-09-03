# Microbiome-Analysis-Qiime2

Microbiome analysis with QIIME2
May 2025

This code Downloads fasta files, demux, merges, and assigns taxonomy for paired end sequencing files


######  Before Running Any Code   ##################

Item 1:
SampleMetadata File
 > User needs to create a file of your experiment's metadata
 > Note: In the sample-id column, don't include deliminators such as ba, ITS, bact, etc
    > Should look like this m1
    > Shouldn't look like m1-ITS or m1_ITS
 > See SampleMetadata.txt for example of how to format this file


Item 2:
Copy the files 00_Download Fasta and 01_Manifest_Demux_Master to an empty folder

###############



00_Download_Fastq
 > Enter URL of samples in genomic.rcac database
   > Update password if needed
 > Enter which sample type you want (Unaligned_filtered, Merged, etc)
 
 
 
01_Manifest_Demux
  > Enter project name
  > Enter Metadata file name
  > Enter type of sequences that 00_Download_Fastq downloaded; default is "filtered"

  > Update dictonary and samples
     ex: [Bact]=ba
    
       [Bact]= fullname or nickname of the microbiome community
       ba = sample deliminator - what you used to differentiate between fasta files
       	ie: ba, 16S, b, etc
       	ie: fu, ITS, f, etc
       	
       	
02_Dada2
 > Look in community subfolders for 02_Dada2 file
 > Change project and community variables if needed
 > Update trim and trunc lengths
 > Update max depth and rarefication if needed
 
 
03_Taxonomy
 > Look in community subfolders for 03_Taxonomy file
 > Change project and community variables if needed
 > Update classifier
    > List of classifiers to choose from are in /depot/lhoaglan/data/'Lily 2023'/Qiime_Pipeline/Classifiers
    > Should only need to update the classifier name; not the file path
 
