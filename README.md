## Design and Implementation of LangChain Expression Language (LCEL) Expressions

### AIM:
To design and implement a LangChain Expression Language (LCEL) expression that utilizes at least two prompt parameters and three key components (prompt, model, and output parser), and to evaluate its functionality by analyzing relevant examples of its application in real-world scenarios.

### PROBLEM STATEMENT:
Develop an LCEL-based application to process expressions with dynamic parameters, leveraging a prompt template for structured interaction, a language model to process the input, and an output parser for extracting meaningful results.
### DESIGN STEPS:
#### STEP 1:
 Create a prompt template with placeholders for at least two parameters.

#### STEP 2:
 Use LangChain's language model to process the prompt and generate a response.

#### STEP 3:
Implement an output parser to extract structured results from the model's response.
### PROGRAM:
## Name: Kanigavel M
## Reg.no: 212224240070
~~~
import os
import openai

from dotenv import load_dotenv, find_dotenv
_ = load_dotenv(find_dotenv()) # read local .env file
openai.api_key = os.environ['OPENAI_API_KEY']
~~~
~~~
#!pip install pydantic==1.10.8
~~~
~~~
from langchain.prompts import ChatPromptTemplate
from langchain.chat_models import ChatOpenAI
from langchain.schema.output_parser import StrOutputParser
~~~
~~~
prompt = ChatPromptTemplate.from_template(
    "tell me a short joke about {topic}"
)
model = ChatOpenAI()
output_parser = StrOutputParser()
~~~
~~~
chain = prompt | model | output_parser
~~~
~~~
chain.invoke({"topic": "Machine learning"})
~~~

### OUTPUT:
<img width="1373" height="693" alt="image" src="https://github.com/user-attachments/assets/f2c05da2-9117-4c4c-ae4e-09ae877f2478" />

### RESULT:
Hence,the program to design and implement a LangChain Expression Language (LCEL) expression that utilizes at least two prompt parameters and three key components (prompt, model, and output parser), and to evaluate its functionality by analyzing relevant examples of its application in real-world scenarios is written and successfully execute
