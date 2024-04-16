#### Parser Content
```Java
{
Name = microsoft-evsecurity-csv-ds-object-activity-success-4662
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""""An operation was performed on an object",""", ""","4662",""" ]
  Fields = [
    """({event_name}An operation was performed on an object)""",
    """"({event_code}4662)"""",
    """"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)","({host}[\w\-.]+)"""",
    """"4662"",""({user_sid}[^"]+)"""",
    """"4662",("[^"]*",){1}"({user}[\w\.\-]{1,40}\$?)"""",
    """"4662",("[^"]*",){2}"({domain}[^"]+)"""",
    """"4662",("[^"]*",){3}"({login_id}[^"]+)"""",
    """"4662",("[^"]*",){4}"({dest_domain}[^"]+)"""",
    """"4662",("[^"]*",){5}"({dest_user}[^"]+)"""",
    """"4662",("[^"]*",){6}"({dest_user_sid}[^"]+)"""",
    """"(An operation was performed on an object)",("[^"]+",){2}"({ds_object_class}[^"]+)""",
    """"(An operation was performed on an object)",("[^"]+",){3}"({ds_object_name}[^"]+)""",
    """"(An operation was performed on an object)",("[^"]+",){4}"({ds_object_type}[^"]+)""",
    """"(An operation was performed on an object)",("[^"]+",){5}"(LOCAL SERVICE|({user}[\w\.\-]{1,40}\$?))""",
    """"(An operation was performed on an object)",("[^"]+",){6}"({login_id}[^"]+)""",
    """"(An operation was performed on an object)",("[^"]+",){7}"(NT AUTHORITY|({domain}[^"]+))""",
    """"(An operation was performed on an object)",("[^"]+",){8}"({operation}[^"]+)""",
    """"(An operation was performed on an object)",("[^"]+",){9}"[\\ntr-]*(-|({properties}[^"]+))""",
    """"(An operation was performed on an object)",("[^"]+",){10}"[\\ntr-]*({attribute}[^"]+?)[trn\s\\]*(<\/Message>|")""",
    """"(An operation was performed on an object)",("[^"]+",){12}"({result}[^"]+)"""
  ]
  DupFields = ["host->dest_host","ds_object_name->object"]
  ParserVersion = "v1.0.0"


}
```