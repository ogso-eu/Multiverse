# Data Generation for multiverse-1k.jsonl

Data section outlines the process for generating the `Multiverse-1K` dataset. The generation process begins with the `simplescaling/s1K-1.1` dataset and involves a series of sequential scripts to transform and refine the data.

## Prerequisites

Before initiating the data generation process, you must first acquire the `simplescaling/s1K-1.1` dataset. Once obtained, rename the file to `1.1k.jsonl` and place it in the root directory of this project. You can use follow the step 1 to collect data.

## Data Generation Pipeline

The conversion from the source `1.1k.jsonl` file to the final `multiverse-1k.jsonl` dataset is accomplished by executing a series of scripts in the specified order. Each step builds upon the output of the previous one.

### Step 1: Initial Data Collection

This initial step gathers the source `1.1k.jsonl` dataset to prepare it for processing.

```bash
bash run/collect.sh
```

### Step 2: Extracting Reasoning Structures

In this step, the initial `1.1k.jsonl` data is processed using Large Language Models (LLMs). The primary goal is to extract the underlying reasoning structures and identify potential parallel groupings within the data.

```bash
bash run/step1.sh
```

### Step 3: Reconstructing Reasoning Chains

With the foundational structure from the previous step, this script applies a map-reduce paradigm to refill and reconstruct the reasoning chains. This creates a more detailed and structured representation of the reasoning process.

```bash
bash run/step2.sh
```

### Step 4: Parsing and Quality Assurance

This step focuses on structuring and validating the generated data. The script parses the reasoning chains into XML format. Following the parsing, both a content checker and a parser checker are used to filter for high-quality data. Any data that does not meet the quality standards is cycled back to Step 2 for reprocessing.

```bash
bash run/parse.sh
```

### Step 5: Final Refinement

The last step in the pipeline is to refine the data to further enhance its quality. The output of `step3.sh` constructs the `Multiverse-1K` dataset.

```bash
bash run/step3.sh
```

## Training data

To convert `Multiverse-1K` data to the training data prepared for the next section, please run:
```bash
bash run/train_data.sh
```