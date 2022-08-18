# RUN AFTER ALL FAILED DAGS, CUSTOM MESSAGE TO THE OUTPUT

send_debug_message = BashOperator(
    task_id=f'task_name',
    bash_command=f'echo "My custom message"',
    trigger_rule='all_failed',
    dag=dag
)
