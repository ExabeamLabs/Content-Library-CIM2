#### Parser Content
```Java
{
Name = "epic-siem-cef-app-login-success-login"
  ParserVersion = "v1.0.0"
  Vendor = "Epic"
  Product = "Epic SIEM"
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|Epic|Security-SIEM|""", """|LOGIN|""" ]
  Fields = [
    """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
    """({host}[\w\-.]+)\s+CEF:""",
    """LOGINLDAPID=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """workstationID=({dest_host}[\w\-.]+)""",
    """shost=({src_host}[\w\-.]+)""",
    """IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """ROLE=({additional_info}.+?)(\s+\w+=|\s*$)""",
    """USERJOB=(|({resource}.+?))\s+(\w+=|$)""",
  ]


}
```