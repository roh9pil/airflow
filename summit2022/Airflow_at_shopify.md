* Oozie, Azkaban을 소소하게 쓰다가 2020년부터 Airflow를 사용하 시작함
* 3명의 엔지니어
* Google Cloud 위에 올렸네

## Testing
### Unit tests
* make assertions abount the structure and composition of the workflow, DAG
* no duplicated DAG IDs

### Smoke Tests
* operators and libraries
   - a set of supported operators
   - Create a DAG which uses all of these operators
   - Just run this DAG every time something changes

### Load Tests
* used by infrastructure team


## Policies and Guardrails
### Multi tenancy via Airflow Manifests
* airflow_projects.yaml 
### Dag policy
* allows you to conditionally reject DAGs at time of loading

Metadata truncation daily: save time when migration

