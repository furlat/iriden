
The general idea for the project Polar Space is to have easy to host workspace that can be interacted with via API that is able to host a set of polar frames and their disk representation in parquet and arbitrarily visualize the polar frame and apply expressions for them or operations in between them.

The computing stack is composed by Polars for the data frames, FastAPI for serving the data frames and GreatTables for converting the data frames into HTML code.  
Ideally the user would authenticate to the web app and would have access to a workspace with the available parquet, would be able to upload new Parquet files and then would be able to load those parquet files, probably would be able to have the possibility to associate a polar schema to those parquet files to ease up the loading. Under a first approximation, the first capability that the user should be able to do would be to visualize part of the frame. Visualizing part of the frame means combining the select context and the column selector in Polars with the slice operator to select only the columns and rows that we are interested in. And probably it would be nice to simulate the possibility to scroll down or up calling the slice operator and consequently the table representation. 

In a second degree it would be nice to have access to a text block that allows to define polar expressions. Probably at the beginning it would be better not to allow any polar expression, but to have something like a drop-down menu that allows to select the context of the expression and the frame over which the expression is applied, and then only a single step and the content of the expression, that is going to be a string that then gets parsed and executed. It is important to notice that it would be really nice to be able to select whether the expression would result in a new data frame, which is the default polar behavior, not to have any place operation, or whether we want to simulate an in-place operation by overwriting the previous data frame with the current one. In general, I think we want to always be able to allow to give the possibility to a user to go back in time and cancel the effect of the operation. This could come with some memory costs, or time costs in terms of saving to disk the data, but I think it would be a very nice functionality for exploratory data, interactive exploratory data. 

In third degree it would be very nice to be able to apply frame operations to the frame that are in the workspace. So operations like concatenation or join between the frames are an example. 

Fourth, we should be able to apply complex sequences of expressions preferentially through the utilization of lazy frame and lazy expressions, such that we are not constraining ourselves to a single context or a single operation. 

I think the last two most interesting final steps would be: fifth, allowing the user to visualize data not only through grade tables but through a plotting library and fifth, would be to allow the user to specify expressions and probably use expressions leading to visualizations using natural language with a language model under the hood that is able to translate to polar expression. 


format in markdown the text above





