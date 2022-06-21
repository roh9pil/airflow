## Deployment, versioninn, and package management

* Dags code in a single repository is problematic
* Split dag cods using git submodule
   - git submodule add http://~~
* pipeline steps
   1. initialize all submodules
      - git submodule update --init
   2. Dags validation tests
      - grammar, dependency check
   3. Generate version: semantic version
   4. build airflow image
   5. push to ECR
   6. update helm chart
   7. ArgoCD sync
 
* AIP-36: DAG Versioning
* DAG1, DAG2 수행시 필요한 python package version이 다를때
   - workflow management and execution
   - airflow run a container where business logics performed
   - Docker Operator or Kubernates Pod Operator
   - 우리와 비슷한 approach임 (execution이 jenkins agent에서 이뤄짐)
