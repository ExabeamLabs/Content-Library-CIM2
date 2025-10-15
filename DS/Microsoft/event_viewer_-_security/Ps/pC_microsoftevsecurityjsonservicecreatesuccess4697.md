#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-service-create-success-4697"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
ExtractionType = json
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [ """"EventID":4697""", """"ServiceName":"""", """"ServiceFileName":"""", """"ServiceStartType":"""" ]
Fields = [
""""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).\d+Z\s[^\s]+\s"""
"""({event_code}4697)"""
"""({event_name}A service was installed in the system)"""
""""Hostname":"({host}[\w\-.]+)""""
""""Keywords":({result}[^,]+),"""
""""SubjectUserSid":"({user_sid}[^"]+)""""
""""SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
""""SubjectDomainName":"({domain}[^"]+)""""
""""SubjectLogonId":"({login_id}[^"]+)""""
"""Service Name:\s*(\\+r|\\+t|\\+n)*(({service_name}[^=:\\_]+?)(_[^"\<]+?)?)\s*(\\+r|\\+t|\\+n)*Service """
""""ServiceName":"(({service_name}[^_"]+?)(_[^"\<]+?)?)"""",
""""ServiceFileName":"({service_command_line}.*?)"""",
""""ServiceType":"({service_type}[^"]+)""""
""""ServiceStartType":"({service_start_type}[^\"]+)""""
""""ServiceAccount":"({account_domain}[^"]+)""""
""""ProcessID":({process_id}\d+)"""
""""EventType":"({operation_type}[^"]+?)""""
""""Computer(Name)?":"({host}[\w\-\.]+)"""

"""exa_json_path=$.EventTime,exa_field_name=time""",
"""exa_json_path=$.EventID,exa_field_name=event_code""",
"""exa_regex=({event_name}A service was installed in the system)""",
"""exa_json_path=$.Hostname,exa_field_name=host""",
"""exa_json_path=$.Keywords,exa_field_name=result""",
"""exa_json_path=$.SubjectUserSid,exa_field_name=user_sid""",
"""exa_json_path=$.SubjectUserName,exa_field_name=user""",
"""exa_json_path=$.SubjectDomainName,exa_field_name=domain""",
"""exa_json_path=$.SubjectLogonId,exa_field_name=login_id""",
"""exa_json_path=$.ServiceName,exa_field_name=service_name""",
"""exa_json_path=$.ServiceFileName,exa_field_name=service_command_line""",
"""exa_json_path=$.ServiceType,exa_field_name=service_type""",
"""exa_json_path=$.ServiceStartType,exa_field_name=service_start_type""",
"""exa_json_path=$.ServiceAccount,exa_field_name=account_domain""",
"""exa_json_path=$.ProcessID,exa_field_name=process_id""",
"""exa_json_path=$.EventType,exa_field_name=operation_type""",
"""exa_json_path=$.SourceName,exa_field_name=provider_name"""
]
DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]
ParserVersion = "v1.0.0"


}
```