# Frustratingly Easy WSD

### Abstract
Accurate interpretation of medical abbreviations is essential for clinical
decision-making since most clinical text from Electronic Health Records (EHRs)
are unstructured and often contain ambiguous abbreviations without full spells or
expansions. A simple approach for Word Sense Disambiguation (WSD) for med-
ical abbreviations is presented in this research. By calculating the odds ratio of
word tokens surrounding ambiguous abbreviations with their potential expansions,
our method constructed a knowledge dictionary from a large medical text corpus.
The knowledge dictionary is used to expand expansions using a word we call Most
Informative Word , determined by Odds Ratio (OR) calculation. Using the NCBI
Disease Corpus test set we constructed a set of sentences with ambiguous abbrevia-
tions, which we used to evaluate our approach, as well as traditional machine learn-
ing (SVM) and deep learning (BERT) models. The results show that our most ca-
pable OR approach, despite its simplicity of using a single word in the disambigua-
tion process, achieved an accuracy of 0.821, which is close to the SVM (0.868) and
BERT (0.892) models. This study highlights the potential of using a simple and
interpretable method for WSD tasks in fields where precision is crucial..


---

### data (Folder Structure)

#### OR 
- **OR1_WC.csv**: Dictionary filtered, with non-zero word count or frequency.
- **OR1_WC_top1.csv**: Dictionary filtered containing a single word with the highest odds ratio per expansion.

#### ncbi
- **NCBItestset_corpus_WSD.txt**: Manually annotated version for WSD built from the original test set of the NCBI disease corpus.
- **WSD_NCBI_dict.csv**: Dictionary containing the abbreviations, expansions, and expansion variations used in the study.
- **WSD_NCBI_sentences.csv**: Set of 200 ambiguous sentences containing ambiguous abbreviations where their expansions are absent.

#### pubmed_abstracts
- **abstracts_final.csv**: Set of abstracts used in the study.

#### rule_based
- **sentences_final.csv**: Processed sentences using a rule-based context annotation from the PubMed abstracts, used for Machine Learning and Deep Learning model training.
