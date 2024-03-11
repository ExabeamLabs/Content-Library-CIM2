#### Parser Content
```Java
{
Name = pan-gp-cef-app-notification-success-hipmatch
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  TimeFormat = "MMM dd yyyy HH:mm:ss zzz"
  Conditions = [ """CEF:""", """|Palo Alto Networks|PAN-OS|""", """|HIPMATCH|""", """PanOSVsysName =""", """PanOSActionFlags=""" ]
  Fields = [
    """\s({host}[\w\-.]+?)\sCEF:""",
    """\sdvchost=({host}[\w\-.]+)""",
    """\|rt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d\s\w{3})""",
    """suser=(({domain}[^\\=]+)\\+)?({user}[^=]+?)\s\w+=""",
    """\sshost=({src_host}[\w\-.]+)\s""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\s+\w+=""",
    """\scat=({category}[^=]+)\s+\w+=""",
    """\scs2=({os}[^=]+)\s+\w+=""",
    """PanOSActionFlags=({action_flags}[^\s]+)\s""",
    """cs3=({virtual_system}[^=]+)\s+\w+=""",
    """PanOSHostID=({host_id}[\w\-]+)""",
    """\|({subtype}[^\|]+?)\|({event_category}HIPMATCH)\|"""
  ]
  ParserVersion = "v1.0.0"


}
```