This app implements selected packages from the [RSeQC
suite](http://code.google.com/p/rseqc/wiki/Manual). These are:

* geneBody_coverage
* inner_distance
* junction_annotation
* read_distribution
* read_duplication

The app requires as input RNA-Seq mappings and a BED file describing the
gene model used for or derived from these mappings.

Optionally, the user may estimate the amounts of different contaminants in
the sample. This is done by suppling sequences through the "contaminants"
input, which takes any number of [ContigSet
objects](http://wiki.dnanexus.com/Types/ContigSet). FASTA files may be
imported into ContigSet objects using the **Genome Importer** app.

One or more [Reads objects](http://wiki.dnanexus.com/Types/Reads) MUST also
be given if contaminants are given. The reads will be matched against each
contaminant using the BWA app and the percent mapping will be stored.

The output is a set of charts in a report that can be viewed by selecting
the report object in the data browser.
