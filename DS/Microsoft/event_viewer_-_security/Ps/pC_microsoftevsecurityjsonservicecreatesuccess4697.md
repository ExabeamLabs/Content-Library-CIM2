#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-service-create-success-4697"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = ["yyyy-MM-dd HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss"]
Conditions = [
""""EventID":4697"""
"""A service was installed in the system"""
]
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
""""ServiceFileName":"\s*(|({process_path}({process_dir}.*?[\\\/]+)?({process_name}[^\\\/]+?)))""""
""""ServiceType":"({service_type}[^"]+)""""
""""ServiceStartType":"({service_start_type}[^\"]+)""""
""""ServiceAccount":"({account_domain}[^"]+)""""
""""ProcessID":({process_id}\d+)"""
""""EventType":"({operation_type}[^"]+?)""""
""""ComputerName":"({host}[\w\-\.]+)"""
]
DupFields = [
"host->dest_host"
]
ParserVersion = "v1.0.0"


}
```