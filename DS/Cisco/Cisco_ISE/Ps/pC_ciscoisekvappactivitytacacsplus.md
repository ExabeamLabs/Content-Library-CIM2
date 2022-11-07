#### Parser Content
```Java
{
Name = cisco-ise-kv-app-activity-tacacsplus
  Vendor = Cisco
  Product = Cisco ISE
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CISE_TACACS_Accounting""", """Tacacs-Accounting:""", """Device IP Address=""", """Authen-Method=TacacsPlus"""]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)\.\d+""",
    """({host}[^\s]+)\sCISE_TACACS_Accounting""",
    """Device IP Address=({src_ip}[a-fA-F:\d.]+),""",
    """Remote-Address=(0.0.0.0|({dest_ip}[a-fA-F:\d.]+)),""",
    """CmdAV=({operation}[^,]+)\s<cr>\s\],""",
    """Privilege-Level=({privileges}[^,]+),""",
    """({app}TACACS\+ Accounting)""",
    """\sUser=(({email_address}[^\s]+?@[^\s]+?)|({user}[^,]+)),"""
  ]
  ParserVersion = "v1.0.0"


}
```