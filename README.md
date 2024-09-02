# MutationScripts

Mutation caller tools:
MutationCaller3.py
Current draft of the mutation caller script.
In a future update, I will make the setup.py file so that it can handle its own dependencies, but for the moment, it requires the following dependencies:
-PyVCF3
--(not to be confused with PyVCF, which is not being supported anymore and is complicated to get functioning for python3.)
--I will be replacing this with my own modified package when I succeed in getting programs to correctly import and interpret it. It is already written, it is currently called PyVCF3_mod, but is not currently being found
-collections
-multiprocessing
-functools
-sys
-numpy
-unittest

Utility tools:

double_seg_sorter.sh:
Converts a HapIBD IBD segment output format to the pair of sorted IBD segment files required by our mutation caller.




Test Input Files for experimentation:
183.interval_list_shailee_run_1.vcf.gz
-is a gatk-generated file I use as a template to make smaller files with consistent VCF formatting.
-It does not currently contain all the contigs referenced in its header, and this causes problems with some tools.

segsTest1.seg
-A basic HapIBD format file for ibd segment input

TestInput.vcf.gz
-A smaller test vcf. Formatting may not be viable as of most recent update, and is not used in any current test.

testPedigree1.ped
-example pedigree input file
