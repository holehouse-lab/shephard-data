## *Arabidopsis Thaliania* proteome

From UniProt (UP000006548_3702) downloaded August 5th 2022


## Processing

Remove sequences with invalid amino acid sequences with [pfasta](https://protfasta.readthedocs.io/en/latest/).

	pfasta UP000006548_3702.fasta --invalid-sequence remove -o arabidopsis_clean.fasta
	
	
Predict IDRs using [metapredict](https://metapredict.readthedocs.io/en/latest/):


	metapredict-predict-idrs arabidopsis_clean.fasta  --mode shephard-domains-uniprot  -o shprd_domains_arabidopsis_idrs.tsv --verbose