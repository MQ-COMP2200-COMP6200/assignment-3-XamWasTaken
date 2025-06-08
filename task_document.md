## Task Document

Here is the written answers for the tasks 


### Task 1 - (1.5 Marks)
Within the context of this Data Scientist's Notebook, the <u>Eigenvector centrality</u> value outlines a person who is not just well-connected but connected to other well-connected individuals or companies. 

In this dataset, a high eigenvector centrality is likely influential in the network, sitting on many boards or highly connected amongst companies. A lower eigenvector score shows the opposite, a director with little influence or connections to other board members or companies.

The <u>Degree centrality</u> stat counts the number of direct links a node has. 

A high degree centrality for a director means they sit on the boards of many companies. Such individuals may not be connected to powerful nodes, but their broad reach suggests operational or advisory influence across many firms, which is relevant for identifying social or versatile professionals.

A new measurement we've added is:

<b> Betweenness centrality. </b>

This measurement measures the amount of times a node lies on the shortest path between other nodes. In the context of the data, a high betweenness measure tells us an individual may serve as a connector or bridge between two or more disconnected groups or individuals. 

A further extrapolation would be that using this measurement could result in finding individuals who are highly involved in the flow of communication or information between firms.

This aligns with our project goals because individuals with high eigenvector, degree and betweenness scores might hold sway over major business decisions or industry-wide strategies.

### Task 2 - (8 Marks)
Task 2 changes are viewable in the "directos-network.ipynb" file.

<b> Code Adjustment 1 </b>

Seen in the second block of code, the most_common function originally did not account for the edge case of both genders having equal totals, and would simply return the first name in the array. With adjustments it now accounts for this and returns 'Multiple' if this edge case was met. This avoids misleading information being trusted and reflects higher quality of product for the team behind the file.

<b> Code Adjustment 2 </b>

Seen in the fifth block, the director plot was entirely unlabelled and had zero descriptions used to showcase the data. Added code with labelling has made the graph far more meaningful and better showcases why it is being displayed. 

<b> Code Adjustment 3 </b>

Seen in the eighth  block. the biggest_connected_graph variable originally grabbed the first value in the array which won't always necessarily be the most connected component. Code adjustment was made to ensure the largest value is always picked using max().

<b> Code Adjustment 4 </b>

Seen in the tenth block. the people_df dataframe is merged with the pandas default 'inner' merge, which requires both dataframes to have data to complete the merge, if one of the dataframe cells is empty,both rows are dropped which can sliently delete important data. Adjusted code is shown to make the dataframe a left merge, only dropping if demographic info is missing, not if the centrality data is missin (it also see the records that are incomplete with this merge). A check is made afterwards to warn if there was some data dropped/missing.

<b> Why these four changes </b>

These four changes were chosen as they seemed to greatly affect the data seen in the document and added real value to the analysis. Other options like better documenting the code used were less important than cutting out the reduction of important data, covering edge cases and better describing graphs shown. 

### Task 3 - (0.5 Marks)

The software_background data point is transformed very early in the code (from string 'f' and 't's into boolean), but is never used to showcase or extrapolate any data or result. Directors with a software background could be compared to many other statistics to learn about this application. For example do they form clusters with other directors with a strong software background? Are they paid more or less than other directors? 

This metric is very underused and could be added to the analysis to better understand differences in directors and their backgrounds.

### Task 4 - (2 Marks)

Attached to the repository is a document that outlines a large list of companies with measurements including their revenue growth, employees and headquarters. This could be compared to both collections of data where we could investigate what directors have worked in what big US companies and to what success (For example, the attached document has records relating to pepsico, nike, johnson & johnson and others). 

This could give us a greater outlook on influential directors and investors in this market to find out who has had greater impact and give us a more confident judgement of who is better equipped to widen the company's connections.

### Task 5 - (8 Marks)

#### Chosen Options

OPTION A: <u>Improve the data visualisations and turn this into a presentation that you could give to a non-technical audience.</u>

OPTION C: <u>Write up your take on the ethics of this project.</u>


### Option A - Presentation
Included in <i>directors-network.ipynb</i> are four new visualisations to help with the short presentation.

#### Figure 1

To begin the presentation we highlight the top 13 directors with the highest eigenvector scores, there are two main points to bring up with this figure, all of their eigenvector scores are approximately equal and the choice of showcasing the top 13 is an odd number to choose from. We show this graph as a point of question that will be answered in future graphs. 

#### Figure 2

Figure 2 does not display much differently than figure 1, investigating the same question we see all our directors fall under two distinct points along the X-Axis. This suggests that the eigenvector scores for all directors really only fit into two separate categories which we will investigate in future figures. 

#### Figure 3

To investigate the two questions that figure 1 outlined for us we made a bar chart that shows the groupings of all directors into 4 succinct bins. It becomes more clear now as almost all directors fall into a bin that holds incredibly small eigenvector centrality measurements whilst there is no directors in the two middle bins, and a very small few in the top bin. This shows us how skewed our data is, with only a few directors having a non-almost-zero eigenvector score. Included under this bar graph is a printed data point that tells us that there are exactly 13 directors who fall under the top bin.

This is why we chose to showcase the names of the top 13 as it appears they are the only directors with meaningful eigenvector centrality values. 

#### Figure 4

Moving on to a different point of interest. This figure displays the comparison of directors' age to their compensation via a DBSSCAN. It has added labelling to the Y-Axis to better understand the compensation these directors are receiving at different brackets. Almost all data is well balanced about ages 55-70 meaning the average age of the very wealthy directors is quite high and most make over 6 figures but below 7 in compensation.

#### Figure 5

This figure better shows the compensation difference between the genders. With a fairly even distribution for each gender, it is important to note the interquartile range for women has a slightly higher band than the men, but the men have far more outliers on the upper range or fourth quartile than the women.

#### Figure 6

Figure 6 has been used previously in the document and it shows us the distribution of the log compensation a director has plotted against the number of companies that they work for. At the bottom end we have a far higher compensation value, this could elude to a lack of data points at this amount of companies worked for, or that working for a lesser number of companies can result in a higher compensation, this might make sense as working at the same company for an extended period of time can net you higher positions in that company and thus greater compensation in the long run.

Past this lower number, the compensation jumps around mostly unevenly with the lowest points being seen at 5 and 14 companies worked for, its most likely a lack of data points for the high end of x-values showcasing only a minor change in compensation compared to the middle values but the middle end would have a safe amount of data points to hold this information as verifiable.

#### Figure 7

Finally, figure 7 outlines the impact that our measurement values actually have when mapped against a director's compensation. According to this mapping it appears the eigenvector centrality measurement is the only significant measurement that can accurately predict a directors' compensation. 

### Option C - Ethics

The ethics of this project are complicated but once broken down it can be clear how contraversial the data collection is.