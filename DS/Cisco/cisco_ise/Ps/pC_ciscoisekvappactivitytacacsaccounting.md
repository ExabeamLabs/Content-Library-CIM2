#### Parser Content
```Java
{
Name = cisco-ise-kv-app-activity-tacacsaccounting
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CISE_TACACS_Accounting""", """Tacacs-Accounting""", """Device IP Address="""]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\.\d+""",
    """({host}[^\s]+)\sCISE_TACACS_Accounting""",
    """Device IP Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """CmdAV=({command}[^,]+)\s],""",
    """Privilege-Level=({privileges}[^,]+),""",
    """({app}TACACS\+ Accounting)""",
    """TACACS\+\s*({operation}Accounting with Command)""",
    """NetworkDeviceName =({src_host}[\w\-\.]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```