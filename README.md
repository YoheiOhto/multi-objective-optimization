# Multi-Objective Optimization of Reference Compound Lists for Rigorous Evaluation of Predictive Toxicity Models

This repository optimizes a set of compounds using a genetic algorithm. Furthermore, we curate a dataset of compounds used in pharmaceutical safety test validation studies by JaCVAM and compare them with the compounds derived from the genetic algorithm.

---

## Publication
### preprint
Rigorous Evaluation of Predictive Toxicity Models by Multi-Objective Optimization of Reference Compound Lists Using Genetic Algorithms  
https://arxiv.org/abs/2505.07140  

### peer-reviewed publication
not yet

---

## File Structure

The project is organized into the following main directories:

- **data/**: Contains data files.
- **processed/**: Processed data.
- **raw/**: Raw data.
- **result/**: The directory is structured to correspond with the figures in our paper.
- **data_validation_test_and_HTS/**: Contains validation test and HTS (High-Throughput Screening) data in an easy-to-use format.
- **notebook/**: Contains Jupyter Notebooks for various tasks.
- **experiment/**:
  - `0_dataset_unbalance.ipynb`: Visualizes the imbalance in the number of positive data points and the bias in toxicity strength within the dataset.
  - `1_GA.ipynb`: Runs the multi-objective genetic algorithm (GA) to optimize compound sets based on similarity scores and toxicity variation.
  - `2_UMAP.ipynb`: Uses UMAP to visualize the distribution of compounds generated through a genetic algorithm.
  - `3_random_generation.ipynb`: Compares the random population, GA results, and the validation test dataset by generating various plots and histograms.
  - `4_use_each_gen_for_eval.ipynb`: Analyzes the performance of the GA by measuring the distance of the generated compound sets from the Pareto front.
  - `5_tox_prediction.ipynb`: Compares toxicity prediction performance between the validation data and the GA-generated datasets.
- **preprocess/**:
  - `0_preprocess_ice.ipynb`: Extracts LD50 or DART test data, including CAS-RN and toxicity information, from the ICE dataset.
  - `1_preprocess_toxcast.ipynb`: Extracts Tox21 ER or AR test data, including CAS-RN and toxicity information, from the ToxCast dataset.
  - `2_preprocess_validation_test.ipynb`: Prepares the main dataset for the genetic algorithm by removing compounds used in the validation test.
  - `3_preprocess_for_lookup.ipynb`: Creates lookup tables containing canonical SMILES and physicochemical properties for compound pairs by utilizing PubChemPy and CAS-RN.
  - `4_preprocess_for_tox_prediction.ipynb`: Prepares the datasets for toxicity prediction by splitting the data into training, evaluation, test, and GA-selected sets.
- **src/**: Python scripts for core functionalities.
  - `ga.py`: Genetic algorithm core components.
  - `prep.py`: Data preprocessing scripts.
  - `util.py`: Utility functions.
- **requirements.txt**: Lists the project dependencies.

---

## Authors

- **Yohei Ohto** - Main contributor  
- **Tadahaya Mizuno** - Correspondence  

---

## Contact

If you have any questions or comments, please feel free to create an issue on GitHub here, or email us:

- oy826c60[at]gmail.com  
- tadahaya[at]gmail.com  
- tadahaya[at]mol.f.u-tokyo.ac.jp
