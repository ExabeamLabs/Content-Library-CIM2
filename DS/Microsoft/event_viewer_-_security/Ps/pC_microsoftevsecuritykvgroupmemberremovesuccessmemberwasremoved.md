#### Parser Content
```Java
{
Name = "microsoft-evsecurity-kv-group-member-remove-success-memberwasremoved"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = [
    """MSWinEventLog"""
    """A member was removed from a security-enabled"""
  ]
  Fields = [
    """({event_name}A member was removed from a security-enabled [\w\s]+ group)""",
    """({time}\w{1,3}\s\d{1,2}\s\d{1,2}:\d{1,2}:\d{1,2}\s\d{1,4})""",
    """({event_code}4757|4729|4733)""",
    """({event_code}\d+)\s+Microsoft-Windows-Security-Auditing""",
    """({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\sMSWinEventLog""",
    """Information\s+({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))\s+""",
    """(?:Success|Audit)\s+\w+\s+({host}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[\w.\-]+))""",
    """A member was removed from a security-enabled\s+({group_type}.+?)\s+group.+?Account Name:\s+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+Account Domain:\s+({domain}.+?)\s+Logon ID:\s+({login_id}[^\s]+)\s+Member:""",
    """Member:\s+Security ID:\s+(({dest_user_sid}S-\d+-[^\s"]+)|({account_id}[^\s]+))\s+Account Name:\s*(-|({user_dn}CN=.+?OU.+?DC.+?))?\s*Group:\s+Security ID:\s+({group_id}[^\s]+)\s+(Group|Account) Name:\s*({group_name}.+?)?\s+(Group|Account) Domain:\s+({group_domain}.+?)\s+Additional""",
    """Member:.+?Account Name:\s*CN=.+?({user_ou}OU.+?DC.+?)\s+Group:""",
  ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```