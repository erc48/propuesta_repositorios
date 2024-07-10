# propuesta_repositorios

## Infrastructura

```
infra/
├── ansible/
│   ├── group_vars/
│   │   ├── all/
│   │   │   └── vault.yml  
│   ├── roles/
│   │   ├── common/
│   │   │   ├── tasks/
│   │   │   │   └── main.yml  
│   │   ├── emd/
│   │   │   ├── tasks/
│   │   │   │   ├── main.yml  
│   │   │   │   ├── deploy.yml  
│   │   │   │   └── common.yml 
│   │   ├── odoo/
│   │   │   ├── tasks/
│   │   │   │   ├── main.yml  
│   │   │   │   ├── deploy.yml  
│   │   │   │   └── common.yml 
│   │   ├── jenkins/
│   │   │   ├── tasks/
│   │   │   │   ├── main.yml  
│   │   │   │   ├── deploy.yml  
│   │   │   │   └── common.yml 
│   │   ├── github_runners/
│   │   │   ├── tasks/
│   │   │   │   ├── main.yml
│   │   │   │   ├── deploy.yml 
│   │   │   │   └── common.yml 
│   ├── deploy_staging.yml  
│   ├── deploy_production.yml  
│   └── README.md  
├── emd/
│   ├── Dockerfile
│   ├── docker-compose.yml
│   ├── vars_staging.yml
│   ├── vars_production.yml  
│   ├── vault_staging.yml
│   ├── vault_prod.yml
│   └── README.md  
├── odoo/
│   ├── service1/
│   │   ├── entrypoint.sh
│   │   └── Dockerfile
│   ├── service2/
│   │   ├── entrypoint.sh
│   │   └── Dockerfile
│   ├── docker-compose.yml
│   ├── vars_staging.yml
│   ├── vars_production.yml  
│   ├── vault_staging.yml
│   ├── vault_prod.yml
│   └── README.md 
├── jenkins/
│   ├── master/
│   │   ├── jenkins.yaml
│   │   └── Dockerfile
│   ├── agents/
│   │   ├── linux/
│   │   │   └── Dockerfile
│   │   ├── windows/
│   │   │   └── Dockerfile
│   ├── docker-compose.yml
│   ├── vars_staging.yml
│   ├── vars_production.yml  
│   ├── vault_staging.yml
│   ├── vault_prod.yml
│   └── README.md  
└── github_runners/
    ├── linux/
    |   ├── entrypoint.sh
    │   └── Dockerfile
    ├── windows/
    |   ├── entrypoint.sh
    │   └── Dockerfile
    ├── docker-compose.yml
    ├── vars_staging.yml
    ├── vars_production.yml  
    ├── vault_staging.yml
    ├── vault_prod.yml  
    └── README.md  
```
    

## CI

```
sw_CI_Libs
├── README.md
├── .github
│   ├── workflows 
│   │   ├── sw_JOB_EMD_Check_Consistency_TRIGGER.yml
│   │   ├── sw_JOB_EMD_Post_Doc_TRIGGER.yml
│   │   └── sw_JOB_EMD_Version_TRIGGER.yml
│   └── actions
│       ├── sw_JOB_EMD_Check_Consistency_TRIGGER.yml
│       ├── sw_JOB_EMD_Post_Doc_TRIGGER.yml
│       └── sw_JOB_EMD_Version_TRIGGER.yml
└── items
    ├── github
    │   └── workflows
    │       ├── wf_EMD
    │       │   ├── README.md
    │       │   ├── sw_JOB_EMD_Check_Consistency_TRIGGER.yml
    │       │   ├── sw_JOB_EMD_Post_Doc_TRIGGER.yml
    │       │   └── sw_JOB_EMD_Version_TRIGGER.yml
    │       ├── wf_check_requisites
    │       │   ├── README.md
    │       │   └── sw_JOB_wf_check_requisites_TRIGGER.yaml
    │       └── wf_drop_between_releases
    │           ├── README.md
    │           └── sw_JOB_drop_between_releases_TRIGGER.yml
    ├── jenkins
    │   ├── ci_jobs
    │   │   ├── sw_JOB_EMD_Check_Consistency
    │   │   │   ├── README.md
    │   │   │   └── code
    │   │   │       ├── requirements.txt
    │   │   │       ├── requirements.txt.dev
    │   │   │       ├── sw_JOB_EMD_Check_Consistency.json
    │   │   │       ├── sw_JOB_EMD_Check_Consistency.py
    │   │   │       └── sw_JOB_EMD_Check_Consistency.xml
    │   │   ├── sw_JOB_EMD_Post_Doc
    │   │   │   ├── README.md
    │   │   │   └── code
    │   │   │       ├── requirements.txt
    │   │   │       ├── requirements.txt.dev
    │   │   │       ├── sw_JOB_EMD_Post_Doc.json
    │   │   │       ├── sw_JOB_EMD_Post_Doc.py
    │   │   │       └── sw_JOB_EMD_Post_Doc.xml
    │   │   ├── sw_JOB_EMD_Version
    │   │   │   ├── README.md
    │   │   │   └── code
    │   │   │       ├── requirements.txt
    │   │   │       ├── requirements.txt.dev
    │   │   │       ├── sw_JOB_EMD_Version.json
    │   │   │       ├── sw_JOB_EMD_Version.py
    │   │   │       └── sw_JOB_EMD_Version.xml
    │   │   └── sw_JOB_drop_between_releases
    │   │       ├── README.md
    │   │       └── code
    │   │           ├── requirements.txt
    │   │           ├── requirements.txt.dev
    │   │           ├── sw_JOB_drop_between_releases.json
    │   │           ├── sw_JOB_drop_between_releases.py
    │   │           └── sw_JOB_drop_between_releases.xml
    │   └── libraries
    │       ├── python
    │       │   ├── sw_ci_cm
    │       │   │   ├── README.md
    │       │   │   └── code
    │       │   │       ├── emb_ci_cm
    │       │   │       │   ├── __init__.py
    │       │   │       │   ├── cm_config.py
    │       │   │       │   └── requirements.txt
    │       │   │       ├── pyproject.toml
    │       │   │       ├── requirements.txt
    │       │   │       └── setup.py
    │       └── groovy
    │           ├── sw_jenkins_lib
    │           │   ├── README.md
    │           │   └── code
    │           │       ├── ... # Código y archivos de configuración para librerías compartidas de Groovy
    └── libraries
        ├── ci_emd
        │   ├── README.md
        │   └── code
        │       ├── emb_ci_emd
        │       │   ├── __init__.py
        │       │   ├── emd_api.py
        │       │   ├── emd_config.py
        │       │   ├── emd_mail.py
        │       │   ├── emd_utils.py
        │       │   └── requirements.txt
        │       ├── pyproject.toml
        │       ├── requirements.txt
        │       └── setup.py
        └── python_modules
            ├── sw_github_api_utils
            │   ├── README.md
            │   └── code
            │       ├── emb_gh_api_utils
            │       │   ├── __init__.py
            │       │   ├── gh_api_client.py
            │       │   └── requirements.txt
            │       ├── pyproject.toml
            │       ├── requirements.txt
            │       └── setup.py
            ├── sw_json_utils
            │   ├── README.md
            │   └── code
            │       ├── emb_json_utils
            │       │   ├── __init__.py
            │       │   ├── main.py
            │       │   └── requirements.txt
            │       ├── pyproject.toml
            │       ├── requirements.txt
            │       └── setup.py
            ├── sw_path_utils
            │   ├── README.md
            │   └── code
            │       ├── emb_path_utils
            │       │   ├── __init__.py
            │       │   ├── main.py
            │       │   └── requirements.txt
            │       ├── pyproject.toml
            │       ├── requirements.txt
            │       └── setup.py
            ├── sw_pygithub_utils
            │   ├── README.md
            │   └── code
            │       ├── emb_pgh_utils
            │       │   ├── __init__.py
            │       │   ├── emb_pgh_client.py
            │       │   ├── emb_pgh_commit.py
            │       │   ├── emb_pgh_release.py
            │       │   ├── emb_pgh_repo.py
            │       │   └── requirements.txt
            │       ├── pyproject.toml
            │       ├── requirements.txt
            │       └── setup.py
            └── sw_smtp_lib_utils
                ├── README.md
                └── code
                    ├── emb_smtp_lib_utils
                    │   ├── __init__.py
                    │   ├── emb_smpt_ssl_client.py
                    │   └── requirements.txt
                    ├── pyproject.toml
                    ├── requirements.txt
                    └── setup.py
```
