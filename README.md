# Analyzing Science Articles: Identifying Genes Associated with Brain Tumors
**Author: Julia C.**

**Warning: The information presented in this website is an on going senior research project, and the information will be pieriodically updated.**

![Brain Tumor](https://th.bing.com/th/id/R.70beee177fe41452e199ef763fbb2866?rik=kaByp%2baW8pO2nw&riu=http%3a%2f%2fwww.10faq.com%2fassets%2fimg%2fbrain-tumor-symptoms-05.jpg&ehk=9Rz3Egl0RsDaWTvQsq2iGM1aZBW5Blg%2fAOh%2ffLgPzcc%3d&risl=&pid=ImgRaw&r=0)

## *Objective*
The objective of the project is to identify genes associated with brain tumors, providing insight into genetic factors linked to brain tumor development and prognosis through mentions in biological article's and their abstracts.

## Based on Senior Research Paper
Here is the link to the paper: ![Senior Research Paper](For github/Genes Associated with Brain Tumors.docx)

## *Background On The Data Resource and Brain Tumors*
Brain tumors cause serious, life-threatening diseases, for they are abnormal cell growths [2]. There are several factors that can lead to  abnormal cell growth, and researchers are looking at genetic and molecular changes in a person's cell to understand why there was a change in cells that caused them to start growing abnormally, which in turn caused the tumors [3]. Genes are the building blocks of life; they are segments of DNA that determine how an organism looks, behaves, and survives in environments or places they are in [4]. Diagnosing brain tumors can be done through various tests, one being an MRI scan with a gadolinium enhancement that examines the brain, looking for any indications of abnormalities [2]. Brain tumors can either be benign or malignant. Benign tumors stay put and do not travel to other parts of the body, unlike malignant cancerous tumors that can spread (metastasize) from one part of the body to another [5]. Since benign tumors do not disperse, they are just classified by their look, size, and area in which it is located; however, malignant tumors can be further classified into specific types or histologic (main) categories, which will then sometimes have subcategories which will be placed into a type of grade [5]. Grade I or II are low-grade tumors that grow slowly and are less likely to cause nearby tissues to become tumors, and higher-grade tumors, grade III or IV, will grow quickly and cause other tissues to become tumors [5]. The likely hood on developing a primary cancerous brain tumor is less than 1%, however it is estimated that around 5,000 children under 20 will be diagnosed with it in the year 2023 in the United States [6]. The leading cause of death in children and adolescence is cancer, and brain tumors being one of the top 3 cancers [1]. There are so many different types of brain tumors; however, they are hard to diagnose, for they have symptoms like headaches and nausea or vomiting, which other diseases can also cause. These symptoms are why brain tumors in children are often delayed in diagnosis or misdiagnosed, for it could be other ailments [7].  

Studying all tumors' biological, genetic, or mechanical factors is essential to understand how they behave or grow, spread, and react to other tissues in the human body. Understanding the molecular mechanisms of brain cancerous tumors to help improve diagnosis and treatment to help decrease the disease's mortality [8]. Studying the mechanics of the tumors will help researchers learn more about why tumors in the brain happen and learn other things, like how the genetics of the tumors can be different due to mutations, which will affect the locations in which they develop in a person [5]. Mutations (i.e., changes in DNA sequence) can lead to malformation of proteins that cannot perform their duties as they are meant to, leading to genetic disorders or even diseases like cancer [4]. Studying tumor genes and associated genes will help researchers understand what makes a tumor different from normal tissue. If they find what causes the tumor, they can create more effective treatments that will target the cause of the tumor and save lives. 

Researchers share their findings through research articles, which are published and can be accessed through various web platforms such as PubMed (https://pubmed.ncbi.nlm.nih.gov/). PubMed is a literature-based resource where scientific papers and other resources can be found and is one of many resource systems in the National Library of Medicine: National Center for Biotechnology Information (NCBI) government website. PubMed articles and their abstracts can be accessed through the PubTator Central platform, or PubTator for short, a free online resource that provides bio information using PubMed articles. PubTator is a system that highlights six biomedical concepts mentioned in PubMed article abstracts, which are summaries of research articles [9]. A user can obtain PMIDs (PubMed IDs) of articles by saving an article in a collection by clicking the heart icon underneath the article title and author names. There are well over 30 million pieces of biomedical literature that PubTator can access, and there are various categories under biomedical, with brain tumors being one [9]. The point of this tool is to help researchers in many ways, like making it easier to identify genes, diseases, chemicals, and other biomedical concepts to help researchers analyze important information in various numbers or research articles and find related work on biological topics quickly. Suppose researchers want to download data on the biochemicals. In that case, they can use the PubTator API platform, where following the instructions will obtain data and is the main reason PMIDs are important. PubTator helps provide data that researchers can analyze. 

The project aimed to identify genes associated with brain tumors, providing insight into genetic factors linked to brain tumor development and prognosis, through mentions in biological articles and their abstracts. PubTator was the source from which data was obtained for the project, and it contained research articles on studies done regarding brain tumors (Note: the experiment used Python in Jupyter Notebook environment to analyze the data). The project's outcome will help other researchers learn what genes are associated with brain tumors, which could lead to future research on the most frequently referenced gene in brain tumors. In addition, it will help educate researchers new to studying brain tumors on what genetic information has been discovered and what has been most focused on based on the number of times the gene name is referenced. Understanding genes associated with brain tumors will help other research topics focus more on certain types of genes that have the potential for better treatment plans.

## Results
In this section lays the results of the experiment, remember the objective of the experiment was to identify genes associated with brain tumors, providing insight into genetic factors linked to brain tumor development and prognosis through mentions in biological article's and their abstracts. 

[Complete Frequency Table Total](For github/full_total_table.html)

![Top 10 Gene Names for Total](For github/Top10_Total_BarG.png)

[Complete Frequency Table for Abstacts](For github/full_abstract_table.html)

![Top 10 Gene Names for Abstracts](For github/Top10_Ab_BarG.png)

[Complete Frequency Table for Full-Text](For github/full_full-text_table.html)

![Top 10 Gene Names for Full-Text](For github/Top10_FT_BarG.png)


![Word Clouds](For github/WordCloud_AB.png)
![Word Clouds](For github/WordCloud_FT.png)
![Word Clouds](For github/WordCloud_Total.png)


## Code Described in the Methodology Section in the Paper
```python
# Step 1: Read the text file and extract ID numbers
file_name = 'Gene and Diseases proper pmids.txt'
id_num = []

with open(file_name, 'r') as file:
    for line in file:
        line = line.strip()
        if line:
            id_num.append(line)
            
# Step 2: Create a set to store the ID 
#     numbers for quick uniqueness checks
id_set = set()
duplicate_ids = []

# Step 3: Check for duplicates
for id_number in id_num:
    if id_number in id_set:
        duplicate_ids.append(id_number)
    else:
        id_set.add(id_number)
# Output
if not duplicate_ids:
    print("No duplicates found.")
else:
    print("Duplicates:")
    for id in duplicate_ids:
        print(id)
```

## References
> [1]	“Cancer Facts & Figures 2023,” Am. Cancer Soc., 2023. Pages 12 and 14. [Online]. Available: https://www.cancer.org/content/dam/cancer-org/research/cancer-facts-and-statistics/annual-cancer-facts-and-figures/2023/2023-cancer-facts-and-figures.pdf 

> [2]	L. M. DeAngelis, “Brain Tumors | NEJM,” The New England Journal of Medicine. Accessed: Oct. 03, 2023. [Online]. Available: https://www.nejm.org/doi/full/10.1056/NEJM200101113440207

> [3]	“What causes brain tumours?,” The Brain Tumour Charity. Accessed: Oct. 12, 2023. [Online]. Available: https://www.thebraintumourcharity.org/brain-tumour-diagnosis-treatment/how-brain-tumours-are-diagnosed/brain-tumour-biology/what-causes-brain-tumours/

> [4]	“Genes: Function, makeup, Human Genome Project, and research.” Accessed: Oct. 12, 2023. [Online]. Available: https://www.medicalnewstoday.com/articles/120574

> [5]	“Types of Brain and Spinal Cord Tumors in Children.” Accessed: Oct. 03, 2023. [Online]. Available: https://www.cancer.org/cancer/types/brain-spinal-cord-tumors-children/about/types-of-brain-and-spinal-tumors.html

> [6]	“Brain Tumor - Statistics,” Cancer.Net. Accessed: Dec. 05, 2023. [Online]. Available: https://www.cancer.net/cancer-types/brain-tumor/statistics

> [7]	A. L. Albright, “Pediatric brain tumors,” CA. Cancer J. Clin., vol. 43, no. 5, pp. 272–288, 1993, doi: 10.3322/canjclin.43.5.272.

> [8]	M. Zhao, Y. Liu, G. Ding, D. Qu, and H. Qu, “Online database for brain cancer-implicated genes: exploring the subtype-specific mechanisms of brain cancer,” BMC Genomics, vol. 22, no. 1, p. 458, Jun. 2021, doi: 10.1186/s12864-021-07793-x.

> [9]	C.-H. Wei, A. Allot, R. Leaman, and Z. Lu, “PubTator central: automated concept annotation for biomedical full text articles,” Nucleic Acids Res., vol. 47, no. W1, pp. W587–W593, Jul. 2019, doi: 10.1093/nar/gkz389.
