.. :changelog:

=======
History
=======

0.4.x (201x-xx-xx)
------------------
* Do some PEP8 fixes.
* Refactor orthodb module.
* Port code and tests to py33.

0.3.13 (2014-12-23)
-------------------
* Move documentation to readthedocs.
* Do some PEP8 fixes.
* Replace library `pp` for `multiprocessing`.

0.3.12 (2013-11-14)
-------------------
* Using Orthodb_ids for genes
* In order to get only those genes with no paralogs. We want only single-copy
  genes.
* Updated UnitTest for OrthoDB and BLAST

2013-11-12  Carlos Peña  <mycalesis@gmail.com>
    v0.3.11

    Parallel running of function filter_reads
    of module NGS didn't work because the depending function ``prune`` was not
    submitted to the parallel jobs.
    Fixed by importing the function inside ``filter_reads``.

2013-11-11  Carlos Peña  <mycalesis@gmail.com>
    v0.3.10

    Updated internal function `filter_reads`
    of module NGS. It is more efficient and much quicker now.

    Added UnitTest for filter_reads function
    It is an internal function in the module NGS that extracts the FASTQ reads
    according to a BLAST table output and stores them into gene bins.

2013-11-07  Carlos Peña  <mycalesis@gmail.com>
    v0.3.9

    Adding assembly_velvet.sh files
    These are used when doing assembly of contigs. If they are not
    in current folder they get downloaded from github.

2013-10-18  Carlos Peña  <mycalesis@gmail.com>
    v0.3.8

    Primer design, only process .fas[ta]* ending files
    The funcion MUSCLE.designPrimers searches in a folder for files to design
    primers for. It accepted any file. Now it accept only files ending with the
    extension .fasta or .fas (case insensitive).

2013-10-04  Carlos Peña  <mycalesis@gmail.com>
	v0.3.7

	BLAST database making
	Avoid redoing the BLAST database when user wants to use dustmaker as this is
	slow.
	If no dustmaker required, redo the database as it is quick to do.
2013-10-03  Carlos Peña  <mycalesis@gmail.com>
	BLAST: splitting input FASTA files
	If the FASTA file doesn't need to be splitted, then don't remove the original
	file!
2013-10-03  Carlos Peña  <mycalesis@gmail.com>
	Before BLAST, don't split fasta file all the time
	Module BLAST, function *blastn* was spliting all input FASTA files so
	accelerate a BLAST.
	I happened even though the input FASTA consisted of few FASTA sequences. It
	now checks that it happens when the input file has more than 399 sequences.
2013-09-24  Carlos Peña  <mycalesis@gmail.com>
	adding developers to front page
2013-09-20  Carlos Peña  <mycalesis@gmail.com>
	end for now
	testing travis
	upgrading distribute
	adding distribute
	adding blast
	fixing run_test and removing it from readme
	adding build status using Travis CI
	adding script for tests
	adding dependencies
	adding dependencies
	adding language to travis
	start using travis ci
	fixing right extension for Bombyx_exons
2013-09-19  Carlos Peña  <mycalesis@gmail.com>
	polishing test for BLAST
2013-09-18  Carlos Peña  <mycalesis@gmail.com>
	adding more genes for tests, even
	adding more genes for testing and fixing doc
	adding two more genes for testing
	adding test_getLargestExon and fixing typo in docs
2013-09-16  Carlos Peña  <mycalesis@gmail.com>
	version 0.3.5
2013-09-14  Carlos Peña  <mycalesis@gmail.com>
	preparing separtion by index function to be used in parallel
2013-09-13  Carlos Peña  <mycalesis@gmail.com>
	using parallel python for dividing reads into bins according to genes
	fixing typo in documentation
2013-09-12  Carlos Peña  <mycalesis@gmail.com>
	unittest for test_blastn
	continue unittest BLAST module
	more unittest for BLAST module
2013-09-08  Carlos Peña  <mycalesis@gmail.com>
	adding script to run all unit tests
2013-09-04  Carlos Peña  <mycalesis@gmail.com>
	package cleaning
	file cleaning
	removing unneeded files
2013-08-31  Carlos Peña  <mycalesis@gmail.com>
	unittest for BLAST in part
	OrthoDB unittest end
	start writing unittests
	removing unneded DB module
2013-08-05  Carlos.Peña  <mycalesis@gmail.com>
	adding Python version 2.7
2013-07-17  mezarino  <vm_solism@yahoo.es>
	Set 'mask=True' as the default for our blastn function; and eliminated '-parse_seqids' option from the command.
	We made mask=True as the default for blastn, so that low-complexity regions are discarded previous the blast.
	On the other hand, we eliminated '-parse_seqids' option to make the function suitable for local databases, whose sequences have ID formats different to those defined by NCBI.
2013-07-06  Carlos.Peña  <mycalesis@gmail.com>
	removing unneded files
2013-07-05  Carlos.Peña  <mycalesis@gmail.com>
	adding some info for module NGS
2013-07-05  Carlos Pena  <mycalesis@gmail.com>
	end assembly scripts
2013-06-28  Carlos Pena  <mycalesis@gmail.com>
	making sure we use FASTA instead of FAS
2013-06-26  mezarino  <vm_solism@yahoo.es>
	Update BLAST.py
2013-06-25  Carlos Pena  <mycalesis@gmail.com>
	continue from NGS.parse_blats_results
2013-06-24  Carlos Pena  <mycalesis@gmail.com>
	show how to do bluntSplicing of FASTA sequences
	adding blast to requirements
	instructions for MUSCLE under windows
	pointing online documentation
	adding beautiful soup to dependency list
2013-06-21  Carlos.Peña  <mycalesis@gmail.com>
	Preparing inofile.fastq: removing indexes before BLASTn
	Filtering of FASTQ reads, accepting those that align more than 40 bp to expected genes
2013-06-20  Carlos Pena  <mycalesis@gmail.com>
	adding assembly function
	index bins prefixed by "index_"
2013-06-19  Carlos.Peña  <mycalesis@gmail.com>
	levenshtein distance = 0
	output messages
	BLAST.blastn output message
	NGS.prepare_data output to data/modified
2013-06-16  Carlos.Peña  <mycalesis@gmail.com>
	barcode length as variable
2013-06-14  Carlos.Peña  <mycalesis@gmail.com>
	doc files
	doc files
2013-06-14  Carlos Pena  <mycalesis@gmail.com>
	adding info for separation by index
	batch of gene files into indexes
2013-06-13  Carlos Pena  <mycalesis@gmail.com>
	start separation by index
	saving gene files into output folder
	filtering reads according to gene match
	changing *folder* to *folder_path*
	adding folder argument fo bluntSplicer
	fixes
2013-06-12  Carlos.Peña  <mycalesis@gmail.com>
	split ionfile
2013-06-12  Carlos Pena  <mycalesis@gmail.com>
	fixing typo
	script for NGS analysis
	splitting BLAST output and ionrun data
	preparing fasta file
2013-06-12  mezarino  <vm_solism@yahoo.es>
	Update MUSCLE.py
	bluntSplicer function: MSA-objects splicer was incorporated.
2013-06-11  Carlos.Peña  <mycalesis@gmail.com>
	NGS analysis
	some text in NGS analysis
2013-06-11  Carlos Pena  <mycalesis@gmail.com>
	start guide for iontorrent data analysis
2013-06-11  mezarino  <vm_solism@yahoo.es>
	Update BLAST.py
2013-06-10  Carlos.Peña  <mycalesis@gmail.com>
	small fix, @echo
2013-06-10  Carlos Pena  <mycalesis@gmail.com>
	start IonTorrent NGS analysis
	fix do primers
2013-06-10  Carlos.Peña  <mycalesis@gmail.com>
	fixing silkgenome blast
2013-06-10  Carlos Pena  <mycalesis@gmail.com>
	sequences with taxon header between brackets
	primer design
	alingment warmimg
2013-06-09  Carlos Pena  <mycalesis@gmail.com>
	doing alignment
	do_gene_search.py do Heliconius
2013-06-09  Carlos.Peña  <mycalesis@gmail.com>
	do_gene_search.py Doing BLASTn
	fixing downloading silkgenome
	adding Makefile for reproducible analysis
	removing README.txt file
	fastx-toolkit as reference
	adding instructions to install dependencies
2013-06-06  Carlos Pena  <mycalesis@gmail.com>
	fixing importin upper case modules
2013-05-15  Carlos.Peña  <mycalesis@gmail.com>
	adding dependencies
2013-04-24  Carlos.Peña  <mycalesis@gmail.com>
	end primers section
2013-04-22  Carlos Pena  <mycalesis@gmail.com>
	printing primer desing restuls to file
2013-04-20  Carlos.Peña  <mycalesis@gmail.com>
	removing old scripts
2013-04-19  Carlos.Peña  <mycalesis@gmail.com>
	changing headers
	design primers in MUSCLE module
2013-04-19  Carlos Pena  <mycalesis@gmail.com>
	designing primers
2013-04-19  Carlos.Peña  <mycalesis@gmail.com>
	primer design
	adding MUSCLE to dependencies
	fixing MUSCLE
	documentation: exon alignment
2013-04-18  mezarino  <vm_solism@yahoo.es>
	Update MUSCLE.py
	Update MUSCLE.py
	The code has been change accordingly to recognize the ID format of the input sequences.
	Update BLAST.py
	Now the IDs of the stored sequences have the NCBI's format.
2013-04-18  Carlos.Peña  <mycalesis@gmail.com>
	adding sp_name
	adding sp_name for parsing BLAST table
	fixing documentation
	fixing documentation
2013-04-17  mezarino  <vm_solism@yahoo.es>
	Update OrthoDB.py
	The statement "print gene ..." from single_copy_genes function was removed because it's irrelevant to print that information.
	Update BLAST.py
	The sp_name parameter was add to the function blastParser.
2013-04-17  Carlos.Peña  <mycalesis@gmail.com>
	editing documentation
	saving alignments into folder
2013-04-17  Carlos Pena  <mycalesis@gmail.com>
	adding muscle.py
	updating quick guide
	merge
2013-04-13  Carlos.Peña  <mycalesis@gmail.com>
	documentation: Exon alignment
2013-04-12  Carlos.Peña  <mycalesis@gmail.com>
	Heliconius
	Heliconius
	working with Danaus
	working with Danaus
2013-04-11  Carlos.Peña  <mycalesis@gmail.com>
	blasting Danaus
	blasting Danaus
	dont print divisor
	dont print divisor
	editing module
	editing module
2013-04-10  Carlos Pena  <mycalesis@gmail.com>
	adding instuctions and distrubuted script
	adding instuctions and distrubuted script
	using distribute
	using distribute
	fixing code blocks
	fixing code blocks
2013-04-10  Carlos.Peña  <mycalesis@gmail.com>
	adding install pp to README
	adding install pp to README
2013-04-09  Carlos Pena  <mycalesis@gmail.com>
	adding progress bar to blastn
	adding progress bar to blastn
2013-04-09  Carlos.Peña  <mycalesis@gmail.com>
	do parallel blast, part
	do parallel blast, part
2013-04-08  Carlos Pena  <mycalesis@gmail.com>
	fixing argument in blastn function
	fixing argument in blastn function
2013-04-06  Carlos.Peña  <mycalesis@gmail.com>
	using WTF public license
	using WTF public license
2013-04-05  Carlos.Peña  <mycalesis@gmail.com>
	expanded BLAST module
	expanded BLAST module
2013-04-05  Carlos Pena  <mycalesis@gmail.com>
	Merge branch 'BlastExonParser' output a list of candidate genes
	Merge branch 'BlastExonParser' output a list of candidate genes
	including blast table parse functions in BLAST module
	including blast table parse functions in BLAST module
	including blast table parse functions in BLAST module
	including blast table parse functions in BLAST module
	including blast table parse functions in BLAST module
	including blast table parse functions in BLAST module
2013-04-04  Carlos.Peña  <mycalesis@gmail.com>
	removing blank pages from documentation pdf
	removing blank pages from documentation pdf
	adding print messages
	adding print messages
	ignoring csv gz zip files
	ignoring csv gz zip files
	edited script
	edited script
2013-03-23  Carlos.Peña  <mycalesis@gmail.com>
	making db
	making db
2013-03-12  Carlos Pena  <mycalesis@gmail.com>
	doc
	doc
	guide - blast part
	guide - blast part
	blast script
	blast script
	blast script by Mezarino
	blast script by Mezarino
2013-03-10  Carlos.Peña  <mycalesis@gmail.com>
	TODO blast
	TODO blast
	gitignore
	gitignore
2013-03-08  Carlos Pena  <mycalesis@gmail.com>
	some work on BLAST
	some work on BLAST
2013-03-05  Carlos.Peña  <mycalesis@gmail.com>
	get_cds intro
	adding get_cds intro
	adding get_cds intro
	function get_cds
	function get_cds
	getting cds file
	getting cds file
	removing build filess
	removing build filess
	0.2.0
	0.2.0
2013-03-04  Carlos.Peña  <mycalesis@gmail.com>
	including documentation in HTML files
	including documentation in HTML files
2013-03-04  Carlos Pena  <mycalesis@gmail.com>
	OrthoDB and documentation
	OrthoDB and documentation
	start documentation
	start documentation
2013-03-04  Carlos.Peña  <mycalesis@gmail.com>
	fixes
	fixes
	setup fixes
	setup fixes
2013-01-28  Carlos.Peña  <mycalesis@gmail.com>
		modified:   README.md
		modified:   README.md
2012-12-05  Carlos Pena  <mycalesis@gmail.com>
	author mezarino
	author mezarino
	ready script
	ready script
2012-12-05  Carlos.Peña  <mycalesis@gmail.com>
	finished script
	finished script
2012-12-04  Carlos.Peña  <mycalesis@gmail.com>
	arg species_name
	arg species_name
	added pars arguments
	added pars arguments
	work in progress
	work in progress
	initial script
	initial script
2012-11-29  Carlos.Peña  <mycalesis@gmail.com>
	readme in reST
	readme in reST
2012-11-28  Carlos.Peña  <mycalesis@gmail.com>
	adding OrthoDB6 gene table
	adding OrthoDB6 gene table
	adding OrthoDB6 gene table
	adding OrthoDB6 gene table
2012-11-28  Carlos Pena  <mycalesis@gmail.com>
	update README
	update README
2012-11-28  Carlos.Peña  <mycalesis@gmail.com>
	finish renaming repository
	finish renaming repository
	BLAST.py
	BLAST.py
2012-11-27  Carlos.Peña  <mycalesis@gmail.com>
	Merge remote-tracking branch 'mezarino/master'
	update Blast script
	Merge remote-tracking branch 'mezarino/master'
	update Blast script
2012-11-27  mezarino  <vm_solism@yahoo.es>
	Update pyphylogenomics/BLAST.py
	Update pyphylogenomics/BLAST.py
2012-11-27  Carlos.Peña  <mycalesis@gmail.com>
	more scripts
	more scripts
	adding scripts
	adding scripts
2012-11-25  Carlos.Peña  <mycalesis@gmail.com>
	test README
	test README
	rename
	rename
		setup.py
		setup.py
	rename
	rename
	renaming repository
	renaming repository
2012-09-23  Carlos.Peña  <mycalesis@gmail.com>
	more scripts
	more scripts
2012-05-14  Carlos.Peña  <mycalesis@gmail.com>
	README markdown
	README markdown
v0.1.0, 2012-04-08 -- Initial release
