# *Databricks Labs CI/CD Templates*: Automated Databricks CI/CD pipeline creation and deployment

[![asciicast](https://asciinema.org/a/yltp4nutLlqUSQJJF6NnzTq9s.svg)](https://asciinema.org/a/yltp4nutLlqUSQJJF6NnzTq9s)


Short instructions: 
1) Install [Cookiecutter](https://github.com/cookiecutter/cookiecutter) and dependencies from requirements.txt
2) `cookiecutter git@github.com:databrickslabs/cicd-templates.git` (or the HTTPS equivalent)
3) Create new GitHub repo and push created project files there
4) Add `DATABRICKS_HOST` and `DATABRICKS_TOKEN` as Github secrets to the newly created repo
5) Implement DEV tests in dev-tests folder. These pipelines will be run on every push
6) Implement Integration Test pipelines in folder integration-test. These pipelines will be used for testing of new release
7) Implement production pipelines in pipeline folder. 

Please note:
1)Python 3.8 is not supported yet

Project Organization
------------
```bash
├── deployment
│   ├── __init__.py
│   ├── deployment.py
│   ├── dev_cicd_pipeline.py
│   └── release_cicd_pipeline.py
├── deployment.yaml
├── dev-tests
│   ├── pipeline1
│   │   ├── job_spec_aws.json
│   │   ├── job_spec_azure.json
│   │   └── pipeline_runner.py
│   └── pipeline2
│       ├── job_spec_aws.json
│       ├── job_spec_azure.json
│       └── pipeline_runner.py
├── docs
│   ├── Makefile
│   ├── commands.rst
│   ├── conf.py
│   ├── getting-started.rst
│   ├── index.rst
│   └── make.bat
├── integration-tests
│   ├── pipeline1
│   │   ├── job_spec_aws.json
│   │   ├── job_spec_azure.json
│   │   └── pipeline_runner.py
│   └── pipeline2
│       ├── job_spec_aws.json
│       ├── job_spec_azure.json
│       └── pipeline_runner.py
├── mlflow_deployments_sample_project
│   ├── __init__.py
│   ├── data
│   │   ├── __init__.py
│   │   └── make_dataset.py
│   ├── features
│   │   ├── __init__.py
│   │   └── build_features.py
│   ├── models
│   │   ├── __init__.py
│   │   ├── predict_model.py
│   │   └── train_model.py
│   └── visualization
│       ├── __init__.py
│       └── visualize.py
├── notebooks
├── pipelines
│   ├── pipeline1
│   │   ├── job_spec_aws.json
│   │   ├── job_spec_azure.json
│   │   └── pipeline_runner.py
│   └── pipeline2
│       ├── job_spec_aws.json
│       ├── job_spec_azure.json
│       └── pipeline_runner.py
├── requirements.txt
├── runtime_requirements.txt
├── setup.py
└── tests
    └── test_smth.py

18 directories, 43 files
```
--------
