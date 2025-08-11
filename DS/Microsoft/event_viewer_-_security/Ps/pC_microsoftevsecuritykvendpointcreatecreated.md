#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-create-created
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ", "MMM dd HH:mm:ss yyyy"]
  Conditions = [ """A computer account was created""" ]
  Fields = [
    """({event_name}A computer account was created)""",
    """<Computer>({host}[\w\-.]+)<\/Computer>""",
    """<\d+>\w+ \d+ \d\d:\d\d:\d\d ({host}[\w_\-\.]+)""",
    """({time}\w+ \d+ \d+:\d+:\d+ \d\d\d\d)""",
    """SystemTime=('|")({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({event_code}4741)""",
    """Subject:.+?\sAccount Name:\s*(|-|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s*Account Domain:\s*(|-|({domain}.+?))\s*Logon ID:\s*(|-|({login_id}.+?))\s*New Computer Account:.*?\sAccount Name:\s*(|-|({dest_user}.+?))\s*Account Domain:\s*(|-|({object_dn}.+?))\s*Attributes:""",
    """\sComputer Account:.+?Account Name:\s*({dest_host}[^$:]+?)\$""",
    """\sUser Principal Name:\s*(|-|({attribute}.+?))\s*Home Directory:""",
    """New Computer Account:\s+Security ID:\s*({account_id}[^\s]+)"""
  ]


}
```