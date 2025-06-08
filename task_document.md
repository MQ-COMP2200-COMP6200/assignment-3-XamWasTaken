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

