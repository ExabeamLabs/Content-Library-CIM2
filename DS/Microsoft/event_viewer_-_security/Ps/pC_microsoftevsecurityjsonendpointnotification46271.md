#### Parser Content
```Java
{
Name = microsoft-evsecurity-json-endpoint-notification-4627-1
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "MM/dd/yyyy hh:mm:ss a"
  Conditions = [ """"event_id":"4627"""", """"new_logon-AccountName":""", """"group_membership":""" ]
  Fields = [
    """({event_name}The subject fields indicate the account on the local system which requested the logon)""",
    """({time}\d+\/\d+\/\d\d\d\d \d+:\d\d:\d\d (am|AM|pm|PM))""",
    """"computer":"({host}[^"]+)""",
    """"new_logon-AccountName":"({user}[\w\.\-]{1,40}\$?)""",
    """"new_logon-AccountDomain":"({domain}[^"]+)""",
    """"new_logon-LogonID":"({login_id}[^"]+)""",
    """"new_logon-SecurityID":"({user_sid}[^"]+)""",
    """"event_id":"({event_code}\d+)""",
    """"login_type":"({login_type}\d+)""",
# group_membership is removed
  ]
  DupFields = [ "host->dest_host" ]


}
```