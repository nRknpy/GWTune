# Toolbox for Gromov-Wasserstein optimal transport (GWTune)
This toolbox supports an easy-to-use hyperparameter tuning of Gromov-Wasserstein optimal transport (GWOT) and unsupervised alignment based on GWOT.  
To find good local minima in GWOT, hyperparameter tuning is essential.  
This toolbox uses [Optuna](https://optuna.org/) for hyperparameter tuning and [POT](https://pythonot.github.io/) for GWOT optimization.  

## Tutorials
To use our toolbox, please first try out our main tutorial notebook `tutorial.ipynb` in the `scripts` folder.  
You can learn how to use this toolbox on two examples of behavioral data (`color` and `THINGS`).   
By replacing the tutorial data with your own data, you can easily test GWOT on your own data!  
To further facilitate use cases of our toolbox, we also provide tutorials for other types of datasets, neural data (`AllenBrain`) and neural network models (`DNN`).   
You can find these tutorials in the `tutorial_other_datasets` folder.   

## Installation 
We outline instructions for installing the required packages using `poetry`, `conda`, `pip`.

### Step1
- `poetry`
    
    Install the required packages using `pyproject.toml`
    ```
    poetry install
    ```
- `conda`

    Install the required packages using `environemnt.yaml`
    ```
    conda env create -n GWTune -f environment.yaml
    source activate GWTune
    ```
- `pip`
    
    Install the required packages using `requirements.txt`.
    ```
    virtualenv .env && source .env/bin/activate
    pip install -r requirements.txt
    ```

### Step2
After installing the packages above, install `torch` that is compatible with your environment.    
For compatibility information, see the [official pytorch page](https://pytorch.org/get-started/locally/).  

## Datasets for the main tutorial
1. `color`: Human similarity judgements of 93 colors for 5 participant groups made from the data used in [Kawakita et al., 2023, PsyArxiv](https://psyarxiv.com/h3pqm/)
2. `THINGS` : Human similarity judgments of 1854 objects for 4 participant groups made from [the THINGS dataset](https://things-initiative.org/)  

### Other tutorials datasets 
3. `AllenBrain`: Neuropixels recordings in the primary visual cortex of mice from [the Visual Coding - Neuropixels dataset](https://portal.brain-map.org/explore/circuits/visual-coding-neuropixels)    
4. `DNN`: Internal representations of vision DNNs (ResNet50 and VGG19) for a subset of visual images from the ImageNet dataset   
5. `simulation`: Synthetic data illustrating differences between supervised alignment and unsupervised alignment

### Using and Citing the toolbox
If you use this toolbox in your research and find it useful, please cite the following papers and give a star ⭐.

[1] Toolbox for Gromov-Wasserstein optimal transport: Application to unsupervised alignment in neuroscience   
Masaru Sasaki\*, Ken Takeda\*, Kota Abe, Masafumi Oizumi    
bioRxiv: To be uploaded   
\*equal contribution   

[2] Is my "red" your "red"?: Unsupervised alignment of qualia structures via optimal transport.  
Genji Kawakita\*, Ariel Zeleznikow-Johnston\*, Ken Takeda\*, Naotsugu Tsuchiya, Masafumi Oizumi  
PsyArxiv: https://psyarxiv.com/h3pqm/  
*equal contribution

## References
If you are interested in the details of dataset used in the tutorials or in the mathematical details of unsupervised alignment based on GWOT, please refer to the papers above [1,2].  

## Creators and Maintainers
This toolbox has been created and is maintaned by:

- Masaru Sasaki
- Ken Takeda
- Kouta Abe
- Masafumi Oizumi

## Acknowledgments
We thank Genji Kawakita for early code contributions. We also thank Ariel Zeleznikow-Johnston and Naotsugu Tsuchiya for providing the data on color similarity judgments.
