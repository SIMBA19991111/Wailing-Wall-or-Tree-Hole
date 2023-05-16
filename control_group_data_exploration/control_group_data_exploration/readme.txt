###########Content Structure
├── word_counts_csv         // folder , the word count of each category for each account.
├── images                        // folder ,output images
├── external                    // folder, store font files used in the visualization images
├── every_words_difference_csv // folder, all the selected tree-hole and wailing wall data for each account, sorted based on "difference" indicators  .
├── data_overview_csv // folder, store CSV files for stacked barcharts visualization
├── comments_every_account // folder, all comments (with category labels and corresponding word segmentation) of each account
├── Comments_All_Word_Clouds.ipynb   // Code, for displaying and generating a word cloud for the control group.
├── Comments Distribution Control Group.ipynb   // Compute the comments type count for the 11 control accounts, and generate a stacked bar chart.
├── Every_counts_words_flited.ipynb   // Extract the comments of the tree holes and wailing wall of the 11 accounts in the control group, filter them using certain rules [1], and generate the corresponding CSV.

[1]After multiple trial adjustments, we have set the following criteria: in the current data set, words count should greater than 10, and we rank each account's words in descending order based on the "Difference" indicator and select the top 75% of words for further exploration. This ensures the details of each account's words and controls the data volume, guaranteeing a manageable time for manual classification and exploration.

"Difference" Function
Difference = |['Wailing Wall'] - ['Tree Hole'] / (['Wailing Wall'] + ['Tree Hole']) * 100|

The calculation rule of the "Difference" index is as follows: "Difference" is a measure of the "purity/confidence" of a word. If a word exists in a certain sentence, the higher the purity of this word, the more likely this sentence belongs to either "tree hole" or "wailing wall".
