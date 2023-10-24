#### Parser Content
```Java
{
Name = "endgame-edr-json-alert-trigger-success-investigationid"
Vendor = "Endgame"
Product = "Endgame EDR"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""investigation_id"""
""""doc_type": "alert""""
"""origination_task_id"""
]
Fields = [
""""serial_event_id\":\s*({alert_id}\d+)"""
""""pid\":\s*({process_id}\d+)"""
""""sha256\":\s*\"({hash_sha256}[^\",]+)"""
""""process_name\":\s*\"({process_name}[^\",]+)"""
""""user_name\":\s*\"(SYSTEM|({user}[\w\.\-]{1,40}\$?))"""
""""timestamp_utc\":\s*\"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""""parent_process_path\":\s*\"({parent_process_path}[^\",]+)"""
""""original_file_name\":\s*\"({file_name}[^\",]+)"""
""""user_sid\":\s*\"({user_sid}[^\",]+)"""
""""parent_process_name\":\s*\"({parent_process}[^\",]+)"""
""""process_path\":\s*\"({process_path}({process_dir}.*?)(\\+({process_name}[^\\\"]+?))?)\""""
""""user_domain\":\s*\"({domain}[^\",]+)"""
""""md5\":\s*\"({hash_md5}[^\",]+)"""
""""opcode\":\s*({opcode}\d+)"""
""""command_line\":\s*\"({process_command_line}.+?)\"(,|\})"""
""""rule_id\":\s*\"({rule_id}[^\"]+)"""
""""event_type_human\":\s*\"({event_name}[^\"]+)"""
""""rule_name\":\s*\"({alert_name}[^\"]+)"""
"""severity\":\s*\"({alert_severity}[^\"]+)"""
""""hostname\":\s*\"({src_host}[^\"]+)"""
""""ip_address\":\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""operating_system\":\s*\"({os}[^\"]+)"""
]
ParserVersion = "v1.0.0"


}
```