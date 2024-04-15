#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-service-create-success-4697"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
""""EventID":4697"""
"""A service was installed in the system"""
]
Fields = [
""""EventTime":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
"""({event_code}4697)"""
"""({event_name}A service was installed in the system)"""
""""Hostname":"({host}[^"]+)""""
""""Keywords":({result}[^,]+),"""
""""SubjectUserSid":"({user_sid}[^"]+)""""
""""SubjectUserName":"({user}[^"]+)""""
""""SubjectDomainName":"({domain}[^"]+)""""
""""SubjectLogonId":"({login_id}[^"]+)""""
""""ServiceName":"({service_name}[^"]+)""""
""""ServiceFileName":"\s*(|({process_path}({process_dir}.*?[\\\/]+)?({process_name}[^\\\/]+?)))""""
""""ServiceType":"({service_type}[^"]+)""""
""""ServiceStartType":"({service_start_type}[^\"]+)""""
""""ServiceAccount":"({account_domain}[^"]+)""""
""""ProcessID":({process_id}\d+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```