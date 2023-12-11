# Analyzing Science Articles: Identifying Genes Associated with Brain Tumors
**Author: Julia C.**


![Brain Tumor](https://th.bing.com/th/id/R.70beee177fe41452e199ef763fbb2866?rik=kaByp%2baW8pO2nw&riu=http%3a%2f%2fwww.10faq.com%2fassets%2fimg%2fbrain-tumor-symptoms-05.jpg&ehk=9Rz3Egl0RsDaWTvQsq2iGM1aZBW5Blg%2fAOh%2ffLgPzcc%3d&risl=&pid=ImgRaw&r=0)

## *Objective*
The objective of the project is to identify genes associated with brain tumors, providing insight into genetic factors linked to brain tumor development and prognosis through mentions in biological article's and their abstracts.

## Based on Senior Research Paper
Here is the link to the paper: [Senior Research Paper](For github/GenesAssociatedwithBrainTumors.docx.html)

## Table of Contents
- [Background](#background-on-the-data-resource-and-brain-tumors)
- [Results](#results)
- [Discussion](#discussion)
    - [Discussions: Overview](#overview)
    - [Discussions: Reflection and Limitations](#reflection-and-limitations)
    - [Discussions: Last-Remarks](#last-remarks)
- [Code and Description of the Code](#code-described-in-the-methodology-section-in-the-paper)
    - [Gathering PMIDs](#dealing-with-pmids)
    - [Gathering Information](#using-the-pmids-to-gather-proper-information)
    - [Gene Names into Lists](#placing-gene-names-into-lists)
    - [Analyzing the data](#analyzing-the-data)
        - [Frequency Tables](#frequency-tables)
        - [Bar Graphs](#bar-graphs)
        - [Word Clouds](#word-clouds)
- [References](#references)
<a name="headers"/>

## *Background On The Data Resource and Brain Tumors*
Brain tumors cause serious, life-threatening diseases, for they are abnormal cell growths [2]. There are several factors that can lead to  abnormal cell growth, and researchers are looking at genetic and molecular changes in a person's cell to understand why there was a change in cells that caused them to start growing abnormally, which in turn caused the tumors [3]. Genes are the building blocks of life; they are segments of DNA that determine how an organism looks, behaves, and survives in environments or places they are in [4]. Diagnosing brain tumors can be done through various tests, one being an MRI scan with a gadolinium enhancement that examines the brain, looking for any indications of abnormalities [2]. Brain tumors can either be benign or malignant. Benign tumors stay put and do not travel to other parts of the body, unlike malignant cancerous tumors that can spread (metastasize) from one part of the body to another [5]. Since benign tumors do not disperse, they are just classified by their look, size, and area in which it is located; however, malignant tumors can be further classified into specific types or histologic (main) categories, which will then sometimes have subcategories which will be placed into a type of grade [5]. Grade I or II are low-grade tumors that grow slowly and are less likely to cause nearby tissues to become tumors, and higher-grade tumors, grade III or IV, will grow quickly and cause other tissues to become tumors [5]. The likely hood on developing a primary cancerous brain tumor is less than 1%, however it is estimated that around 5,000 children under 20 will be diagnosed with it in the year 2023 in the United States [6]. The leading cause of death in children and adolescence is cancer, and brain tumors being one of the top 3 cancers [1]. There are so many different types of brain tumors; however, they are hard to diagnose, for they have symptoms like headaches and nausea or vomiting, which other diseases can also cause. These symptoms are why brain tumors in children are often delayed in diagnosis or misdiagnosed, for it could be other ailments [7].  

Studying all tumors' biological, genetic, or mechanical factors is essential to understand how they behave or grow, spread, and react to other tissues in the human body. Understanding the molecular mechanisms of brain cancerous tumors to help improve diagnosis and treatment to help decrease the disease's mortality [8]. Studying the mechanics of the tumors will help researchers learn more about why tumors in the brain happen and learn other things, like how the genetics of the tumors can be different due to mutations, which will affect the locations in which they develop in a person [5]. Mutations (i.e., changes in DNA sequence) can lead to malformation of proteins that cannot perform their duties as they are meant to, leading to genetic disorders or even diseases like cancer [4]. Studying tumor genes and associated genes will help researchers understand what makes a tumor different from normal tissue. If they find what causes the tumor, they can create more effective treatments that will target the cause of the tumor and save lives. 

Researchers share their findings through research articles, which are published and can be accessed through various web platforms such as PubMed (https://pubmed.ncbi.nlm.nih.gov/). PubMed is a literature-based resource where scientific papers and other resources can be found and is one of many resource systems in the National Library of Medicine: National Center for Biotechnology Information (NCBI) government website. PubMed articles and their abstracts can be accessed through the PubTator Central platform, or PubTator for short, a free online resource that provides bio information using PubMed articles. PubTator is a system that highlights six biomedical concepts mentioned in PubMed article abstracts, which are summaries of research articles [9]. A user can obtain PMIDs (PubMed IDs) of articles by saving an article in a collection by clicking the heart icon underneath the article title and author names. There are well over 30 million pieces of biomedical literature that PubTator can access, and there are various categories under biomedical, with brain tumors being one [9]. The point of this tool is to help researchers in many ways, like making it easier to identify genes, diseases, chemicals, and other biomedical concepts to help researchers analyze important information in various numbers or research articles and find related work on biological topics quickly. Suppose researchers want to download data on the biochemicals. In that case, they can use the PubTator API platform, where following the instructions will obtain data and is the main reason PMIDs are important. PubTator helps provide data that researchers can analyze. 

The project aimed to identify genes associated with brain tumors, providing insight into genetic factors linked to brain tumor development and prognosis, through mentions in biological articles and their abstracts. PubTator was the source from which data was obtained for the project, and it contained research articles on studies done regarding brain tumors (Note: the experiment used Python in Jupyter Notebook environment to analyze the data). The project's outcome will help other researchers learn what genes are associated with brain tumors, which could lead to future research on the most frequently referenced gene in brain tumors. In addition, it will help educate researchers new to studying brain tumors on what genetic information has been discovered and what has been most focused on based on the number of times the gene name is referenced. Understanding genes associated with brain tumors will help other research topics focus more on certain types of genes that have the potential for better treatment plans.

## Results
In this section lays the results of the experiment, remember the objective of the experiment was to identify genes associated with brain tumors, providing insight into genetic factors linked to brain tumor development and prognosis through mentions in biological article's and their abstracts. 

For the experiment, 1,100 samples were examined, and around a total of 736 gene names were referenced. However, split between abstracts and full-text around 656 genes were mentioned in the abstracts and 136 in full-text. **Table 1** is the complete frequency table ([Footnote: 1]) that contains all the gene names referenced in order from highest frequency (*the most mentioned*) to the lowest and at the top displaying the total number of genes in the table and the amount of genes that are unique (*only mentioned once*).
[Footnote: 1]: It is the combination of abstract and full-text data together.
**Table 1:** [Complete Frequency Table Total](For github/full_total_table.html) ([Footnote: 2])
**Table 1:** The complete frequency table containing the combination of abstracts and full-text date.

[Footnote: 2]: In some visualizations the title will reference to Total or TOTAL, which just means the total gene names data (*combination of abstracts and full-text*).

**Table 2** displays the top 10 gene names from **Table 1**. Both tables show there were two genes that were the most mentioned, BRAF and MGMT. For a better view of the most mentioned genes overall, a bar graph (see **Graph 1**) was made, and it is a great visualization of BRAF and MGMT being referenced 33 times. The first 5 gene names mentioned were all in the thirties, with the first and second (BRAF and MGMT) having the same number, 33, and the third and fourth (IDH and EGFR) having the frequency of 31. 
**Table 2:** [Top 10 Total Gene Names](For github/Complete_Top10_FreqTable.png)
**Table 2:** Displays the top 10 most frequently mentioned genes.

**Graph 1:**![Top 10 Gene Names for Total](For github/Top10_Total_BarG.png)
**Graph 1:** The graph displays the top 10 most frequenly mentioned genes shown in **Table 2**.

**Graph 1** displays that the first 4 gene names are tide in first and second place. It also shows that the number of mentions from the first rank genes names is almost 2 times more than the last in the top 10, VEGF.

However, when abstracts and full-text are separated the gene names most mentioned changes. **Table 3** displays the complete table of all the abstracts data, with the gene names referenced in order from highest frequency (*the most mentioned*) to the lowest and at the top displaying the total number of genes in the table and the amount of genes that are unique (*only mentioned once*).
**Table 3:** [Complete Frequency Table for Abstacts](For github/full_abstract_table.html)
**Table 3:** The complete frequency table containing the abstracts data.

**Table 4:** [Top 10 Abstracts Frequency Table](For github/Abstracts_Top10_FreqTable.png)
**Table 4:** Displays the top 10 most frequently mentioned gene names in abstract data alone.

**Table 4** displays the top 10 gene names from **Table 3**. For abstracts, GFAP was mentioned 29 times and is ahead of BRAF by only 2. For a better visualization that GFAP was the most mentioned in the abstract data a bar graph (**Graph 2**) was made. 

**Graph 2:**![Top 10 Gene Names for Abstracts](For github/Top10_Ab_BarG.png)
**Graph 2:** The graph displays the top 10 most frequently mention genes shown in **Table 4**.

Additionally, in full-text alone, the MGMT was the most referenced with being mentioned only 8 times (see **Table 5 and 6**). 

**Table 5:**[Complete Frequency Table for Full-Text](For github/full_full-text_table.html)
**Table 5:** The complete frequency table containing the full-text data.

**Table 6:**[Top 10 Full-Text Frequency Table](For github/FullText_Top10_FreqTable.png)
**Table 6:** Displays the top 10 most frequently mentioned gene names in full-text data alone.

**Table 6** displays the top 10 gene names from **Table 5**. As stated before, the MGMT gene was the most mentioned, and it was ahead of the second place gene IDH1 by only 1 and ahead of BRAF by 2. For a better visualization that MGMT was the most mentioned in the full-text data a bar graph (**Graph 3**) was made. 

**Graph 3:**![Top 10 Gene Names for Full-Text](For github/Top10_FT_BarG.png)
**Graph 3:** The graph displays the top 10 most frequently mentioned gene names in full-text data alone.

Word clouds were created to display the most referenced gene names, the size of the word represents the number of frequecies it had. **Graph 4** contains all three word clouds with the top represents the abstracts only data, the middle for only full-text data, and the last for the total (*combination of both abstract and full-text data*).
**Graph 4:**
![Word Clouds](For github/WordCloud_AB.png)
![Word Clouds](For github/WordCloud_FT.png)
![Word Clouds](For github/WordCloud_Total.png)
**Graph 4:** The graph is composted of three word clouds. Abstacts (top), Full-text (middle) and Total data (bottom).

All the word clouds were able to display the top frequency gene names seen in the other results as well.

## Discussion
### Overview

Understanding genes associated with brain tumors provided insight into genetic factors linked to brain tumor development and prognosis through how much they were mentioned in biological articles and their abstracts. Looking at the results, it showed the most referred to gene along with the other top 10 frequently mentioned genes (see **Tables 1** for complete table, **Table 2** for top 10 total gene names), which will help researchers new to studying brain tumors on what genes are associated with this disease had been discovered and most focused on based on the number of times the gene name is referenced.
The results show out of the total 739 genes total, the BRAF and MGMT genes were the most referenced overall. Both genes had the same frequency of 33, with IDH and EGFR coming in second place with a frequency of 31.  BRAF stands for B-Raf proto-oncogene which encodes for a protein that plays a role in regulating MAP kinase which affects cell division and other things along the line and if it is mutated it is most commonly found in cancer causing mutations [10]. The MGMT gene also called O-6-methylguanine-DNA methyltransferase, which codes for a protein that repairs and protects cells from mutagenesis and toxicity, also seen in cancer causing mutations [10a]. When looking at the data separately, the abstracts and the full-text there is a slight difference in the ranking of the gene names. For in the abstracts only the gene GFAP is at the top with 29 frequencies or mentions, and BRAF in second with 27 frequencies. When just looking at the full-text the gene MGMT was first with the highest number, being 8. In comparing the number of frequencies between abstracts and full-text there is a considerable difference for the abstracts’ top mentioned genes were in the twenties, the full-text was in the single digits (see **Tables 5** fo complete table and **Table 6** for top 10). It is good to note that majority of the genes found in total only were mentioned once, about 540 to be exact, which can be seen in the full total table (see **Table 1**).

### Reflection and Limitations

The methods used during the experiment were more complex, or in other words, a long way to obtain the information was used. Being new to PubTator and PubMed, the researcher did not initially realize there were other, more straightforward methods to get the data but learned them along the way. One lesson is that although PubTator API states that abstract and full-text code to obtain the data are slightly different, they are not. Using just the code for abstracts will work for both. Another lesson learned was that PubMed has filters for abstracts and full-text, so instead of downloading the list of samples, splitting them into abstracts and full-text was unnecessary. Of course, looking through each chunk of PMIDs would still be the same steps to see what documents contain gene information, for not all of them would. As a precaution, to ensure there are no duplicates, the steps on comparing the PMIDs for abstracts and full-text are still done. Other than those lessons, the rest of how the data was obtained would stay the same.

Although the experiment went over well and lots of precautions were taken to obtain sufficient data to make a scientific reasoning or conclusion based on the information gathered that BRAF and MGMT are the most known gene associated with brain tumors, there were a few limitations to the study.  One limitation of the experiment is a small data sample size was used. Although 1,100 samples might seem sufficient, remember there were around 226,378 results but only 10,000 PMIDs could be downloaded and saved at a time. After the samples, there were still 8,556 more PMIDs that could have been looked through if there was no deadline for the project. Time is another limitation, for a deadline was required for the project because it is a senior research project. When using PubTator, the way the website operated made it hard for quick keyboard shortcuts to be used and splitting the screen harder than it should have been. For splitting the screen, PubTator had to take up most of the screen to see the number of collections and other important aspects of the website, so going back and forth with it took time. Also, the enter button does not work in PubTator for the search bar, which made it an inconvenience when copying and pasting the PMIDs in the search bar by using the keyboard shortcuts worked; however, then the mouse cursor had to be moved and click on the search icon to start the request which affected the time it took to get the necessary data. Relying on the accuracy of PubTator code, looking at biochemical genes being properly labeled was another limitation found during the experiment. Like all code, it sometimes makes mistakes, especially when finding text. For example, PRODUCT and AID were counted as genes in articles since the letters are similar to those of a specific gene name, such as PRAC1 and ACIDA, so some mentioned genes might not have been in an article [9]. The code only made some of these errors due to the inconsistency of scientists calling genes by different names. PubTator’s gene code contains a section when trying to find genes called “alias,” which lists all the different alias names that scientists call a gene [9]. Another limitation is that the code created might not have captured all of the genes for a few shared the same or more than one identifier number separated by a semicolon (;). If more time was given then it would be used to check the code more thoroughly one a much smaller sample size before transitioning to a sample size that is over 1,000. 

### Last Remarks

Despite the limitation, PubTator is still a powerful tool for researchers to study types of biochemicals in diseases, such as brain tumors. It can be seen in similar research studies where researchers used PubTator to help provide data. One group of researchers created a website containing data collection on tumor suppressor gene (TSG) biological functions associated with various cancers [11]. They developed an updated database of their old model, a literature base database that provides resources for cancer research, and the researchers looked for keywords in abstracts from PubMed and extracted the gene names [11]. The researchers continued doing other things while collecting the data, with the results being a database that contains information on various types of tumor suppressor genes, like how they are expressed and mutated in different types of cancer, and more biological information. The TSG research is similar to this project, taking biological information about genes and their association with diseases like cancer and brain tumors from scientific literature. 

Similar to the other related work, a research group also created their database website; however, it was based on genes associated with leukemia. These researchers also used leukemia-based literature from the NCBI website to obtain the proper gene information for their database, which contains around 1805 genes associated with leukemia [12]. PubTator made it easier for researchers for this project or others to look at biological information and their associated diseases in one spot for easy access. 
Overall, the experiment was successful, showing that BRAF and MGMT were the most talked about gene concerning brain tumors. If the experiment could be repeated, a few methods would be changed, such as more time, leading to a bigger sample size and an easier way to obtain the data, as described above. In any case, the experiment should help provide researchers with necessary information on the genes that are associated the most with brain tumors, which has the potential to help further other research in brain tumors to understand the disease in the hope that one day, more efficient treatments will develop and lives will be saved.


## Code Described in the Methodology Section in the Paper
In this section, discussion about the code and what the code used to obtain the results will be here. **If you are trying to repeat the experiment the PMIDs used are in the "For Github" folder with the names of:**
> Gene and Diseases proper pmids.txt: Contains the over 8,000 rest of the PMIDs not used in the experiment if you would like to use more samples in your experiment
> Make an excel worksheet that contains the PMIDs in abstracts and full-text
    > In the experiment Abstracts and full text.xlsx was made

### Dealing with PMIDs
In this subsection, created code to look through the list of samples of PMIDs to check for duplicates and separated them into abstracts and full-text. (**The processed used, but menstioned in the REFLECTION AND LIMITAIONS part of Discussions, there was an easier way.**)

Down below is looking through the text file that contains the 1,100 PMID samples, checking for any duplicates. **If there are duplicates delete one of them and collect more PMIDs if needed.**
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

The code down below is counting the number of PMIDs to make sure there are 1,100 of them.
```python
# Step 1: Read the text file and extract ID numbers
file_name = 'Gene and Diseases proper pmids.txt'
id_num = []

with open(file_name, 'r') as file:
    for line in file:
        line = line.strip()
        if line:
            id_num.append(line)
            
# Step 2: Count the number of samples
total_count_sample = len(id_num)

# Output
print(f"The total number of samples for this experiment: {total_count_sample}")
```
Down below was how the abstracts and full-text PMIDs were separated. Copy and paste a batch of the PMIDs from the 1,100 samples file to the main_list variable and the full-text PMIDs into the full_text variable. **See paper [Senior Research Paper](For github/GenesAssociatedwithBrainTumors.docx.html) for how the researcher use the code.**
```python
# Function to find IDs that do not match between two lists
def find_non_matching_ids(list1, list2):
    # Convert the lists to sets for faster comparison
    set1 = set(list1)
    set2 = set(list2)

    # Find the IDs that are in list1 but not in list2
    non_matching_ids = set1 - set2

    return list(non_matching_ids)

# Example lists of IDs
main_list = []
full_text = []

print("Length of main list", len(main_list))

print("Length of full-text", len(full_text))

# Find non-matching IDs
non_matching_ids = find_non_matching_ids(main_list, full_text)
print("length of non_matching_ids", len(non_matching_ids))

# Display the non-matching IDs
print("Non-matching IDs:", non_matching_ids)

```

Here is an example on how the code above would work when placing the PMIDs into it.

**Example:**
```python
# Function to find IDs that do not match between two lists
def find_non_matching_ids(list1, list2):
    # Convert the lists to sets for faster comparison
    set1 = set(list1)
    set2 = set(list2)

    # Find the IDs that are in list1 but not in list2
    non_matching_ids = set1 - set2

    return list(non_matching_ids)

# Example lists of IDs
main_list = [31090175, 
33476393, 
33972919, 
34570449, 
36717507,
7848917,
11837749, 
25464144]
full_text = [25464144, 31090175, 33476393, 33972919, 34570449, 36717507]

print("Length of main list", len(main_list))

print("Length of full-text", len(full_text))

# Find non-matching IDs
non_matching_ids = find_non_matching_ids(main_list, full_text)
print("length of non_matching_ids", len(non_matching_ids))

# Display the non-matching IDs
print("Non-matching IDs:", non_matching_ids)
```

Checking the abstracts text file, looking at how many samples are in it and for duplicates.

*Sample Length*
```python
# Step 1: Read the text file and extract ID numbers
file_name = 'Pmids_Abstracts.txt'
id_num = []

with open(file_name, 'r') as file:
    for line in file:
        line = line.strip()
        if line:
            id_num.append(line)
            
# Step 2: Count the number of samples
ab_count_sample = len(id_num)

# Output
print(f"The total number of samples for this experiment: {ab_count_sample}")
```
*Duplicate Check*
```python
# Step 1: Read the text file and extract ID numbers
file_name = 'Pmids_Abstracts.txt'
id_num = []

with open(file_name, 'r') as file:
    for line in file:
        line = line.strip()
        if line:
            id_num.append(line)
            
# Step 2: Create a set to store the ID numbers for quick uniqueness checks
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

Checking the full-text text file, looking at how many samples are in it and for duplicates.

*Sample Length*
```python
# Looking at length of full-text list

# Step 1: Read the text file and extract ID numbers
file_name = 'Pmcids_FullText.txt'
id_num = []

with open(file_name, 'r') as file:
    for line in file:
        line = line.strip()
        if line:
            id_num.append(line)
            
# Step 2: Count the number of samples
full_count_sample = len(id_num)

# Output
print(f"The total number of samples for this experiment: {full_count_sample}")
```
*Duplicat Check*
```python
# Step 1: Read the text file and extract ID numbers
file_name = 'Pmcids_FullText.txt'
id_num = []

with open(file_name, 'r') as file:
    for line in file:
        line = line.strip()
        if line:
            id_num.append(line)
            
# Step 2: Create a set to store the ID numbers for quick uniqueness checks
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

The code down below checks to make sure the PMIDs in both the abstract and full-text are not in both.
```python
# Step 1: Read the contents of the first text file and extract numbers
file_path1 = 'Pmids_Abstracts.txt'
numbers1 = set()

with open(file_path1, 'r') as file1:
    for line in file1:
        line = line.strip()
        if line:  # Ignore empty lines
            numbers1.add(line)

# Step 2: Read the contents of the second text file and extract numbers
file_path2 = 'Pmcids_FullText.txt'
numbers2 = set()

with open(file_path2, 'r') as file2:
    for line in file2:
        line = line.strip()
        if line:  # Ignore empty lines
            numbers2.add(line)

# Step 3: Compare the two sets to find duplicates
duplicates = numbers1.intersection(numbers2)

# Check if there are duplicates (Output)
if not duplicates:
    print("No duplicates found.")
else:
    print("Duplicates found:")
    for duplicate in duplicates:
        print(duplicate)
```

Making sure that the length of abstracts and full-text equals the total amount of samples: 1,100.

```python
# do the numbers add up?
print(total_count_sample)

match = ab_count_sample + full_count_sample
print(match)

total_count_sample == match
```
### Using the PMIDs to Gather Proper Information
Down below the code used the PubTator API to create JSON code and places the information into an excel file. 
**The code is only gathering:**
    > full-text article or abstract ID number
    > gathering type "Gene"
    > the identifier of the gene name
    > the gene name

**For abstracts** and placing the information into another tab on the worksheet alsong with highlighting the PMIDs that were checked, to help visualy keep track at what the code looked at.
```python
import requests
import json
from openpyxl import load_workbook
from openpyxl.styles import PatternFill
import pandas as pd

def modify_url():
    workbook = load_workbook('Abstracts and full text.xlsx')
    read_worksheet = workbook['abstracts']
    max_row = read_worksheet.max_row
    chunk_size = 8
    
    yellow_fill = PatternFill(start_color='FFFF00', end_color='FFFF00', fill_type='solid')
    
    gene_info_list = []  # Collect gene info into a list
    
    for start_row in range(1, max_row, chunk_size):
        end_row = min(start_row + chunk_size - 1, max_row)
        
        pmid_list = []
        for row_num in range(start_row, end_row + 1):
            cell_value = read_worksheet.cell(row=row_num, column=1).value
            pmid_list.append(cell_value)
            read_worksheet.cell(row=row_num, column=1).fill = yellow_fill
        
        gene_info = extract_geneInfo(pmid_list)
        gene_info_list.extend(gene_info)  # Append gene info to the list
    
    update_worksheet(gene_info_list, workbook)  # Write all gene info at once

def extract_geneInfo(pmid_list):
    base_url = "https://www.ncbi.nlm.nih.gov/research/pubtator-api/publications/export/biocjson"
    concepts = "gene"
    gene_info_list = []
    
    # Fetch data in batches of 100 PMIDs
    for i in range(0, len(pmid_list), 100):
        pmids = ','.join(str(p) for p in pmid_list[i:i+100])
        mod_url = f"{base_url}?pmids={pmids}&concepts={concepts}"
        response = requests.get(mod_url)
        
        if response.status_code == 200:
            json_objects = response.text.split('\n')
            for json_obj in json_objects:
                if json_obj.strip():
                    data = json.loads(json_obj)
                    _id = data.get('_id')
                    for passage in data['passages']:
                        for ann in passage['annotations']:
                            infons = ann.get('infons', {})
                            if infons.get('type') == 'Gene':
                                identifier = infons.get('identifier')
                                gene_type = infons.get('type')
                                gene_name = ann.get('text')
                                gene_details = {"_id": _id, "identifier": identifier, "type": gene_type, "gene_name": gene_name}
                                gene_info_list.append(gene_details)
        else:
            print("Error:", response.status_code)
            print(response.text) 
    
    return gene_info_list

#update the worksheet
def update_worksheet(gene_info, workbook):
    df = pd.DataFrame(gene_info, columns=['_id', 'identifier', 'type', 'gene_name'])
    with pd.ExcelWriter('Abstracts and full text.xlsx', engine='openpyxl') as writer:
        writer.book = workbook
        writer.sheets = {ws.title: ws for ws in workbook.worksheets}
        df.to_excel(writer, sheet_name='AB_Gene_Names', index=False, startrow=1, header=False)

modify_url()
```

**For full-text** and placing the information into another tab on the worksheet alsong with highlighting the PMIDs that were checked, to help visualy keep track at what the code looked at.

```python
import requests
import json
from openpyxl import load_workbook
from openpyxl.styles import PatternFill
import pandas as pd

def modify_url():
    workbook = load_workbook('Abstracts and full text.xlsx')
    read_worksheet = workbook['FT']
    max_row = read_worksheet.max_row
    
    blue_fill = PatternFill(start_color='0000FF', end_color='0000FF', fill_type='solid')
    
    gene_info_list = []  # Collect gene info into a list
    
    for row_num in range(1, max_row + 1):
        cell_value = read_worksheet.cell(row=row_num, column=1).value
        read_worksheet.cell(row=row_num, column=1).fill = blue_fill
        
        if cell_value is not None:
            pmid_list = [cell_value]
            gene_info = extract_geneInfo(pmid_list)
            gene_info_list.extend(gene_info)  # Append gene info to the list
    
    update_worksheet(gene_info_list, workbook)  # Write all gene info at once

def extract_geneInfo(pmid_list):
    # Remaining code remains the same...
    base_url = "https://www.ncbi.nlm.nih.gov/research/pubtator-api/publications/export/biocjson"
    concepts = "gene"
    gene_info_list = []
    
    # Fetch data in batches of 100 PMIDs
    for i in range(0, len(pmid_list), 100):
        pmids = ','.join(str(p) for p in pmid_list[i:i+100])
        mod_url = f"{base_url}?pmids={pmids}&concepts={concepts}"
        response = requests.get(mod_url)
        
        if response.status_code == 200:
            json_objects = response.text.split('\n')
            for json_obj in json_objects:
                if json_obj.strip():
                    data = json.loads(json_obj)
                    _id = data.get('_id')
                    for passage in data['passages']:
                        for ann in passage['annotations']:
                            infons = ann.get('infons', {})
                            if infons.get('type') == 'Gene':
                                identifier = infons.get('identifier')
                                gene_type = infons.get('type')
                                gene_name = ann.get('text')
                                gene_details = {"_id": _id, "identifier": identifier, "type": gene_type, "gene_name": gene_name}
                                gene_info_list.append(gene_details)
        else:
            print("Error:", response.status_code)
            print(response.text)  
            
    return gene_info_list  # Return the collected gene information

# Update the worksheet
def update_worksheet(gene_info, workbook):
    df = pd.DataFrame(gene_info, columns=['_id', 'identifier', 'type', 'gene_name'])
    with pd.ExcelWriter('Abstracts and full text.xlsx', engine='openpyxl', mode='a') as writer:
        writer.book = workbook
        writer.sheets = {ws.title: ws for ws in workbook.worksheets}
        df.to_excel(writer, sheet_name='fullT_Gene_Names', index=False, startrow=1, header=False)

modify_url()
```

**For Abstracts** gathering the gene names. The code organizes the gene names and helps collect all the unique names mentioned in each abstracts.
```python
import openpyxl
from openpyxl.styles import PatternFill

# Load the Excel workbook
file_path = 'Abstracts and full text.xlsx'
worksheet_name = 'AB_Gene_Names'  # Replace 'Sheet1' with the name of your worksheet
workbook = openpyxl.load_workbook(file_path)
worksheet = workbook[worksheet_name]

# Create an empty dictionary to store unique identifiers with gene names
unique_geneIDs = {}

# Iterate through the rows
for index, row in enumerate(worksheet.iter_rows(min_row=2, values_only=True), start=2):
    pmid = row[0]  # PMID is in the first column (column A)
    identifier = row[1]  # Identifier is in the second column (column B)
    gene_name = row[3]  # Gene Name is in the fourth column (column D)

    # Combine PMID and Identifier to create a unique identifier key to dictionary
    unique_identifier = f"{pmid}_{identifier}"

    # Check if the unique identifier is already in the dictionary
    if unique_identifier not in unique_geneIDs:
        unique_geneIDs[unique_identifier] = [gene_name.upper()]  # Initialize a list with the capitalized gene name
    else:
        # If the key exists, append the capitalized gene name to the existing list
        unique_geneIDs[unique_identifier].append(gene_name.upper())

    # Highlight the current row with yellow fill color
    for cell in worksheet[index]:
        cell.fill = PatternFill(start_color='FFFF00', end_color='FFFF00', fill_type='solid')

# Sort the gene names within each dictionary section
for identifier, gene_names in unique_geneIDs.items():
    unique_geneIDs[identifier] = sorted(set(gene_names), key=lambda x: (len(x), x))

# Display the unique identifiers with their corresponding gene names
for identifier, gene_names in unique_geneIDs.items():
    print(f"Unique Identifier: {identifier}, Gene Names: {', '.join(gene_names)}")
    
# Save the modified workbook (overwriting the original file)
workbook.save(file_path)

# Close the workbook
workbook.close()
```
To make sure that the unique_identifiers dictionary contains information.
```python
print(unique_identifiers)
```

**For Full-Text** gathering the gene names. The code organizes the gene names and helps collect all the unique names mentioned in each full-text article.
```python
import openpyxl
from openpyxl.styles import PatternFill

# Load the Excel workbook
file_path = 'Abstracts and full text.xlsx'
worksheet_name = 'fullT_Gene_Names'  # Replace 'Sheet1' with the name of your worksheet
workbook = openpyxl.load_workbook(file_path)
worksheet = workbook[worksheet_name]

# Create an empty dictionary to store unique identifiers with gene names
unique_geneIDs_2 = {}

# Iterate through the rows
for index, row in enumerate(worksheet.iter_rows(min_row=2, values_only=True), start=2):
    pmid_FT = row[0]  # PMID is in the first column (column A)
    identifier_FT = row[1]  # Identifier is in the second column (column B)
    gene_name_FT = row[3]  # Gene Name is in the fourth column (column D)

    # Combine PMID and Identifier to create a unique identifier key
    unique_identifier = f"{pmid_FT}_{identifier_FT}"

    # Check if the unique identifier is already in the dictionary
    if unique_identifier not in unique_geneIDs_2:
        unique_geneIDs_2[unique_identifier] = [gene_name_FT.upper()]  # Initialize a list with the capitalized gene name
    else:
        # If the key exists, append the capitalized gene name to the existing list
        unique_geneIDs_2[unique_identifier].append(gene_name_FT.upper())

    # Highlight the current row with blue fill color
    for cell in worksheet[index]:
        cell.fill = PatternFill(start_color='0000FF', end_color='0000FF', fill_type='solid')

# Sort the gene names within each dictionary section
for identifier_FT, gene_names_FT in unique_geneIDs_2.items():
    unique_geneIDs_2[identifier_FT] = sorted(set(gene_names_FT), key=lambda x: (len(x), x))

# Display the unique identifiers with their corresponding gene names
for identifier_FT, gene_names_FT in unique_geneIDs_2.items():
    print(f"Unique Identifier: {identifier_FT}, Gene Names: {', '.join(gene_names_FT)}")

# Save the modified workbook (overwriting the original file)
workbook.save(file_path)

# Close the workbook
workbook.close()
```

To make sure that the unique_geneIDs_2 dictionary contains information.
```python
print(unique_geneIDs_2)
```

### Placing Gene Names into Lists
Placing the gathered information from the steps above into lists, so the data could be analyzed.
```python
# Abstracts List
ab_geneNames = [next(iter(gene_name), None) for gene_name in unique_geneIDs.values()]
print(ab_geneNames)

print()

# Full-Text List
ft_geneNames = [next(iter(gene_name), None) for gene_name in unique_geneIDs_2.values()]

print(ft_geneNames)

# Gene names in total (Abstract + Full-text)
geneNames_TOTAL = ab_geneNames + ft_geneNames
```
Testing to make sure that the total list contains all the information from both the abstracts and full-text.
```python
# checking the lengths of the lists
print("length of abstracts list:", len(ab_geneNames))
print("Length of full-text list:", len(ft_geneNames))
print()
print("Do the numbers of total match to the combinination of the abstacts and full-text: ", (len(ab_geneNames) + len(ft_geneNames)) == len(geneNames_TOTAL))
print()
print("total gene names length:", len(geneNames_TOTAL))
print(geneNames_TOTAL)
```

### Analyzing the Data
In this subsection is the code that created the tables, bar graphs and word clouds.

#### Frequency Tables

**For Abstracts**

The complete table.
```python
# Full Frequency Table for Abstracts
import pandas as pd

# Create a DataFrame and count number of times of each gene name
ab_df = pd.DataFrame({'Gene Names': ab_geneNames})
ab_freq_table = ab_df['Gene Names'].value_counts().reset_index()
ab_freq_table.columns = ['Gene Names', 'Frequency']

# Display the frequency table
pd.set_option('display.max_rows', None)
print(ab_freq_table)
```

The top 10 table.
```python
# Top 10 Frequency Table for Abstracts
top_10 = 10
top_ab_geneNames = ab_freq_table.head(top_10)
print(top_ab_geneNames)
```

Looking at how many gene names frequency is 1.
```python
# Number of Frequencies that are unique (only have 1) for Full-text
gene_freq1_Abstract = ab_freq_table[ab_freq_table['Frequency'] == 1]
num_geneFreq1_Abstract = len(gene_freq1_Abstract)
print(num_geneFreq1_Abstract)
```

**For Full-Text**

The complete table.
```python
# Full Frequency Table of Full Text
ft_df = pd.DataFrame({'Gene Names': ft_geneNames})
ft_freq_table = ft_df['Gene Names'].value_counts().reset_index()
ft_freq_table.columns = ['Gene Names', 'Frequency']

# Display the frequency table
pd.set_option('display.max_rows', None)
print(ft_freq_table)
```

The top 10 table.
```python
# Top 10 frequency table for Full text
top_ten = 10
top_ft_geneNames = ft_freq_table.head(top_ten)
print(top_ft_geneNames)
```

Looking at how many gene names frequency is 1.
```python
# Number of Frequencies that are unique (only have 1) for Full-text
gene_freq1_FullText = ft_freq_table[ft_freq_table['Frequency'] == 1]
num_geneFreq1_FullText = len(gene_freq1_FullText)
print(num_geneFreq1_FullText)
```

**For Total (abstract and full-text)**

The complete table.
```python
# Full Frequency Table for Total Amount of Gene Names
TOTAL_df = pd.DataFrame({'Gene Names': geneNames_TOTAL})
TOTAL_freq_table = TOTAL_df['Gene Names'].value_counts().reset_index()
TOTAL_freq_table.columns = ['Gene Names', 'Frequency']

# Display the frequency table
pd.set_option('display.max_rows', None)
print(TOTAL_freq_table)
```

The top 10 table.
```python
# Top 10 Gene Names for TOTAL
top_ten = 10
top_TOTAL_geneNames = TOTAL_freq_table.head(top_ten)
print(top_TOTAL_geneNames)
```

Bottom 10 table.
```python
# least frequent for TOTAL
totalGeneName = len(TOTAL_freq_table)

# The number of genes you want to retrieve
bottom_ten = 10

# calculate the stating index
start_index = max(0, totalGeneName - bottom_ten)

# Output the bottom ten
bottomTOTAL_geneNames = TOTAL_freq_table.tail(totalGeneName-start_index)
print(bottomTOTAL_geneNames)
```

Looking at how many gene names frequency is 1.
```python
# Number of Frequencies that are unique (only have 1) for TOTAL
gene_freq1 = TOTAL_freq_table[TOTAL_freq_table['Frequency'] == 1]
num_geneFreq1 = len(gene_freq1)
print(num_geneFreq1)
```

#### Bar Graphs

**For Abstracts**
```python
# Top Ten Abstracts
import matplotlib.pyplot as plt
import random

# Generate random colors for each bar
num_bars = len(top_ab_geneNames)
random_colors = ['#' + '%06X' % random.randint(0, 0xFFFFFF) for _ in range(num_bars)]

# Plotting the bar graph
plt.figure(figsize=(8, 8))
plt.bar(top_ab_geneNames['Gene Names'], top_ab_geneNames['Frequency'], color=random_colors)
plt.xlabel('Gene Names')
plt.ylabel('Frequency')
plt.title('Top 10 Abstracts: Gene Names Frequency')
plt.xticks(rotation=90)
plt.tight_layout()
plt.show()
```

**For Full-Text**
```python
# Top Ten Full Abstracts
import matplotlib.pyplot as plt

# Plotting the bar graph
plt.figure(figsize=(8, 8))
plt.bar(top_ft_geneNames['Gene Names'], top_ft_geneNames['Frequency'], color=random_colors)
plt.xlabel('Gene Names')
plt.ylabel('Frequency')
plt.title('Top 10 Full-Text: Gene Names Frequency')
plt.xticks(rotation=90)
plt.tight_layout()
plt.show()
```

**For Total Gene Names**
```python
# Top Ten Total Gene Names
import matplotlib.pyplot as plt

# Plotting the bar graph
plt.figure(figsize=(8, 8))
plt.bar(top_TOTAL_geneNames['Gene Names'], top_TOTAL_geneNames['Frequency'], color=random_colors)
plt.xlabel('Gene Names')
plt.ylabel('Frequency')
plt.title('Top 10 TOTAL: Gene Names Frequency')
plt.xticks(rotation=90)
plt.tight_layout()
plt.show()
```

#### Word Clouds

**For Abstracts**
```python
# Abstracts
from wordcloud import WordCloud

all_ab_geneNames = ' '.join(filter(None, ab_geneNames))

ab_wordcloud = WordCloud(width=800, height=400, background_color='white').generate(all_ab_geneNames)

plt.figure(figsize=(10,8))
plt.imshow(ab_wordcloud, interpolation='bilinear')
plt.axis('off')
plt.title('Abstract Word Cloud of Gene Names')
plt.show()
```

**For Full-Text**
```python
# Full Text
from wordcloud import WordCloud

all_ft_geneNames = ' '.join(filter(None, ft_geneNames))

ft_wordcloud = WordCloud(width=800, height=400, background_color='white').generate(all_ft_geneNames)

plt.figure(figsize=(10,8))
plt.imshow(ft_wordcloud, interpolation='bilinear')
plt.axis('off')
plt.title('Full Text Word Cloud of Gene Names')
plt.show()
```

**For Total Gene Names**
```python
# Total
from wordcloud import WordCloud

all_geneNames_TOTAL = ' '.join(filter(None, geneNames_TOTAL))

geneNames_TOTAL_wordcloud = WordCloud(width=800, height=400, background_color='white').generate(all_geneNames_TOTAL)

plt.figure(figsize=(10,8))
plt.imshow(geneNames_TOTAL_wordcloud, interpolation='bilinear')
plt.axis('off')
plt.title('Overall Total of Gene Names')
plt.show()
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

> [10]	National Center for Biotechnology Information. “BRAF B-Raf proto-oncogene, serine/threonine kinase [ Homo sapiens (human)],” Accessed: Dec. 05, 2023. [Online]. Available: https://www.ncbi.nlm.nih.gov/gene/673#summary

> [10a] National Center for Biotechnology Information. “MGMT O-6-methylguanine-DNA methyltransferase [ Homo sapiens (human)],” Accessed: Dec. 05, 2023. [Online]. Available: https://www.ncbi.nlm.nih.gov/gene/673#summaryhttps://www.ncbi.nlm.nih.gov/gene/4255

> [11]	M. Zhao, P. Kim, R. Mitra, J. Zhao, and Z. Zhao, “TSGene 2.0: an updated literature-based knowledgebase for tumor suppressor genes,” Nucleic Acids Res., vol. 44, no. D1, pp. D1023–D1031, Jan. 2016, doi: 10.1093/nar/gkv1268.

> [12]	Y. Liu, M. Luo, Z. Jin, M. Zhao, and H. Qu, “dbLGL: an online leukemia gene and literature database for the retrospective comparison of adult and childhood leukemia genetics with literature evidence,” Database, vol. 2018, p. bay062, Jan. 2018, doi: 10.1093/database/bay062.