# Dynamic Eigenvector Centralities



## Paper / Purpose
This code serves as an implementation of the work on calculating keywords and their emerging importance outlined in:

Neela Avudaiappan, Alexander Herzog, Sneha Kadam, Yuheng Du, Jason Thatcher, and Ilya Safro, "
[Detecting and summarizing emergent events in microblogs and social media streams by dynamic centralities](http://alexherzog.net/files/IEEE_BigData_2017_Dynamic_Centralities.pdf)", in Proceedings of the 2017 IEEE International Conference on Big Data, 2017

The original code for this project was developed by Neela Avudaiappan. This version of the code was developed by [Grace Glenn](https://github.com/mgglenn), who fixed bugs and restructured the code.

## Results
The results in the paper have been replicated on the Boston dataset using time intervals of 60 and 15 minutes, located in `boston_examples`.

## Requirements
1. All code is run in Python 3.6 (Anaconda 4.3.0)
2. Data to be processed should be stored in ordered text files (i.e., file1.txt, file2.txt, ... fileN.txt for N intervals, or some other numbered format.)
3. Text files should contain one-document (i.e., one tweet) per line

## Usage
* Ensure all requirements are satisfied. The program can be run as follows.
```
# after repo has been downloaded
cd dynamic_eigenvector_centralities
pip install requirements.txt
python dec_main.py --input_folder /home/username/time_series_data/ --P 6 --output_folder /home/username/dec_results/
```

## Files
* `dec_main.py` Runs the full algorithm to compute DEC values described in the 
* `dec_graph.py` contains code for the graph logic of the algorithm
* `dec_text.py` contains code for preprocessing and cleaning the data
* `break_files.py` a useful script for dividing time-series CSV data
