## Redesign Airflow System Tests

Test Trinity
1) High Quality Test
2) Automatics Running
3) Report analysis

### AIP-47: New design of Airflow System Tests
* setup과 teardown은 pytest로 되어있었는데, 전체를 DAG로 변환해서 사용
* Watcher, Trigger_Rule을 사용해서 제안함

AIRFLOW Project/test/system
https://github.com/apache/airflow/blob/main/tests/system/providers/google/cloud/text_to_speech/example_text_to_speech.py




