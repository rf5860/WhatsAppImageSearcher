# WhatsAppSearcher

This repository is a tool for searching through images exported from WhatsApp using [CLIP](https://github.com/openai/CLIP).

## Pre-requisites

I'd recommend using a virtual environment to install the required packages. To start, you should install [conda](https://conda.io/projects/conda/en/latest/user-guide/install/index.html). After which, you can create the required environment using the following commands:

Note that you may need to adjust the `pytorch-cuda` version depending on your system - you can find the correct version [here](https://pytorch.org/get-started/locally/).
```sh
conda create --name WhatsAppSearcherEnv python=3.9
conda activate WhatsAppSearcherEnv
conda install --yes pytorch torchvision torchaudio pytorch-cuda=12.1 -c pytorch -c nvidia
conda install --yes ftfy regex tqdm ipykernel Pillow ipywidgets
pip install git+https://github.com/openai/CLIP.git
```

## Usage

Simply export a chat from WhatsApp, and place the extracted contents into the `history/` directory. Then run the Python notebook `WhatsAppSearcher.ipynb` to search through the images.

To change the search query, simply change the `query` variable in the notebook (Under the section  "Encode the query").

## Example

Here's an example of searching for the query "star wars" in a WhatsApp chat:

![Example](./docs/imgs/example.png)