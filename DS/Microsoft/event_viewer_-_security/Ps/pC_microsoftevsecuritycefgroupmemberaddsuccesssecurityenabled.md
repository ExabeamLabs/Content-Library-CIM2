#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-group-member-add-success-securityenabled"
  Vendor = "Microsoft"
  Product = "Event Viewer - Security"
  TimeFormat = "epoch"
  Conditions = [
  """|Microsoft|Microsoft Windows|"""
  """A member was added to a security-enabled"""
  ]
  Fields = [
    """({event_name}A member was added to a security-enabled [\w\s]+ group)"""
    """({event_code}\d+)\|A member was added to a security-enabled"""
    """\|A member was added to a security-enabled ({group_type}\w+)"""
    """\srt=({time}\d{13})"""
    """\ssntdom=({domain}[^\s]+)"""
    """\ssuser=({user}.+?)\s+\w+="""
    """\ssuid=({login_id}\w+)"""
    """\sdntdom=({account_domain}[^\s]+)"""
    """\sduser=({account_id}.+?)\s+\w+="""
    """\scs6=({group_domain}[^\\]+)"""
    """\scs6=[^=]+?\\{1,25}({group_name}[^=]+?)\s+\w+="""
    """\sdvchost=({host}[^\s]+)"""
    """ad.Group:Security_,ID=({group_id}[^\s]+)"""
    """\sduid=(?=\w)({user_dn}.+?)\s+\w+="""
    """\sduid=(?=\w)(.+?CN\\?=.+?,({user_ou}(OU)?.+?DC\\?=[\w-]+))\s\w+="""
  ]

  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```