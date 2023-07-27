#### Parser Content
```Java
{
Name = microsoft-windows-json-service-create-success-4697
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "epoch"
  Conditions = [ """"event_id":4697""", """A service was installed in the system""", """"provider":"Microsoft-Windows-Security-Auditing"""", """"message":""" ]
  Fields = [
    """"timestamp":({time}\d{13})""",
    """({event_code}4697)""",
    """({event_name}A service was installed in the system)""",
    """"hostname":"({host}[^"]+)"""",
    """"keywords":[\["]*({result}[^"\]]+)""",
    """"SubjectUserSid":"({user_sid}[^"]+)"""",
    """"SubjectUserName":"({user}[\w\.\-]{1,40}\$?)"""",
    """"SubjectDomainName":"({domain}[^"]+)"""",
    """"SubjectLogonId":"({login_id}[^"]+)"""",
    """"ServiceName":"({service_name}[^"]+)"""",
    """"ServiceFileName":"\s*(|({process_path}({process_dir}.*?[\\\/]+)?({process_name}[^\\\/]+?)))"""",
    """"ServiceType":"({service_type}[^"]+)"""",
    """"ServiceStartType":"({service_start_type}[^"]+)"""",
    """"ServiceAccount":"({account_domain}[^"]+)"""",
    """"pid":({process_id}\d+)"""
  ]
  DupFields = [ "host->dest_host" ]
  ParserVersion = "v1.0.0"


}
```