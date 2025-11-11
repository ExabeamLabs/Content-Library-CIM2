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
    """"(Hostname|Computer)":"({dest_host}({host}[^"]+))""""
    """"EventTime":\s*"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)"""
    """"SubjectUserSid":"({user_sid}[^"]+)""""
    """"SubjectUserName":"({src_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"SubjectDomainName":"({src_domain}({domain}[^"]+))""""
    """"SubjectLogonId":"({login_id}[^"]+)""""
    """"ObjectServer":"({object_server}[^"]+)""""
    """"HandleId":"({object_id}[^"]+)""""
    """"ProcessName":"(|-|({process_path}({process_dir}.*?)({process_name}[^\\\/]+?)))""""
  ]


}
```