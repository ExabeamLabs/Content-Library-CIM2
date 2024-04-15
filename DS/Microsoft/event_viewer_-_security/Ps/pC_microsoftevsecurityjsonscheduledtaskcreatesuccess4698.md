#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-scheduled-task-create-success-4698"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
""""EventID":4698"""
"""A scheduled task was created"""
]
Fields = [
""""EventTime":\s*\"?({time}\d{10})"""
""""Hostname":"({host}[\w.-]+?)""""
""""EventID":({event_code}\d+)"""
"""({event_name}A scheduled task was created)"""
""""SubjectUserName":"({user}[^\"]+)"""
""""SubjectDomainName":"({domain}[^\"]+)""""
""""SubjectUserSid":"({user_sid}[^\"]+)"""
""""TaskName":"({task_name}[^\"]+)""""
""""SubjectLogonId":"({login_id}[^\"]+)""""
""""Keywords":({result}[^,\"]+)"""
""""ProcessID":({process_id}\d+)"""
""""ThreadID":({thread_id}\d+)"""
"""<UserId>(?=\w)(({account_domain}[^\\<]*)\\)?({account_name}[^<]+)<\/UserId>"""
"""<Settings>[\\rnt\s]*({additional_info}[^\"]+?)\s*[\\rnt\s]*<\/Settings>"""
"""<Triggers>[\\rtn\s]*({triggers}[^\"]+?)[\\rtn\s]*<\/Triggers>"""
"""<RunLevel>(?=\w)({run_level}[^<]+)</RunLevel>"""
"""<Command>"?({process_path}({process_dir}(?:(\w+:)?[^:<\"]+)?[\\\/])?({process_name}[^<\"]+))"""
"""<Arguments>("+)?({arg}[^<\"]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```