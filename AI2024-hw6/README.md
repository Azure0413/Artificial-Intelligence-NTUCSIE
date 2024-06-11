# Environment Installation Instructions:
## 1. conda create -y -n ai_hw6 python=3.10
## 2. conda activate ai_hw6
## 3. install pytorch based on your cuda version (my cuda version is 12.1)
### e.g. pip install torch==2.3.0
## 4. cd ./AI2024-hw6
## 5. pip install --no-deps -r requirements.txt
## 6. pip install -r requirements_1.txt
## 7. install the correct version of unsloth 
### 7-1. conda install pytorch-cuda=12.1 pytorch cudatoolkit xformers -c pytorch -c nvidia -c xformers
### 7-2. pip install "unsloth[cu121-torch230] @ git+https://github.com/unslothai/unsloth.git"

# Run the code
## 1. bash run.sh exp_name model_name wandb_token (and other hyperparameters)
### e.g. bash run.sh DPO unsloth/llama-3-8b-bnb-4bit (wandb_token)
### e.g. bash run.sh ORPO unsloth/llama-3-8b-bnb-4bit (wandb_token)
### e.g. bash run.sh DPO unsloth/llama-3-8b-bnb-4bit (wandb_token) --num_epochs 3
### e.g. bash run.sh DPO unsloth/llama-3-8b-bnb-4bit (wandb_token) --beta 0.5
### e.g. bash run.sh DPO unsloth/mistral-7b-instruct-v0.3-bnb-4bit (wandb_token)
### e.g. bash run.sh ORPO unsloth/mistral-7b-instruct-v0.3-bnb-4bit (wandb_token)
### e.g. bash run.sh DPO unsloth/llama-3-8b-Instruct-bnb-4bit (wandb_token)
### e.g. bash run.sh ORPO unsloth/llama-3-8b-Instruct-bnb-4bit (wandb_token)

## 2. bash inference.sh model_name wandb_token
### e.g. bash inference.sh unsloth/llama-3-8b-bnb-4bit (wandb_token)