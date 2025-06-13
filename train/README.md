# Training

This training setup is adapted from the [s1: Simple test-time scaling](https://github.com/simplescaling/s1) repository.

## Environment

To train `Multiverse-32B`/`Autoregressive-32B`, we recommend 16 A/H100 GPUs (i.e., 2 nodes with 8 each) or 8 B100/200 GPUs.

## Setup and Training

### Quick Start

1.  Clone the repository and navigate into it:
    ```bash
    git clone https://github.com/simplescaling/s1.git
    cd s1
    ```
2.  Install the required dependencies:
    ```bash
    pip3 install -r requirements.txt
    ```
3.  Start the training script:
    ```bash
    bash train/sft.sh
    ```
    If you are on a SLURM cluster, you may want to use `train/launch.sh` after configuring it for your setup.

### Notes
*   If you encounter an out-of-memory (OOM) issue with 8 GPUs, consider enabling gradient checkpointing by adding `--gradient_checkpointing=True` to `train/sft.sh`.
*   For `s1.1`, the original authors set the block size to 20000 to avoid OOM. This is configured in `train/sft.sh`.
