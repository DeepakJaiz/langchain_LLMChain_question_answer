# langchain_LLMChain_question_answer
### Aim 
**LLM Chain** :- Chains allow us to combine multiple components together to create a single, coherent application. For example, we can create a chain that takes user input, formats it with a PromptTemplate, and then passes the formatted response to an LLM. We can build more complex chains by combining multiple chains together, or by combining chains with other components.<br/>
**Different ways of calling chains** 
- By default, __call__ returns both the input and output key values. You can configure it to only return output key values by setting return_only_outputs to True.
- you can use run method. Note that run outputs a string instead of a dictionary.
- generate is similar to apply, except it return an LLMResult instead of string. LLMResult often contains useful generation such as token usages and finish reason.
- predict is similar to run method except that the input keys are specified as keyword arguments instead of a Python dict.

**Question Answer** :- In this we make question answer on our document nd check the answer.<br/>
- **Stuff** :- Stuffing is the simplest method, whereby you simply stuff all the related data into the prompt as context to pass to the language model.
- **Map Reduce** :- This method involves running an initial prompt on each chunk of data (for summarization tasks, this could be a summary of that chunk; for question-answering tasks, it could be an answer based solely on that chunk). Then a different prompt is run to combine all the initial outputs.
- **Refine** :- This method involves running an initial prompt on the first chunk of data, generating some output. For the remaining documents, that output is passed in, along with the next document, asking the LLM to refine the output based on the new document.
- **Map-Rerank** :- This method involves running an initial prompt on each chunk of data, that not only tries to complete a task but also gives a score for how certain it is in its answer. The responses are then ranked according to this score, and the highest score is returned.



### Reference
LLM Chain :- https://python.langchain.com/en/latest/modules/chains/generic/llm_chain.html <br/>
Question Answer Chain :- https://python.langchain.com/en/latest/modules/chains/index_examples/question_answering.html

### Prerequiste
You required Phython in your system fyou can follow this (https://www.python.org)<br/>
OpenAi API key required to get you can follow this link (https://platform.openai.com/account/api-keys)<br/>
Install Jupyter Notebook to run the code

### Modules required
`pip install langchain`<br/>
`pip install chromadb`<br/>

How to run
Open above file in Jupyter Notebook and select the cell from top one by one and click run to run the code.
