#### Parser Content
```Java
{
Name = sap-s-cef-app-login-fail-dialoglogonfailed
  ParserVersion = v1.0.0
  Product = SAP
  Conditions = [ """CEF:""", """|SECUDE|C-Bus|""", """dvchost=""", """|AU2|Dialog Logon Failed|""" ]

sap-login-activity = {
  Vendor = SAP
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """dvchost=({host}[^\s]+)""",
    """dvc=({host_ip}[a-fA-F\d:.]+)""",
    """end=({time}\w+\s\d+\s\d+\s\d\d:\d\d:\d\d)""",
    """SECUDE\|C-Bus\|[^\|]+\|({activity_id}[^\|]+)\|({event_name}[^\|]+)\|""",
    """suser=({user}[^\s]+)\s\w+=""",
    """shost=(({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+))|({src_host}[^\s]+))""",
    """cat=({category}[^=]+?)(\s\w+=|\s*$)""",
    """requestClientApplication=({app}[^"]+?)\s\w+=""",
    """msg=({additional_info}[^"]+?)\s+\w+="""
  ]
  DupFields = [ "activity_id->event_code" 
}
```