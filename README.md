# DataScience Final Project
Final project for Advanced Data Science (CSCI 4022). We are attempting to use K-means clustering to reconstruct the eras of Major League Baseball from historic team data.

### Problem Proposal
  Professional baseball in the US has been around for over a century. Although the rules have hardly changed since the early days of unathletic, cigar-smoking players, the style of play has transformed tremendously. Many modern baseball fans break up professional baseball into 6 to 7 different eras: the 19th century, the deadball era, the live-ball era, the integration era, the expansion era, the free agent era, and the long-ball era (sometimes broken up into the steroid era and then the long-ball era). These different time periods are characterized by different styles of play. For example, the deadball era saw very little home runs, or even runs scored in general. The long-ball era, however, saw a huge increase in home-run rates. We would like to cluster this data to see if, using a computational technique, we can derive these eras from raw data. It would also be interesting to see which modern teams get clustered into older eras, or vice-versa. Creating these clusters could help compare teams across eras and time periods, and allow analysis to be better informed when talking about changes in the game.

  The dataset we are using comes from the Lahman Database. This dataset contains comma-separated files of many general batting, pitching, and overall team statistics. For example, the ‘batting.csv’ file has a row for every single player’s season since 1871 through the 2018 season. It contains statistics such as runs, hits, at-bats, plate appearances, etc. Using these basic statistics, we can calculate even more advanced, modern statistics. Overall, this dataset contains 27 different files categorized by various themes. However, most of these will not be relevant to us, like all-star appearances, college playing, and managers. Using this dataset, we will be able to look at team statistics for any team since 1871, and also average over all players in the league in a given year.
  
  To support our motivating question, we would like to use various clustering strategies to produce classifications of baseball eras. By taking data from all of baseball history and choosing several key features to analyze, we hope to correctly cluster each team (by year) into an era. The first technique which comes to mind is K-means clustering. By taking features such as run scoring frequency, home run rates, innings pitched per pitcher, and various other common baseball statistics, we hope to create some sort of similarity metric to be able to group these teams together.
  
### Qualitative Results  
  Although we attempted to create clusters using both k-means clustering and Gaussian mixture models, both methods failed to create meaningful era clusters. Most clusters were made up of teams that spanned many years, making them mostly indistinguishable from other clusters. Ideally, we would have seen clusters of teams from years that largely do not overlap with other clusters.  
  
  Teams from the deadball era did get clustered together somewhat more effectively than other teams, though. We believe this is due to the fact that the deadball era is one of the only time periods characterised specifically by performance and style of play. We could see a significant dip in hits and power in that era, which was captured nicely by our dataset. Other eras, though, were created along more historical boundaries. The integration era, for example, is defined by ending segregation in professional baseball, which was not directly apparent in our feature-set. 
