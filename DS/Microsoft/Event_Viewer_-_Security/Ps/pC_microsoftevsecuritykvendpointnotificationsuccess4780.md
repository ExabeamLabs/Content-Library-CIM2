#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-notification-success-4780
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """(4780)""", """The ACL was set on accounts which are members of administrators groups""" ]
  Fields = [
    """({event_code}4780)""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)\s+EvntSLog""",
    """({event_name}The ACL was set on accounts which are members of administrators groups)""",
    """Subject:.*?Account Name:\s*(|({account_name}.+?))\s*Account Domain:\s*(|({account_domain}.+?))\s*Logon ID:\s*({account_id}\S+)""",
    """Target.*?Security ID:\s*(|(({dest_domain}[^\\\/]+?)[\\\/]+)?({dest_user}[^\\\/]+?))\s*Account Name:\s*(|({=dest_user}.+?))\s*Account Domain:""",
  ]


}
```