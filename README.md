# Analyzing Science Articles: Gene Identification In Brain Tumors
**Author: Julia C.**

**Warning: The information presented in this website is an on going senior research project, and the information will be pieriodically updated.**

![Brain Tumor](https://th.bing.com/th/id/R.70beee177fe41452e199ef763fbb2866?rik=kaByp%2baW8pO2nw&riu=http%3a%2f%2fwww.10faq.com%2fassets%2fimg%2fbrain-tumor-symptoms-05.jpg&ehk=9Rz3Egl0RsDaWTvQsq2iGM1aZBW5Blg%2fAOh%2ffLgPzcc%3d&risl=&pid=ImgRaw&r=0)

## *Objective*
The objective of the project is to identify genes associated with brain tumors, providing insight into genetic factors linked to brain tumor development and prognosis through mentions in biological article's and their abstracts.

## Based on Senior Research Paper
Here is the link to the paper: 

## *Background On The Data Resource and Brain Tumors*
PubTator Central, or PTC, is a free online resource that provides bio information using PubMed articles. PTC is a system that highlights six biomedical concepts mentioned in PubMed article abstracts, which are summaries of research articles [1]. PubMed is a literature-based resource where scientific articles and other resources can be found. Still, it is just one of many resource systems in the National Library of Medicine: National Center for Biotechnology Information (NCBI) government website. There are well over 30 million pieces of biomedical literature that PubTator can access, and there are various categories under biomedical, with brain tumors being one [1]. The point of this tool is to help researchers in many ways, like making it easier to identify genes, diseases, chemicals, and other biomedical concepts to help researchers analyze important information in various numbers or research articles and find related work on biological topics quickly. It helps provide data that researchers can use data mining techniques to analyze and understand more on the data. PubTator will be the system where data will be obtained for this project, for it contains research article abstracts on studies done regarding brain tumors. 

Studying and researching brain tumors is important because they are serious, life-threatening diseases. They are abnormal cell growth or intracranial neoplasms, for not all tumors come from brain tissues and are very serious [2]. The exact cause of the abnormal cell growth is unknown. However, researchers are looking at genetic and molecular changes in a person's cell to understand why there was a change in cells that caused them to start growing abnormally, which in turn caused the tumors [3]. Genes are essential because they are the building blocks of life; they are segments of DNA that determine how an organism looks, behaves, and survives in environments or places they are in [4]. Diagnosing brain tumors can be done through various tests, one being an MRI scan with a gadolinium enhancement that examines the brain, looking for any indications of abnormalities [2]. Brain tumors can fall under two categories: benign or malignant. Benign tumors stay put and do not travel to other parts of the body, unlike malignant cancerous tumors that can spread (metastasize) from one part of the body to another [5]. Since benign tumors do not disperse, they are just classified by their look, size, and area in which it is located; however, malignant tumors are then can be further classified into specific types or histologic (main) categories, which will then sometimes have subcategories which will be placed into a type of grade [5]. Grades of tumors can be grade I or grade II, low-grade tumors that grow slowly and are less likely to cause nearby tissues to become tumors, and higher-grade tumors, grade III or IV, will grow quickly and cause other tissues to follow its path [5]. Brain tumors are rare in children; however, it is the leading cause of death in children and adults diagnosed with cancer [6].  There are so many different types of brain tumors; however, they are hard to diagnose, for they have symptoms like headaches and nausea or vomiting, which other diseases can also cause. These symptoms are why brain tumors in children are often delayed in diagnosis or misdiagnosed, for it could be other ailments [7].

 Studying all tumors' biological, genetic, or mechanical factors is essential to understand how they behave or grow, spread, and react to other tissues in the human body. It is important to understand the molecular mechanisms of brain cancerous tumors to help improve diagnosis and treatment to help decrease the disease's mortality [6]. Changes in genes, called mutations, can lead to malformation of proteins that cannot perform their duties as they are meant to, leading to genetic disorders or even diseases like cancer [4]. Studying tumor genes and associated genes will help researchers understand what makes a tumor different from normal tissue. If they find what causes the tumor, they can potentially create more effective treatments that will target the cause of the tumor and save lives. For example, take a specific type of primary brain tumor, which is a tumor that originates in the brain and does not spread from another part of the body called glioblastoma multiforme (GBM), which is more common, for it is invasive and malignant, where prognosis or the effect of the disease on the patient and survival rates are poor and makes up about 70% of glioma malignancies [8]. It being the leading cause of death in cancer patients of various ages, from children to adults, makes it crucial for researchers to study brain tumors, especially malignant ones, to help develop treatments to reduce the mortality rate.

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
## Results
In this section lays the results of the experiment, remember the objective of the experiment was to identify genes associated with brain tumors, providing insight into genetic factors linked to brain tumor development and prognosis through mentions in biological article's and their abstracts. 

[Complete Frequency Table for Abstacts](For github/full_abstract_table.html)

[Complete Frequency Table for Full-Text](For github/full_full-text_table.html)

[Complete Frequency Table Total](For github/full_total_table.html)

![Top 10 Gene Names for Abstracts](Top10_Ab_BarG.png)

![Top 10 Gene Names for Full-Text](Top10_FT_BarG.png)

![Top 10 Gene Names for Total](Top10_Total_BarG.png)

![Word Clouds](WordCloud_AB.png)
![Word Clouds](WordCloud_FT.png)
![Word Clouds](WordCloud_Total.png)


## References
- [1]	C.-H. Wei, A. Allot, R. Leaman, and Z. Lu, “PubTator central: automated concept annotation for biomedical full text articles,” Nucleic Acids Res., vol. 47, no. W1, pp. W587–W593, Jul. 2019, doi: 10.1093/nar/gkz389.

> [2]	L. M. DeAngelis, “Brain Tumors | NEJM,” The New England Journal of Medicine. Accessed: Oct. 03, 2023. [Online]. Available: https://www.nejm.org/doi/full/10.1056/NEJM200101113440207

- [3]	“What causes brain tumours?,” The Brain Tumour Charity. Accessed: Oct. 12, 2023. [Online]. Available: https://www.thebraintumourcharity.org/brain-tumour-diagnosis-treatment/how-brain-tumours-are-diagnosed/brain-tumour-biology/what-causes-brain-tumours/

- [4]	“Genes: Function, makeup, Human Genome Project, and research.” Accessed: Oct. 12, 2023. [Online]. Available: https://www.medicalnewstoday.com/articles/120574

- [5]	“Types of Brain and Spinal Cord Tumors in Children.” Accessed: Oct. 03, 2023. [Online]. Available: https://www.cancer.org/cancer/types/brain-spinal-cord-tumors-children/about/types-of-brain-and-spinal-tumors.html

- [6]	M. Zhao, Y. Liu, G. Ding, D. Qu, and H. Qu, “Online database for brain cancer-implicated genes: exploring the subtype-specific mechanisms of brain cancer,” BMC Genomics, vol. 22, no. 1, p. 458, Jun. 2021, doi: 10.1186/s12864-021-07793-x.

- [7]	A. L. Albright, “Pediatric brain tumors,” CA. Cancer J. Clin., vol. 43, no. 5, pp. 272–288, 1993, doi: 10.3322/canjclin.43.5.272.
