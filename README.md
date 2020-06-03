# TaggerOne

This project is from NCBI. Based on [TaggerOne-0.2.1](https://www.ncbi.nlm.nih.gov/research/bionlp/tools/taggerone/). You can get the origin code and model from NCBI by this [URL](https://www.ncbi.nlm.nih.gov/research/bionlp/taggerone/TaggerOne-0.2.1.tgz). 

I haven't found official repo for this project and I fixed an *endless-loop* bug in it. So I put my updated version here. 

If there's any suggestion, feel free to contact me. 

# Use TaggerOne for annotation of texts


The script "ProcessTexts.sh" can be used to run TaggerOne on own texts with a suitable pretrained model.

The TaggerOne-0.2.1.tgz file contains several pretrained models and some other NLP data which is required for using ProcessTexts.sh.

Concretly the two directories "output" (containing pretrained models) and "nlpdata" (containing some NLP data) from inside the tar file need be coppied to the current directory for runnig ProcessTexts.sh

Then the command line below will run the "BC5CDRC" model to find chemicals inside the texts in 
/tmp/pubtatorExample.txt . This file need to be in Pubtator format, which is described here:

[formats](https://www.ncbi.nlm.nih.gov/CBBresearch/Lu/Demo/tmTools/Format.html)

The found mentions of chemicals will be written to /tmp/pubtatorExample.annotated.txt, as well in te Pubtator format.


```
./ProcessText.sh Pubtator output/model_BC5CDRC.bin /tmp/pubtatorExample.txt /tmp/pubtatorExample.annotated.txt
```

