#### Parser Content
```Java
{
Name = questsoftware-caad-cef-app-activity-appactivity
  Vendor = Quest Software
  Product = Quest Change Auditor for Active Directory
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
    """CEF:""",
    """Quest Software""",
    """|Change Auditor|"""
  ]
  Fields = [
    """({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d+(\+|-)\d+:\d+)""",
    """dvchost=({host}[\w\-.]+)""",
    """domain=({domain}[^\s=]+)""",
    """categoryOutcome=({result}[^\s=]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """userMail=({email_address}[^@=]+@[^\.]+[^\s]+)""",
    """suid=({user_sid}[^\s=])+""",
    """suser=(({domain}[^\\]+)\\*)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s\w+=""",
    """event=({operation}({event_name}[^=]+?))\s\w+=""",
    """msg=({additional_info}[^=]+?)\s*\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```