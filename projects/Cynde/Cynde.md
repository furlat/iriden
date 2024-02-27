
Cynde is a project that aims to simplify working with large language models (LLMs), embeddings, and traditional data science tasks by addressing common challenges faced in this field. The main issues addressed include handling state, efficiently parallelizing operations, validating LLM outputs, choosing the best embedding or prompt structure, and managing complex data structures.

Cynde utilizes [[Polars]] as an efficient in-memory data structure for medium to large datasets, which also acts as an orchestrator for multi-threaded operations over the data. The project focuses on working with string data by leveraging two core operators: embedders (encoder language transformer models) and language models that map strings to vectors and other strings, respectively.

To handle structured objects or entities represented as JSON strings, Cynde integrates [[Pydantic]] for validating models and defining custom validation logic using Python type hints. This ensures safety and stability in the entity-based system. Additionally, packages like Instructure or Outlines are used to control the sampling process of language models, ensuring that they output strings with a specific structure defined by JSON templates provided by users.

Cynde extends machine learning capabilities by mapping data columns in Polars containing string values to categories through predictive models and embeddings, as well as using LLMs for structured extraction of information from text. This allows for the conversion of strings into new Pydantic objects or categories based on user-defined validation rules.

In summary, Cynde aims to streamline working with large language models by addressing common challenges in data handling and processing, while also integrating traditional machine learning techniques for string data manipulation and categorization. The project's focus on efficient parallelization, state management, and predictive model-based validation ensures a robust and scalable solution for modern data science tasks involving LLMs and embeddings.


