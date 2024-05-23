Here's the formatted README file for your automation flow project:

# Assignment_nintex

## Some Assumptions Made to Keep Things Simple

* Input data is a set of PDF files downloaded from the PURE Data set link: [Zenodo PURE Data Set](https://www.zenodo.eu/record/1414117).
* The dataset is unlabeled.
* There were multiple approaches to consider, such as defining a classifier specifically for functional requirements and then using a semantic engine for grouping. However, I chose the LLM approach because it is better suited for unsupervised problems.

## Prerequisites

To run this notebook, you need to set up the environment:

1. **Set up environment:**
    ```bash
    pip install -r requirements.txt
    ```
2. **Replace LLM client:**
    * Replace LLM client with open-source models like LLaMA, OpenAI GPT.

## Notebook Structure

The whole notebook is divided into the following sections:
* Load the dependencies
* LLM configuration and data configuration

## Task 1: Data Collection and Preparation

### Data Description
* Data downloaded from [PURE link](https://www.zenodo.eu/record/1414117).
* Data contains 5 SRS documents in PDF format.

### Preprocessing Steps
* Load the PDF files using the `pypdf` package as pages.
* Apply the following preprocessing techniques on the PDF files:
  * Normalization
  * Removing special characters
  * Removing headers, footers, and URLs from the documents.
* Split the document using the following configuration.
* Store the result in text format for each PDF.

## Task 2: Workflow Suggestion using LLMs

* Define the MapReduce custom chain, which includes map and reduce prompt templates.
* Group the semantic requirements into groups using LLMs.
* Parse this output into functional requirements and non-functional dictionaries.
* Generate the graph.

## TODOs

* Adapt for other types of data formats.
* Add header and footer remover logic in preprocessing steps.
* Identify LLM response parser to get results in a dictionary format at first place.
* Add additional logic for mapping functional requirements with non-functional requirements TAGs.

## Future Work

* Bring the conditional branches in the automation graph.
* Identify actors and systems along with requirements.
* Build robust logic for creating dependencies and task list for the graph.
