#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-ds-object-modify-success-5136"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
ExtractionType =json
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [
"""EventID"""
"""":5136"""
"""A directory service object was modified"""
]
Fields = [
"""<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
""""TimeGenerated\\?":\\?"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
""""+EventTime\\?"+:\\?"+({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})\\?"+"""
"""({additional_info}({event_name}A directory service object was modified))"""
""""+Hostname\\?"+:\\?"+({dest_host}({host}[\w\-.]+))\\?"+"""
""""Computer(|Name)":"({dest_host}({host}[\w\-.]+))""""
""""+EventType\\?"+:\\?"+({result}[^"\\]+)\\?"+"""
""""+Severity\\?"+:\\?"+({severity}[^"\\]+)\\?"+"""
""""+EventID\\?"+:({event_code}\d+)"""
""""+SourceName\\?"+:\\?"+({log_source}[^"\\]+)\\?"+"""
""""+ProviderGuid\\?"+:\\?"+\{({process_guid}[^}]+)"""
""""+ActivityID"+:"+\{({activity_id}[^}]+)"""
""""+ProcessID\\?"+:({process_id}\d+)"""
""""+Category\\?"+:\\?"+({category}[^"\\]+)"""
"""Subject:.+?Security ID:((\\)*(\\r|\\t|\\n))*({user_sid}[^:]+?)((\\)*(\\r|\\t|\\n))*Account Name:(\\n|\\r|\\t)*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))((\\)*(\\r|\\t|\\n))*Account Domain:((\\)*(\\r|\\t|\\n))*({src_domain}({domain}[^:]+?))((\\)*(\\r|\\t|\\n))*Logon ID:((\\)*(\\r|\\t|\\n))*({login_id}[^\s]+?)\s*((\\)*(\\r|\\t|\\n))*\w+\s"""
"""Object:.+?Class:((\\)*(\\r|\\t|\\n))*(\s*|)({object_type}[^:]+?)(\s*|)((\\)*(\\r|\\t|\\n))*\w+:"""
""""SubjectUserName\\?"+:\\?"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?""""
""""SubjectUserSid\\?"+:\\?"+({user_sid}[^"\\]+)\\?""""
""""SubjectLogonId\\?"+:\\?"+({login_id}[^"\\]+)\\?""""
""""ObjectClass\\?":\\?"({object_type}[^"\\]+)\\?""""
""""ObjectDN\\?":\\?"({ds_object_dn}[^"\\]+)\\?""""
""""SubjectDomainName\\?":\\?"({src_domain}({domain}[^"\\]+))\\?""""
"""<Data Name\\*=('|")ObjectDN('|")>\s*({ds_object_dn}[^<]+?)\s*</Data>"""
"""<Data Name\\*=("|')DSName("|')>(|({ds_name}[^<]+?))</Data>"""
"""<Data Name\\*=('|")DSType('|")>(|({ds_type}[^<]+?))</Data>"""
"""exa_regex=<TimeCreated SystemTime(\\)?=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
"""exa_regex="TimeGenerated\\?":\\?"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)"""
"""exa_regex="+EventTime\\?"+:\\?"+({time}\d{4}-\d{2}-\d{2}\s\d{2}:\d{2}:\d{2})\\?"+"""
"""exa_regex=({additional_info}({event_name}A directory service object was modified))"""
"""exa_regex="+Hostname\\?"+:\\?"+({dest_host}({host}[\w\-.]+))\\?"+"""
"""exa_regex="Computer(|Name)":"({dest_host}({host}[\w\-.]+))""""
"""exa_regex="+EventType\\?"+:\\?"+({result}[^"\\]+)\\?"+"""
"""exa_regex="+Severity\\?"+:\\?"+({severity}[^"\\]+)\\?"+"""
""""+EventID\\?"+:({event_code}\d+)"""
"""exa_regex="+SourceName\\?"+:\\?"+({log_source}[^"\\]+)\\?"+"""
"""exa_regex="+ProviderGuid\\?"+:\\?"+\{({process_guid}[^}]+)"""
"""exa_regex="+ActivityID"+:"+\{({activity_id}[^}]+)"""
"""exa_regex="+ProcessID\\?"+:({process_id}\d+)"""
"""exa_regex="+Category\\?"+:\\?"+({category}[^"\\]+)"""
"""exa_regex=Subject:.+?Security ID:((\\)*(\\r|\\t|\\n))*({user_sid}[^:]+?)((\\)*(\\r|\\t|\\n))*Account Name:(\\n|\\r|\\t)*({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))((\\)*(\\r|\\t|\\n))*Account Domain:((\\)*(\\r|\\t|\\n))*({src_domain}({domain}[^:]+?))((\\)*(\\r|\\t|\\n))*Logon ID:((\\)*(\\r|\\t|\\n))*({login_id}[^\s]+?)\s*((\\)*(\\r|\\t|\\n))*\w+\s"""
"""exa_regex=Object:.+?Class:((\\)*(\\r|\\t|\\n))*(\s*|)({object_type}[^:]+?)(\s*|)((\\)*(\\r|\\t|\\n))*\w+:"""
"""exa_regex="SubjectUserName\\?"+:\\?"+({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?""""
"""exa_regex="SubjectUserSid\\?"+:\\?"+({user_sid}[^"\\]+)\\?""""
"""exa_regex="SubjectLogonId\\?"+:\\?"+({login_id}[^"\\]+)\\?""""
"""exa_regex="ObjectClass\\?":\\?"({object_type}[^"\\]+)\\?""""
"""exa_regex="ObjectDN\\?":\\?"({ds_object_dn}[^"\\]+)\\?""""
"""exa_regex="SubjectDomainName\\?":\\?"({src_domain}({domain}[^"\\]+))\\?""""
"""exa_regex=<Data Name\\*=('|")ObjectDN('|")>\s*({ds_object_dn}[^<]+?)\s*</Data>"""
"""exa_regex=<Data Name\\*=("|')DSName("|')>(|({ds_name}[^<]+?))</Data>"""
"""exa_regex=<Data Name\\*=('|")DSType('|")>(|({ds_type}[^<]+?))</Data>"""
"""AttributeValue("|')>({attribute_value}[^"'<]+)</Data>"""
"""exa_regex=AttributeValue("|')>({attribute_value}[^"'<]+)</Data>"""
"""<Data Name(\\)?=('|")OperationType('|")>({operation_type}[^<]+)"""
"""exa_regex=<Data Name(\\)?=('|")OperationType('|")>({operation_type}[^<]+)"""
"""exa_json_path=$.AttributeValue,exa_field_name=attribute_value""",
"""exa_json_path=$.OperationType,exa_field_name=operation_type""",
"""exa_json_path=$.AttributeLDAPDisplayName,exa_field_name=attribute""",
"""AttributeValue(\\)?":(\\)?"({attribute_value}[^"'>\\]+)""",
"""OperationType(\\)?":(\\)?"({operation_type}[^"\\]+)"""
"""<Data Name\\*=('|")AttributeLDAPDisplayName('|")>\s*({attribute}[^<]+?)\s*</Data>"""
"""exa_regex=<Data Name\\*=('|")AttributeLDAPDisplayName('|")>\s*({attribute}[^<]+?)\s*</Data>"""
"""AttributeLDAPDisplayName(\\)?":(\\)?"({attribute}[^"\\]+)"""
"""exa_json_path=$.EventID,exa_field_name=event_code""",
]
ParserVersion = "v1.0.0"


}
```