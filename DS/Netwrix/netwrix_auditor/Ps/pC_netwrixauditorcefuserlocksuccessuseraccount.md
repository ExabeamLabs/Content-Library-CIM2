#### Parser Content
```Java
{
Name = netwrix-auditor-cef-user-lock-success-useraccount
  ParserVersion = v1.0.0
  Vendor = Netwrix
  Product = Netwrix Auditor
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:0|Netwrix|Active Directory|""", """msg=User Account Locked Out """ ]
  Fields = [
    """start=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """suser=(N\/A|({email_address}[^@]+@[^\\\s]+)|(({domain}[^\\\s]+)\\+)?({user}[\w\.\-]{1,40}\$?)) """,
    """shost=(unknown|({src_host}[^\s]+))""",
    """({app}Netwrix)""",
    """msg=({additional_info}.+?)(\s\w+=|$)""",
    """CEF:0\|Netwrix\|Active Directory\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|""",
    """cat=user.+?filePath=\\+?([^\\]+\\+)*?({dest_user}[^\\]+) start=""",
  ]
ParserVersion = "v1.0.0"


}
```