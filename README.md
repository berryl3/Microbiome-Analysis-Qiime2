# Microbiome-Analysis-Qiime2
### May 2025

This code Downloads fasta files, demux, merges, and assigns taxonomy for paired end sequencing files



## Project Set Up
> [!IMPORTANT]
> Don't skip these steps!

- [ ] Step 1: SampleMetadata File
  - Create a file of your experiment's metadata
  - In the sample-id column, do not include deliminators such as ba, ITS, bact, etc
 
  > Examples:
  >  - ✅ m1 
  >  - ❌ m1-ITS or m1_ITS 

 - See SampleMetadata.txt for example of how to format this file

   
- [ ] Step 2: Create directory
Copy the files 00_Download Fasta and 01_Manifest_Demux_Master to an empty folder

- [ ] Step 3: Download Microbiome Classifiers
      - Download 




###############



**00_Download_Fastq**

Copy URL of the project directory from the genomic.rcac database
> Enter which sample type you want (Unaligned_filtered, Merged, etc)
 
 
 
**01_Manifest_Demux**
  > Enter project name
  > Enter Metadata file name
  > Enter type of sequences that 00_Download_Fastq downloaded; default is "filtered"

  > Update dictonary and samples
     ex: [Bact]=ba
    
       [Bact]= fullname or nickname of the microbiome community
       ba = sample deliminator - what you used to differentiate between fasta files
       	ie: ba, 16S, b, etc
       	ie: fu, ITS, f, etc
       	
       	
**02_Dada2**
 > Look in community subfolders for 02_Dada2 file
 > Change project and community variables if needed
 > Update trim and trunc lengths
 > Update max depth and rarefication if needed
 
 
**03_Taxonomy**
 > Look in community subfolders for 03_Taxonomy file
 > Change project and community variables if needed
 > Update classifier
    > List of classifiers to choose from are in /depot/lhoaglan/data/'Lily 2023'/Qiime_Pipeline/Classifiers
    > Should only need to update the classifier name; not the file path
 
