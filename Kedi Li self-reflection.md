# Kedi Li self-reflection

I am Kedi Li. I am responsible for data preprocessing and PPT making. Even though I did not step much into machine learning, I contributed some of my ideas to our group, and in this project I understood the official coding methodology, including preprocessing, EDA, data splitting, and model selection processes.

In data preprocessing at the very beginning, combining all the data into the same file might not be necessary, because combined data can be extremely large, which cannot be viewed in Excel if the number of rows is larger than 10,000 thousand. More than that, if the datasets are in the same period of time, combination can lead to overlap of dates, which may cause failure of modelling, as time series is an important feature in the process of machine learning.

In the data splitting process, we should compare the autocorrelation between different assemblies, using the data that has higher autocorrelation as training material, and using the one that has weaker correlation as a reference for machine learning.

In collaboration, it is relatively hard for people to work on the same code. Therefore, GitHub becomes incomparably important. When we are dealing with machine learning, tons of data and code are going to be produced. Without proper management of format and documentation, it is impossible for other users to reproduce the results according to the given code and program. Meanwhile, naming is one of the most important tasks when we merge the code that we have written. The files are going to mix with each other, and proper naming can help our partners distinguish their own work.

At the end, this experience gave me a brief view of how people collaborate with each other in the same programming project, and also helped me understand how data scientists, game makers, and program developers work remotely. More than that, it also helped me to clarify the general workflow for developing a model or analysis.
