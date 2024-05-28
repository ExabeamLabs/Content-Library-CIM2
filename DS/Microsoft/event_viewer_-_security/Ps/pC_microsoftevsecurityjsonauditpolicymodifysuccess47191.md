#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-audit-policy-modify-success-4719-1"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
ExtractionType = json
Conditions = [ """"event_id":4719""", """System audit policy was changed."""]
Fields = [
"""exa_json_path=$.message_info,exa_field_name=event_name""",
"""exa_json_path=$.@timestamp,exa_field_name=time""",
"""exa_json_path=$.computer_name,exa_regex=^({host}[\w\-.]+)$""",
"""exa_json_path=$.event_id,exa_field_name=event_code""",
"""exa_json_path=$.event_data.SubjectUserName,exa_regex=^({user}[\w\.\-]{1,40}\$?)$""",
"""exa_json_path=$.event_data.SubjectDomainName,exa_field_name=domain""",
"""exa_json_path=$.event_data.SubjectLogonId,exa_field_name=login_id""",
"""exa_json_path=$.logon_id,exa_field_name=login_id""",
"""exa_json_path=$.event_data.CategoryId,exa_field_name=audit_category""",
"""exa_json_path=$.message,exa_regex=Category:(\\t|\\n|\s)*({audit_category}.+?)(\\t|\\n|\s)+Subcategory:""",
"""exa_json_path=$.$.event_data.SubcategoryId,exa_field_name=sub_category""",
"""exa_json_path=$.message,exa_regex=Subcategory:(\\t|\\n|\s)*({sub_category}.+?)(\\t|\\n|\s)+Subcategory GUID:""",
"""exa_json_path=$.event_data.AuditPolicyChanges,exa_field_name=policy_name""",
"""exa_json_path=$.message,exa_regex=Changes:(\\t|\\n|\s)*({policy_name}.+?)(\\t|\\n|")"""
]
DupFields = [ "host->src_host" ]
ParserVersion = "v1.0.0"


}
```