

 ## SnowSQL Streamline

 To facilitate effective collaboration and streamline the development process, we utilized the Snowpark Python guide and the associated GitHub repository for data engineering with Snowpark. The implementation involves a minimum of three SQL processes and three User Defined Functions, leveraging two or all three datasets in the queries. Additionally, the project integrates Git actions for deployment purposes, following a continuous integration and continuous deployment (CI/CD) approach. A custom chatbot is being created using streamlit and deployed to GCP to assist users with table specific queries using natural language.


# Links

- LiveApp - http://34.75.29.161:8501


# Project Tree

```
📦 
├─ .DS_Store
├─ .devcontainer
│  └─ config
├─ .github
│  └─ workflows
│     └─ build_and_deploy.yaml
├─ .gitignore
├─ AskMe.py
├─ Pipfile
├─ Pipfile.lock
├─ README.md
├─ deploy_covid_pipelines.py
├─ image.jpg
├─ pages
│  └─ 1_ViewData.py
├─ requirements.txt
├─ snowflake
│  ├─ .DS_Store
│  ├─ 01_setup_snowflake.sql
│  ├─ 02_load_coviddata.sql
│  ├─ 05_create_view_one.py
│  ├─ Data_transformation
│  │  ├─ covid_vaccinations
│  │  │  ├─ 01_loading_covid_vaccinations.sql
│  │  │  └─ 02_transforming_covid_vaccinations.sql
│  │  ├─ retail_data
│  │  │  ├─ 01_loading_retail_data.sql
│  │  │  └─ 02_transforming_retail_data.sql
│  │  └─ who_situation_reports
│  │     ├─ 01_cleaning_who_situation_reports.sql
│  │     └─ 02_transforming_who_situation_reports.sql
│  ├─ Pipfile
│  ├─ Pipfile.lock
│  ├─ SQL_Processes
│  │  ├─ 01_test.sql
│  │  ├─ 02_test.sql
│  │  ├─ 03_test.sql
│  │  └─ 04_test.sql
│  ├─ User_Defined_Functions
│  │  ├─ Mortality
│  │  │  ├─ .gitignore
│  │  │  ├─ app.py
│  │  │  ├─ app.sql
│  │  │  └─ app.toml
│  │  ├─ Normalized_Sales
│  │  │  ├─ .gitignore
│  │  │  ├─ app.py
│  │  │  ├─ app.sql
│  │  │  └─ app.toml
│  │  └─ Vaccinations
│  │     ├─ .gitignore
│  │     ├─ app.py
│  │     ├─ app.sql
│  │     └─ app.toml
│  ├─ requirements.txt
│  └─ teardown.sql
└─ utils
   ├─ __init__.py
   └─ snowpark_utils.py
```

# Environment Variables

```
#Openai
OPENAI_API="Your_Secret_Key"

# Snowflake 
SNOWFLAKE_ACCOUNT=""
SNOWFLAKE_USER=""
SNOWFLAKE_PASSWORD=""
SNOWFLAKE_ROLE=""
SNOWFLAKE_DATABASE="HOL_DB1"
SNOWFLAKE_TABLE1="COVID_WORLDWIDE"
SNOWFLAKE_TABLE2="COVID_VACCINES"
SNOWFLAKE_TABLE3="RETAIL_DATA"
```

# Create virtual environment for streamlit

### Install virtualenv if you haven't already
```
pip install virtualenv
```

### Create a virtual environment
```
virtualenv myenv
```

### Create python environment for the directory
```
python -m venv myenv
```

### Activate the virtual environment
```
source myenv/bin/activate
```

### Pip install requirements
```
pip install -r requirements.txt
```

# Streamlit Installation & Activation

```
$ mkdir streamlit

$ cd streamlit 

$ mkdir .streamlit

$ python -m venv .streamlit 

$ source .streamlit/bin/activate

$ cd ..
```

### Run streamlit application
```
streamlit run AskMe.py
```

# ATTESTATION:

I ATTEST THAT I HAVEN’T USED ANY OTHER STUDENTS’ WORK IN MY ASSIGNMENT AND ABIDE BY THE POLICIES LISTED IN THE STUDENT HANDBOOK.