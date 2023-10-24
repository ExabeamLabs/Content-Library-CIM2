#### Parser Content
```Java
{
Name = pan-gp-cef-vpn-logout-success-logoutuserid
  Vendor = Palo Alto Networks
  Product = GlobalProtect
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """globalprotect """, """|logout|USERID|""" ]
  Fields = [
    """end=({time}\d{4}\/\d{2}\/\d{2}\s(\d{2}:){2}\d{2})\s""",
    """\srt=({time}\d{13})""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """({event_name}logout)""",
    """duser=(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-]{1,40}\$?)""",
    """dvchost=({src_host}[\w.-]+?)\s""",
    """GPStatus=({result}\S+?)\s""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]


}
```