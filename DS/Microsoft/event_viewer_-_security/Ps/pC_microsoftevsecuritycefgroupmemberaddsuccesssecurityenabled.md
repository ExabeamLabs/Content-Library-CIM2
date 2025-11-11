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
    """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+\w+="""
    """\ssuid=({login_id}\w+)"""
    """\sdntdom=({account_domain}[^\s]+)"""
    """\sduser=(({dest_user_sid}S-[^=]+?)|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?))\s+\w+="""
    """\scs6=({group_domain}[^\\]+)"""
    """\scs6=[^=]+?\\{1,25}({group_name}[^=]+?)\s+\w+="""
    """\sdvchost=({dest_host}({host}[\w\-.]+))"""
    """ad.Group:Security_,ID=({group_id}[^\s]+)"""
    """\sduid=(?=\w)({user_dn}.+?)\s+\w+="""
    """\sduid=(?=\w)(.+?CN\\?=.+?,({user_ou}(OU)?.+?DC\\?=[\w-]+))\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```