# Measuring Gender Bias in Information Retrieval Models

The files `DocumentSet.csv`, `QuerySet.csv`, and `FineTuningDataset.csv` are based on data from the User Study by Kopeinik et al. [1] (https://github.com/CPJKU/user-interaction-gender-bias-IR). The contents of the file `GenderedSentences` are taken from May et al. [2] (https://github.com/W4ngatang/sent-bias). The file `wordlist_genderspecific.txt` is taken from Rekabsaz et al. [3] (https://github.com/navid-rekabsaz/GenderBias_IR).
Below the contents of each file are described.

**DocumentSet.csv**

The file `DocumentSet.csv` contains a set of documents from domains sensitive to gender bias. They are a subset of the `Grep-BiasIR dataset` (https://github.com/KlaraKrieg/GrepBiasIR). The columns names and their content descriptions follow:

* `Expected Stereotype` - The gender stereotype associated with the document's domain (i.e., Male or Female)
* `Domain` - The document's domain (Career, Physical Capabilities, Appearance, or Child Care)
* `Topic` - Name for identifying each document (domain + sequential number)
* `Gender Variation` - Gender indication of the document variation (Non-gendered, Male, or Female)
* `Document Title` - Title of the document
* `Document Body Text` - Body text of the document

**QuerySet.csv**

The file `QuerySet.csv` contains 280 bias-sensitive queries (35 from each of eight topics).

* `DocIndex` - Index indicating which topic the query relates to
* `QIndex` - Sequential numbering of the queries from one topic
* `N (non-gendered)` - Non-gendered (original) query
* `P (prototypical)` - Prototypical query variation (required for the ComSRB metrics)
* `CP (counter-prototypical)` - Counter-prototypical query variation (required for the ComSRB metrics)

**FineTuningDataset.csv**

The file `FineTuningDataset.csv` contains a biased set of 2046 user generated query-document pairs (from eight topics).

* `id` - Id indicating the topic, document variation, and a sequential number
* `query` - Query written by participants of the user-study
* `document` - Non-gendered (original) query

**GenderedSentences.csv**

The file `GenderedSentences.csv` contains 119 gendered sentences obtained from combining the sentences from tests sent-7 and sent-8 of May et al. [2] (https://github.com/W4ngatang/sent-bias).

* `Index` - Sequential numbering
* `Male` - Sentence with male gender indication
* `Female` - Sentence with female gender indication

**wordlist_genderspecific.txt**

The file `wordlist_genderspecific.txt` contains the list of 32 gender-representative words per gender used in the RepSRB metrics.

### References

[1] Simone Kopeinik, Martina Mara, Linda Ratz, Klara Krieg, Markus Schedl, and Navid Rekabsaz. “Show me a "Male Nurse"! How Gender Bias is Reflected in the Query Formulation of Search Engine Users”. In: Proceedings of the CHI Conference on Human Factors in Computing Systems (CHI ’23). 2023

[2] Chandler May, Alex Wang, Shikha Bordia, Samuel R. Bowman, and Rachel Rudinger. “On Measuring Social Biases in Sentence Encoders”. In: Proceedings of the 2019 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, Volume 1 (Long and Short Papers). 2019

[3] Navid Rekabsaz and Markus Schedl. “Do neural ranking models intensify gender bias?” In: Proceedings of the 43rd International ACM SIGIR Conference on Research and Development in Information Retrieval. 2020
