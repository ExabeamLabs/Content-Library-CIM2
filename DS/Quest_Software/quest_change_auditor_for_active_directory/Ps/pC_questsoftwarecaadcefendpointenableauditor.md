#### Parser Content
```Java
{
Name = questsoftware-caad-cef-endpoint-enable-auditor
  Vendor = Quest Software
  ParserVersion = "v1.0.0"
  Product = Quest Change Auditor for Active Directory
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """Quest Software""", """|Change Auditor|""", """|Active Directory|""", """Computer account enabled""" ]
  Fields = [
    """start=({time}\w+\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
    """dvchost=({host}[\w\-.]+)""",
    """domain=({domain}\S+)""",
    """categoryOutcome=({result}\S+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """userMail=({email_address}[^@=]+@[^\.]+[^\s]+)""",
    """suid=({user_sid}\S+)""",
    """suser=(({domain}[^\\\/]+)[\\\/]*)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
    """event=({event_name}[^=]+?)\s\w+=""",
    """msg=({additional_info}[^=]+?)\s*\w+=""",
    """msg=The computer account\s*({user_ou}[^$]+?)\s*was enabled"""
  ]


}
```