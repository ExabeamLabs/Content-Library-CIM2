#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-scheduled-task-create-success-4698"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "epoch_sec", "yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [
""""EventID":4698"""
"""A scheduled task was created"""
]
Fields = [
""""EventTime":\s*\"?({time}\d{10})"""
""""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""Hostname":"({host}[\w.-]+?)""""
""""Computer(Name)?":"({host}[\w\-.]+)"""
""""EventID":({event_code}\d+)"""
"""({event_name}A scheduled task was created)"""
""""SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
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
"""<Command>\\?"?({process_path}({process_dir}(?:(\w+:)?[^:<\"]+?)?[\\\/]+)?({process_name}[^<\"\\\/]+?))\\?"?<"""
"""<Arguments>("+)?({arg}[^<\"]+)"""
"""Subject:.+?Security ID:(\\r|\\n|\\t)*({user_sid}[^:]+?)(\\r|\\n|\\t)*Account Name:"""
]
DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]
ParserVersion = "v1.0.0"


}
```