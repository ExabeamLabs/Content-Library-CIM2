#### Parser Content
```Java
{
Name = microsoft-evsecurity-str-endpoint-notification-logon
  Vendor = Microsoft
  Product = Event Viewer - Security
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """The subject fields indicate the account on the local system which requested the logon""", """Event in sequence:""", """Group Membership:""" ]
  Fields = [
    """({event_name}The subject fields indicate the account on the local system which requested the logon)""",
    """Subject:\s+Security ID:\s+\S+\s+Account Name:\s+(-|SYSTEM|({account}[^\s]+))\s+Account Domain:\s+(-|NT AUTHORITY|({account_domain}[^\s]+))\s+Logon ID""",
    """New Logon:\s+Security ID:\s+({user_sid}[^\s]+)\s+Account Name:""",
    """New Logon:\s+Security ID:\s+\S+\s+Account Name:\s+(-|SYSTEM|Administrator|({user}[^\s]+))\s+Account Domain:\s+(-|NT AUTHORITY|({domain}[^\s]+))\s+Logon ID:\s+({login_id}[^\s]+)\s""",
# group_membership is removed
    """Logon Type:\s+({login_type}\d+)\s+New Logon"""
  ]


}
```