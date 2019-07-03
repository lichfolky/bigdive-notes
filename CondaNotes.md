#How to install dependencies from a requirements.txt file with conda
while read requirement; do conda install --yes $requirement; done < requirements.txt

#How can I install packages directly from conda-forge?¶
conda config --add channels conda-forge
conda config --set channel_priority strict
