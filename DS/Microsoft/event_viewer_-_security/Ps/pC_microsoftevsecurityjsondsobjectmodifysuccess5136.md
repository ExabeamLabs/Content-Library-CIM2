#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-modify-success-5136"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
"""EventID"""
"""":5136"""
"""A directory service object was modified"""
]
Fields = [
""""+EventTime\\?"+:\\?"+({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})\\?"+"""
"""({event_name}A directory service object was modified)"""
""""+Hostname\\?"+:\\?"+({host}[\w\-.]+)\\?"+"""
""""ComputerName":"({host}[\w\-.]+)""""
""""+EventType\\?"+:\\?"+({result}[^"\\]+)\\?"+"""
""""+Severity\\?"+:\\?"+({severity_type}[^"\\]+)\\?"+"""
""""+EventID\\?"+:({event_code}\d+)"""
""""+SourceName\\?"+:\\?"+({log_source}[^"\\]+)\\?"+"""
""""+ProviderGuid\\?"+:\\?"+\{({process_guid}[^}]+)"""
""""+ActivityID"+:"+\{({activity_id}[^}]+)"""
""""+ProcessID\\?"+:({process_id}\d+)"""
""""+Message\\?"+:\\?"+({additional_info}[^"\.\\]+)\s*"""
""""+Category\\?"+:\\?"+({category}[^"\\]+)"""
"""Subject:.+?Security ID:((\\)*(\\r|\\t|\\n))*({user_sid}[^:]+?)((\\)*(\\r|\\t|\\n))*Account Name:(\\n|\\r|\\t)*({user}[\w\.\-]{1,40}\$?)((\\)*(\\r|\\t|\\n))*Account Domain:((\\)*(\\r|\\t|\\n))*({domain}[^:]+?)((\\)*(\\r|\\t|\\n))*Logon ID:((\\)*(\\r|\\t|\\n))*({login_id}[^\s]+?)\s*((\\)*(\\r|\\t|\\n))*\w+\s"""
"""Object:.+?Class:((\\)*(\\r|\\t|\\n))*({ds_object_class}[^:]+?)((\\)*(\\r|\\t|\\n))*\w+:"""
""""SubjectUserName\\?"+:\\?"+({user}[\w\.\-]{1,40}\$?)\\?""""
""""SubjectUserSid\\?"+:\\?"+({user_sid}[^"\\]+)\\?""""
""""SubjectLogonId\\?"+:\\?"+({login_id}[^"\\]+)\\?""""
""""ObjectClass\\?":\\?"({ds_object_class}[^"\\]+)\\?""""
""""ObjectDN\\?":\\?"({ds_object_dn}[^"\\]+)\\?""""
""""SubjectDomainName\\?":\\?"({domain}[^"\\]+)\\?""""
"""<Data Name\\*=('|")ObjectDN('|")>\s*({ds_object_dn}[^<]+?)\s*</Data>"""
"""<Data Name\\*=("|')DSName("|')>(|({ds_name}[^<]+?))</Data>"""
"""<Data Name\\*=('|")DSType('|")>(|({ds_type}[^<]+?))</Data>"""

]
DupFields = [
"host->dest_host",
"event_name->additional_info"
]
ParserVersion = "v1.0.0"


}
```