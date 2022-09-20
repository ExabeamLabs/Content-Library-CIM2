#### Parser Content
```Java
{
Name = questsoftware-caad-cef-endpoint-login-sessionended
  ParserVersion = "v1.0.0"
  Vendor = Quest Software
  Product = Quest Change Auditor for Active Directory
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """Quest Software""", """|Change Auditor|""", """|Logon Activity|""", """A user session was ended by user logging off""" ]
  Fields = [
    """start=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """dvchost=({host}[\w\-.]+)""",
    """domain=({domain}\S+)""",
    """categoryOutcome=({result}\S+)""",
    """src=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """userMail=({email_address}[^@=]+@[^\.]+[^\s]+)""",
    """suid=({user_sid}\S+)""",
    """suser=(({domain}[^\\]+)\\\\)?({user}[^=\\]+?)\s\w+=""",
    """event=({event_name}[^=]+?)\s\w+=""",
    """msg=({additional_info}[^=]+?)\s*\w+="""
  ]


}
```