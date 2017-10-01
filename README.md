SVmine_V2
I. Prerequisites
1. Software environment:
1. Unix/Linux system.
2. Samtools 0.1.18 or above.
3. samtools-0.1.7a_getUnique-0.1.3 (http://www.math.pku.edu.cn/teachers/xirb/downloads/software/BICseq2/BICseq2/samtools-0.1.7a_getUnique-0.1.3.tar.gz)
4. BWA
5. NBICseq_v0.7_alpha (http://www.math.pku.edu.cn/teachers/xirb/downloads/software/BICseq2/BICseq2.html)
6. NBICseq-norm_v0.2.4 (http://www.math.pku.edu.cn/teachers/xirb/downloads/software/BICseq2/BICseq2.html)
7.Breakdancer-1.1.2 (http://breakdancer.sourceforge.net/)
8.Meerkat (http://compbio.med.harvard.edu/Meerkat/)
9.Lumpy (https://github.com/arq5x/lumpy-sv.)
10 python2.7 and cython
2. Reference file and other files:
1. Reference genome sequence in fasta format and the fasta file of each chromosome
2. BWA index of reference file generated by “bwa index” command.
3. Fai index of reference file generated by “samtools faidx” command.
4. Repeat annotation (RepeatMasker output) of reference genome which can be downloaded from UCSC which put the same folder with reference genome
II Installation
After decompression
cd build
python svmine_exe_v2.py -h
or if you want to recompile the file
python setup.py src/
cp script/* build
III．Workflow
python svmine_exe_v2.py
Usage:
Python svmine_exe1.py
-h		   show this help message and exit
-b FILE   sorted and indexed bam file, required  
-f FILE    bam file dictionary, required
-o FILE   output dictionary, default output
                      
-r FILE   reference fasta file, required
-l INT    read length, default 100
-i INT    insert size of paired-end reads, default 300
-d FLOAT standard deviation of fragment, default 50
-c FILE   config file which contains path of different methods, required
-p INT   the number of paired_end reads support, default 5
-s INT   the number of split reads support, default 5
-t INT   number of threads, default 1

