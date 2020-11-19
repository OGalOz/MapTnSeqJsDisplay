


You will need python3 and Rscript to get this to run.

Input files are all listed in the directory SampleData.

You will need 3 input files: 
    The genome's fna file (such as genome.fna in SampleData)
    The genome's gene table (TSV file), (such as genes.GC in SampleData)
    A transposon insertion pool file (such as pool.n10 in SampleData (TSV file))

Then you name an uncreated directory to which you have write access, and the HTML directory
    will be created there.

Then, to run the program, run:

python3 MakeHTMLdir.py SampleData/genome.fna SampleData/genes.GC SampleData/pool.n10 NewHTMLFolder genome_name 1

where you can replace SampleData/X with your own versions of those files, and replace
MyNewHTMLFolder with your own new folder name. Include the genome name for display purposes.
1 must be at the end of the command for the program to run.
Note: The genome name must have no spaces! None of the inputs should include spaces.

After it runs, go to your dir, e.g. NewHTMLFolder, and open the file "FullDisplay_index.html"
That should run in your browser, and you will be able to see and interact with the data.


FILE FORMATS:
    The gene table must have the following columns (TSV separated):
        locusId, sysName, type, scaffoldId, begin, end, strand, name, desc
    
    The pool file must have the following columns (TSV separated):
        barcode, rcbarcode, nTot, n, scaffold, strand, pos, n2, scaffold2, strand2, pos2, nPastEnd


