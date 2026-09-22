# Visualise: Cohort ATC 

This simple project structure template repository is adapted from the [Good Enough Project](https://github.com/bvreede/good-enough-project) Cookiecutter template by Barbara Vreede (2019).
If you plan to develop a package, check the [template repository for a Python package](https://github.com/UtrechtUniversity/re-python-package).

## Usage

Download this repository locally, then add the following files to data/raw (download the file from the hyperlink): 
- [documents-output-json-report_en.json](https://www.ema.europa.eu/en/documents/report/documents-output-json-report_en.json)
- yyyymmdd-initial-authorisation-epar.zip (this folder contains .txt files already parsed from .pdf files)

In case files are not uploaded, the following files are run:
- 20260504-documents-output-json-report_en.json
- 20260504-initial-authorisation-epar.zip

Then, go to the config file. Define regex pattern(s) for your query that will be used to flag documents for your cohort. By default, the patterns are defined to flag the type of opinion given by the EMA. You may read more about [how experts in the EMA committees make decisions for medicinal approval here] (https://www.ema.europa.eu/en/documents/regulatory-procedural-guideline/guidance-document-voting-framework-discussion-and-adoption-chmp-opinions_en.pdf).

Running the .py script will produce a print-ready alluvial chart that displays the following:
- the total number of medicines in your analysis
- the number of medicines that were flagged by the script

## Project Structure

The project structure distinguishes three kinds of folders:
- read-only (RO): not edited by either code or researcher
- human-writeable (HW): edited by the researcher only.
- project-generated (PG): folders generated when running the code; these folders can be deleted or emptied and will be completely reconstituted as the project is run.


```
.
├── .gitignore
├── LICENSE
├── README.md
├── requirements.txt
├── data               <- All project data, ignored by git
│   ├── processed      <- The final, canonical data sets for modeling. (PG)
│   ├── raw            <- The original, immutable data dump. (RO)
│   └── temp           <- Intermediate data that has been transformed. (PG)
├── docs               <- Documentation notebook for users (HW)
│   ├── manuscript     <- Manuscript source, e.g., LaTeX, Markdown, etc. (HW)
│   └── reports        <- Other project reports and notebooks (e.g. Jupyter, .Rmd) (HW)
├── results
│   ├── figures        <- Figures for the manuscript or reports (PG)
│   └── output         <- Other output for the manuscript or reports (PG)
└── src                <- Source code for this project (HW)

```

## Add a citation file
Create a citation file for your repository using [cffinit](https://citation-file-format.github.io/cff-initializer-javascript/#/)

## License

This project is licensed under the terms of the [MIT License](/LICENSE).
