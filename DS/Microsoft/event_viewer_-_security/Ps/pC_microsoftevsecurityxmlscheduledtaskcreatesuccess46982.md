#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-scheduled-task-create-success-4698-2"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch_sec"
Conditions = [
"""EventID=4698"""
"""A scheduled task was created"""
]
Fields = [
"""\WComputer=({host}[\w\.\-]+)"""
"""\WEventID=({event_code}\d+)"""
"""\WTimeGenerated=({time}\d{10})"""
"""\sAccount Name:\s*(|({user}[\w\.\-]{1,40}\$?))\s*Account Domain:\s*(|({domain}.+?))\s*Logon ID:\s*(|({login_id}.+?))\s*Task Information:"""
"""\sTask Name:\s*(|(?=[\\\w])({task_name}.+?))\s*Task Content:"""
"""<UserId>(?=\w)(({account_domain}[^\\<]*)\\)?({account_name}[^<]+)</UserId>"""
"""<RunLevel>(?=\w)({run_level}[^<]+)</RunLevel>"""
"""<RegistrationInfo>.+?<Description>(?=\w)({description}[^<]+)</Description>"""
"""<Command>\"?({process_path}({process_dir}(?:(\w+:)?[^:<\"]+)?[\\\/])?({process_name}[^<\"]+))"""
"""<Arguments>(\"+)?({arg}[^<\"]+)"""
"""({event_name}A scheduled task was created)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```