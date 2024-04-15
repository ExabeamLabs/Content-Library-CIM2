#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-modify-success-5136"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""EventID":5136"""
"""A directory service object was modified"""
]
Fields = [
""""+EventTime"+:"+({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})"+"""
"""({event_name}A directory service object was modified)"""
""""+Hostname"+:"+({host}[^"]+)"+"""
""""+EventType"+:"+({result}[^"]+)"+"""
""""+Severity"+:"+({severity_type}[^"]+)"+"""
""""+EventID"+:({event_code}\d+)"""
""""+SourceName"+:"+({log_source}[^"]+)"+"""
"""""+ProviderGuid"+:"+\{({process_guid}[^}]+)"""
""""+ActivityID"+:"+\{({activity_id}[^}]+)"""
""""+ProcessID"+:({process_id}\d+)"""
""""+Message"+:"+({additional_info}[^"]+?)\s*"""
""""+Category"+:"+({category}[^"]+)"""
""""SubjectUserName"+:"+({user}[^"]+)""""
""""SubjectUserSid"+:"+({user_sid}[^"]+)""""
""""SubjectLogonId"+:"+({login_id}[^"]+)""""
""""ObjectClass":"({ds_object_class}[^"]+)""""
""""ObjectDN":"({object_dn}[^"]+)""""
""""SubjectDomainName":"({domain}[^"]+)""""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```