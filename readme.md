# Notebooks

This repo contains Jupyter notebooks for training the following neural audio models on Kaggle (some also on Google Colab):

- [RAVE](https://github.com/acids-ircam/RAVE)
- [VSCHAOS2](https://github.com/acids-ircam/vschaos2)
- [MSPrior](https://github.com/caillonantoine/msprior)
- [AFTER](https://github.com/acids-ircam/AFTER)
- [RAVE-Latent Diffusion](https://github.com/moiseshorta/RAVE-Latent-Diffusion)
- [RAVE-Latent Diffusion (Flex'ed)](https://github.com/devstermarts/RAVE-Latent-Diffusion-Flex-ed)

## How to use on Kaggle

### Setup training
1. Add new notebook (via "+" button)
2. Inside notebook editor, go to "File -> Import Notebook"
3. Select "GitHub" from the tab options in the fly-in menu
4. Search for and add "devstermarts/Notebooks"
5. Select main branch (default)
6. Choose from any of the Kaggle notebooks 
7. Click "Import"
8. Add your datasets and models via "Input" section
9. Change paths to your datasets and models in the respective parts of the notebook
10. Add/ change your preferred preprocessing/ training/ generation options
11. Click "Save Version" in the top right
12. In "Advanced Settings" select "Run with GPU for this session"
13. Click "Save"
14. Hope, wait, go for a walk, sleep, repeat

### Resume training
Kaggle notebooks run for 12h max before terminating automatically. In case you need to run a longer training, here's a hacky resume option:
1. Wait for your run to finish
2. Go to Output tab of your finished notebook
3. On the right, next to "Output" click on the three dots -> select "New Dataset". This creates a new dataset out of the earlier training run.
4. Go back into your original training notebook.
5. Add the newly created dataset from your earlier training run via "Input" section. 
6. In the code of your notebook, add a command to copy the contents of the new dataset into your working folder BEFORE the training section ('!cp -r /kaggle/input/my-earlier-training-run/* /kaggle/working')
7. Change your training command with flags to resume training and/or updated paths (model dependent, check the respective documentation)
8. Optional/ model dependent: deactivate preprocessing step. 
9. Save notebook to run.

## Disclaimer
I don't maintain the code in the source repositories (exception being RAVE-Latent Diffusion (Flex'ed)) and therefore cannot provide support. However, if you notice that any of the notebooks in this repository do not work and run into errors, please let me know and i'll see to investigate.
