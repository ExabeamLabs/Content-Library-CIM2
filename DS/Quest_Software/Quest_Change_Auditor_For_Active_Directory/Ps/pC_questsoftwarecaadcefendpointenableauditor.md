#### Parser Content
```Java
{
Name = questsoftware-caad-cef-endpoint-enable-auditor
  Vendor = Quest Software
  ParserVersion = "v1.0.0"
  Product = Quest Change Auditor For Active Directory
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """Quest Software""", """|Change Auditor|""", """|Active Directory|""", """Computer account enabled""" ]
  Fields = [
    """start=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """dvchost=({host}[\w\-.]+)""",
    """domain=({domain}\S+)""",
    """categoryOutcome=({result}\S+)""",
    """src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """userMail=({email_address}[^@=]+@[^\.]+[^\s]+)""",
    """suid=({user_sid}\S+)""",
    """suser=(({domain}[^\\\/]+)[\\\/]*)?({user}[^=]+?)\s\w+=""",
    """event=({event_name}[^=]+?)\s\w+=""",
    """msg=({additional_info}[^=]+?)\s*\w+=""",
    """msg=The computer account\s*({user_ou}[^$]+?)\s*was enabled"""
  ]


}
```