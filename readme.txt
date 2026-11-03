Student Feedback Dataset (Peru, 2019) — Version 1.0.2

Dataset overview

This dataset contains 23,168 open-ended comments from university
students collected during institutional satisfaction surveys in Peru in
2019. The comments are written in Spanish and are labeled for sentiment
analysis and thematic categorization.

Version 1.0.2 is a privacy-correction release. Residual personal names
and direct identifiers found in a small number of free-text responses
were replaced with neutral placeholders. The number of records,
sentiment labels, and thematic labels were not changed.

Files

student_feedback_dataset.csv

The dataset contains three columns:

-   comentario: student feedback comment in Spanish. Privacy-related
    replacements may appear as [PERSON], [STUDENT_ID], [EMAIL], or
    [PHONE].
-   Valor: sentiment polarity assigned to the comment (Positivo or
    Negativo).
-   nombreAspecto: institutional thematic category assigned to the
    comment.

The file contains 23,168 records.

student_feedback_analysis_notebook.ipynb

A Jupyter notebook with basic exploratory analysis of the dataset. The
notebook is configured to load the v1.0.2 CSV file. Cached outputs from
the superseded dataset version were removed before this release.

Encoding

The v1.0.2 CSV file is encoded in UTF-8 with BOM (utf-8-sig).

Example in Python:

    import pandas as pd

    df = pd.read_csv(
        "student_feedback_dataset.csv",
        encoding="utf-8-sig"
    )

Privacy and de-identification

The original free-text responses were intended to be anonymized. A
subsequent privacy audit identified residual personal information
embedded in a small number of comments. For version 1.0.2, confirmed
personal names and direct identifiers were replaced with neutral
placeholders while preserving the analytical content of the dataset as
much as possible.

The following placeholders may occur:

-   [PERSON]
-   [STUDENT_ID]
-   [EMAIL]
-   [PHONE]

This correction does not change the number of records or the
distributions of the sentiment and thematic labels.

As with any free-text dataset, automated and manual de-identification
reduces disclosure risk but cannot guarantee absolute anonymity. Users
should not attempt to re-identify individuals.

Version history

v1.0.2

Privacy and de-identification correction. Residual personal names and
direct identifiers found in free-text responses were replaced with
neutral placeholders. Scientific labels and record counts were
preserved.

v1.0.1

Minor release created to enable Zenodo DOI integration. Dataset content
was identical to v1.0.

Use cases

-   Sentiment analysis in Spanish
-   Natural language processing
-   Educational quality assessment
-   Supervised machine-learning experiments

Citation

When using this dataset, cite the Zenodo record for the version used and
the associated publication, when applicable.

License

This release preserves the usage conditions of the previous public
version: the dataset is provided for non-commercial academic research
purposes only. Redistribution or commercial use is not permitted without
written permission from the authors.

Responsible use

The dataset contains educational feedback written by students. Users
should handle the text responsibly, avoid re-identification attempts,
and report any residual identifying information discovered in the public
release to the dataset authors.
