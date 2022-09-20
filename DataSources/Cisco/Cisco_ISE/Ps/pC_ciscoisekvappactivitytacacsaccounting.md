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
    """Device IP Address=({src_ip}[a-fA-F:\d.]+),""",
    """CmdAV=({operation}[^,]+)\s<cr>\s\],""",
    """Privilege-Level=({privileges}[^,]+),""",
    """({app}TACACS\+ Accounting)""",
  ]
  ParserVersion = "v1.0.0"


}
```