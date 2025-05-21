#### Parser Content
```Java
{
Name = pan-gp-cef-app-notification-success-globalprotect
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss zzz"
  Conditions = ["""|gateway-config-release|GLOBALPROTECT|""", """GLOBALPROTECT""", ]
  Fields = [
    """GPClientHostName =({host}[^=]*?)(\s+)?\w+?=""",
    """rt=({time}\w{3}\s\d{2}\s\d{4}\s(\d{2}:){2}\d{2}\s\S{3})\s""",
    """GPClientPrivateIPv4=({src_translated_ip}[A-Fa-f0-9.:]+)""",
    """ClientPublicIPv4=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """GPSourceUser=(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
    """dvchost=({src_host}[\w.-]+?)\s""",
    """GPClientOS=({os}[^=]*?)(\s+)?\w+?=""",
    """msg="({additional_info}[^"]+?)"""",
    """({app}GLOBALPROTECT)""",
    """({event_name}gateway-config-release)"""
  ]


}
```