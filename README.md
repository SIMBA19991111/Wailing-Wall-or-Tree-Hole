# **AIDM-7340**
## **Group Project**
**Wailing Wall or Tree Hole? An AI Exploration of Mourning Behaviors for the Deceased on Chinese Social Media - Taking Li Wenliang as an Example**

###  **Content Introduction**
```
│   Chinese-Words-Spllit-Comparison.ipynb
                //  Word Splitting for Control Group using ERNIE model. 
│   Chinese-Words-Spllit-Liwenliang.ipynb
                //  Word Splitting for Li Wenliang using ERNIE model. 
│   Comments_Select_Sample.ipynb
                //  Select representative comments context for text analysis.
│   Comparison_ModelClassification.ipynb
                //  Sequence classification task on control group using trained BERT model. 
│   DataVisualization_Liwenliang.ipynb
                //  Data Visualization for Li Wenliang.
│   LiwenliangSampling.ipynb
                // Sampling measurements for manual labeling Li Wenliang.
│   Liwenliang_BERT_torch_tree_hole.ipynb
                // BERT classification model establishment for Tree Hole.
│   Liwenliang_BERT_torch_whaling wall.ipynb
                // BERT classification model establishment for Wailing Wall.
│   Liwenliang_ModelClassification.ipynb
                // Model Classification procedure for Li Wenliang.
│   README.md
│   WeiboScraping.ipynb
                // Main scraping functions.
│   
├───dataset
│       codebook.csv
                // Distinctive words for identifying Li Wenliang comments' categories.
                // Divided by Wailing Wall, Tree Hole and Not Related.
                // Used in sequence tokenizer tasks.
│       codebook.txt
                // TXT version of the words without label for better tokenization. 
│       codebook_comparison.txt
                // Distinctive words for control group.
│       comparison_group.csv
                // Manual labelled comparison group.
│       comparison_group_codebook.csv
                // Comparison group's codebook.
│       LiwenliangAllWordscount.csv
                // Word counts after segment. 
│       LiwenliangComments_Split_sample.csv
                // Complete dataset with comments split and classification marked.
                // Due to the file storage limitation, here only provide examples on Github.
                // Please assest OneDrive link below to fetch complete dataset.
│       LiwenliangSampleAll.csv
                // Liwenliang sample results for manual labelling.
│       LiwenliangSample_Tree_Hole.csv
                // Liwenliang sample results for Tree Hole model training.
│       LiwenliangSample_Whailing_Wall.csv
                // Liwenliang sample results for Wailing Wall model training.
│       
├───external
│       Alibaba-PuHuiTi-Medium.ttf 
                //External font file for Wordcloud generation.
│       
├───images
│       Average Comments per User on Each Day by Category (Li Wenliang).png
│       Distinctive Wordcloud by Category.png
│       Distribution of Comments.png
│       Number of Comments and Average Comments Counts on Each Day (Li Wenliang).png
│       Number of Comments by Category on Each Day (Li Wenliang).png
│       Overall Trend of the Proportion of Comments by Category (Li Wenliang).png
│       Probability_Distribution_of_Comments.png
│       Ratio of Tree Hole Comments to Wailing Wall (Li Wenliang).png
│       Top 20 Commenters.png
│       Top 20 Single Users’ Comments Counts by Categories.png
│       Trend of Comments' Uniqueness Ratio.png
│       Wordcloud by Category.png
│       
└───model_save
    ├───tree_hole
    └───whailing_wall
    // Empty folders just for interpretation due to the storage limitation of Github.
    // Please assest OneDrive link below to fetch trained models.
```
### **Comparison Group Exploration**
```
├── word_counts_csv         
                // folder , the word count of each category for each account.
├── images                        
                // folder ,output images
├── external                    
                // folder, store font files used in the visualization images
├── every_words_difference_csv 
                // folder, all the selected tree-hole and wailing wall data for each account, sorted based on "difference" indicators  .
├── data_overview_csv 
                // folder, store CSV files for stacked barcharts visualization
├── comments_every_account 
                // folder, all comments (with category labels and corresponding word segmentation) of each account
├── Comments_All_Word_Clouds.ipynb   
                // Code, for displaying and generating a word cloud for the control group.
├── Comments Distribution Control Group.ipynb   
                // Compute the comments type count for the 11 control accounts, and generate a stacked bar chart.
├── Every_counts_words_flited.ipynb  
                 // Extract the comments of the tree holes and wailing wall of the 11 accounts in the control group, filter them using certain rules [1], and generate the corresponding CSV.

[1]After multiple trial adjustments, we have set the following criteria: in the current data set, words count should greater than 10, and we rank each account's words in descending order based on the "Difference" indicator and select the top 75% of words for further exploration. This ensures the details of each account's words and controls the data volume, guaranteeing a manageable time for manual classification and exploration.

"Difference" Function
Difference = |['Wailing Wall'] - ['Tree Hole'] / (['Wailing Wall'] + ['Tree Hole']) * 100|

The calculation rule of the "Difference" index is as follows: "Difference" is a measure of the "purity/confidence" of a word. If a word exists in a certain sentence, the higher the purity of this word, the more likely this sentence belongs to either "tree hole" or "wailing wall".
```

#### **OneDrive External Link for Big Files:**
(Including Models and Full Dataset)

https://1drv.ms/f/s!AmIVffcWFoDC2XVpcUQcAO4kuB7p?e=IKa18b