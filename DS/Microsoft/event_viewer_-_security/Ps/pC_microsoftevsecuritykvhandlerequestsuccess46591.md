#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-handle-request-success-4659-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "MM/dd/yyyy HH:mm:ss"
  Conditions = ["""A handle to an object was requested with intent to delete""", """4659""", """Computer"""]
  Fields = [
    """({event_name}A handle to an object was requested with intent to delete)""",
    """({event_code}4659)""",
    """({time}\d\d\/\d\d\/\d\d\d\d \d\d:\d\d:\d\d)\s(AM|PM|am|pm)""",
    """<?Computer>?(Name)?\s*=?\s*"*({host}[\w\.-]+)(\s|,|"|</Computer>|$)""",
    """Subject:.+?Security ID:\s*(|-|({user_sid}.+?))\s*Account Name:\s*(|-|({user}[\w\.\-]{1,40}\$?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}.+?))\s*Object:""",
    """\sObject:.+?Object Server:\s*(|-|({object_server}.+?))\s*Object Type:\s*(|-|({object_type}.+?))\s*Object Name:\s*(|-|({object}.+?))\s*Handle ID:\s*(|-|({object_id}.+?))\s*Process Information:\s*(|-|(.+?))\s*Process ID:\s*(|-|({process_id}.+?))\s*Access Request Information:""", # process_info is removed
    """TransactionId=\s\{({transaction_id}[^\}]+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```