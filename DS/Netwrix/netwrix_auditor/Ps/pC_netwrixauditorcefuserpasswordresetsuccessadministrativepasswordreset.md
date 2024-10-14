#### Parser Content
```Java
{
Name = netwrix-auditor-cef-user-password-reset-success-administrativepasswordreset
  Product = Netwrix Auditor
  Conditions = [ """CEF:0|Netwrix|Active Directory|""", """msg=Administrative Password Reset""" ]
  Fields = ${NetWrixParserTemplates.netwrix-app-activity-2.Fields}[
    """CEF:0\|Netwrix\|Active Directory\|[^\|]+\|[^\|]+\|({operation}[^\|]+)\|""",
    """cat=user.+?filePath=\\*?([^\\]+\\+)*?({dest_user}[^\\]+) start=""",
  ]
  ParserVersion = "v1.0.0"

netwrix-app-activity-2 = {
  Vendor = Netwrix
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """start=({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """suser=(N\/A|(({email_address}[^@]+@[^\\\s]+)|({domain}[^\\\s]+))\\+({user}[\w\.\-\!\#\^\~]{1,40}\$?))\s""",
    """shost=(unknown|({src_host}[^\s]+))""",
    """({app}Netwrix)""",
    """msg=({additional_info}.+?)(\s\w+=|$)""",
  
}
```