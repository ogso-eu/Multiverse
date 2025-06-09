# Data Generation for Multiverse

This document explains how to generate the `multiverse-1k.jsonl` dataset from a source `1k.jsonl` file.

## Conversion Steps

To convert the data, you need to run a series of scripts in a specific order. Before you begin, make sure your source file, `1k.jsonl`, is placed in this directory.

Then, execute the following steps sequentially.

## Step 1: Initial Processing

This step performs the first transformation on the source data. We use the LLMs to get the reasoning structure and potential parallel groups.

```bash
bash run/step1.sh
```

## Step 2: Intermediate Processing
This step continues the data transformation. With the structure of step 1 we refill the structure to get the new reasoning chain with map-reduce paradigm.
```bash
bash run/step1.sh
```

## Step 3: Parse and Structure
This step continues the data transformation. We parse all the reasoning chain into xml file and filter the quality data with content and parser checker.
```bash
bash run/parse.sh
```

## Step 4: Refine
In this step we fine the data to improve data quality.
```bash
bash run/step3.sh
```