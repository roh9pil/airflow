# Dag를 어떻게 만드라는 것인지

## Principles
* Atomicity; All or None
* Idempotency: Make failures safe
  - e.g., UPSERT for database insert method
* Protect downstream
  - retries, backoff
  - max active runs
  - preemtive load shedding
* Fail fast and fail forward
  - sla at task: expected maximum execution time
     - dashboard에 표시
  - execution_timeout: 이건 넘어가면 fail 처리
  - Raise AirflowSkipException and AirflowFailException on obvious errors
  - Checkpoint/validate data

## Best practices
* Use Airflow as an orchestration tool
* Operation as code
* Monitoring Workflow
  - operational metrics
