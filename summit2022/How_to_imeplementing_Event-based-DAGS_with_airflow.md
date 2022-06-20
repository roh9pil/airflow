## Event-based triggering

### TriggerDagRunOperator
* for when the trigger event comes from another DAG in the same environment
* Easy to implement
* Both controller and triggered DAGs must be in the same Airflow environment

### Sensors
* For when you are not quite sure of the right time
* wait for something happens
* Effectively just another operator in your DAG

### Deferrable Operator
* For when sensors are ideal bu the waiting is expensive
* compute saving
* trigger process

### Airflow API
* for when the trigger event is truly random
* good to ad-hoc triggering
* support only triggering dags

현재는 trigger가 첫번째 이벤트에 대해서 launch 혹은 resume 만 하도록 되어있는데, 
특정 이벤트가 감지되면 계속 DAG를 실행하도록 변경하고 있다고..

