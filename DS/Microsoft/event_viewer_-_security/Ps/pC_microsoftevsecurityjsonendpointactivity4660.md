#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-activity-4660
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""An object was deleted""", """"EventID":4660"""]
  Fields = [
    """({event_name}An object was deleted)""",
    """({event_code}4660)""",
    """"(Hostname|Computer)":"({host}[^"]+)""""
    """"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"SubjectUserSid":"({user_sid}[^"]+)""""
    """"SubjectUserName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """"SubjectDomainName":"({domain}[^"]+)""""
    """"SubjectLogonId":"({login_id}[^"]+)""""
    """"ObjectServer":"({object_server}[^"]+)""""
    """"HandleId":"({object_id}[^"]+)""""
    """"ProcessName":"(|-|({process_path}({process_dir}.*?)({process_name}[^\\\/]+?)))""""
  ]
  DupFields = [ "host->dest_host", "user->src_user", "domain->src_domain" ]


}
```