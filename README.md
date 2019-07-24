# Notebooks for the anlysis of [NLM Medical Subject Headings MeSH](https://www.nlm.nih.gov/mesh/meshhome.html)

## Extracting information from MeSH thesaurus

The processus of extracting information frome MeSH follows this simple steps:

 1. Download MeSH thesaurus in XML format from https://www.nlm.nih.gov/mesh/filelist.html
 1. Extract and anlyze the MeSH XML tree
 1. Select the informations to extract with the UID (loops and secondary loops)
 
## Examples

### [Entry Terms for all the Pharamacological Actions](pharmacologial_actions)

The idea, proposed by Mrs Kirsten van Gelderen-Ziesemer for the workshop "[Mining PubMed metadata with Pandas and Jupyter Notebooks](https://www.conftool.com/eahil2019/index.php?page=browseSessions&downloads=show&form_session=39&mode=table&presentations=show)", was to collect all underlying [entry terms (synonyms)](https://www.nlm.nih.gov/mesh/intro_entry.html) for the MeSH terms that are noted for one particular pharmacological action, without manual copy/paste form the multiple MeSH terms concerned. The list of synonyms may be useful in the research work carried out in systematic reviews, in order to include the largest possible number of studies.

The solution proposed in this folder was to execute two separate extractions for each MeSH term: one with all the Phramacological Actions and another one with all the Entry Terms for each MeSH term. Then we merge the two dataframes and get a table with all the possible Entry Terms for all the MeSH terms concerned by each Pharmacological Action. There are 4'617 Pharmacological Actions, 234'843 combination of MeSH Term / Entry Term and 48'181 combination of Pharmacological Actions / Entry Term in total. For example, one single Pharmacological Action as "Antihypertensive agents" has 102 MeSH terms and 1'188 Entry Terms for those MeSH terms.

 