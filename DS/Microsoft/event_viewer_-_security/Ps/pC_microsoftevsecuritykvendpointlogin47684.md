#### Parser Content
```Java
{
Name = microsoft-evsecurity-kv-endpoint-login-4768-4
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Event Viewer - Security
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""A Kerberos authentication ticket (TGT) was requested""", """Account Name""", """computer_name"""]
  Fields = [
    """({event_name}A Kerberos authentication ticket \(TGT\) was requested)""",
    """"(?:winlog\.)?computer_name\\*":\\*"({host}[^\\"]+)""",
    """@timestamp":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """({event_code}4768)""",
    """Account Name(:|=)\s*({user}[^@;\s]+?)(?:@.+?)?[\s;]*Supplied Realm Name""",
    """Client Address(:|=)\s*(::[\w]+:)?({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """Result Code(:|=)\s*({result_code}.+?)[\s;]*Ticket Encryption Type(:|=)""",
    """Supplied Realm Name(:|=)\s*(-|({domain}[^\s]+?))[\s;]*User ID(:|=)""",
    """Supplied Realm Name(:|=)\s*.*?User ID(:|=)\s*(?:NULL SID|({user_sid}[^\s]+?))[\s;]*Service Information"""
  ]


}
```