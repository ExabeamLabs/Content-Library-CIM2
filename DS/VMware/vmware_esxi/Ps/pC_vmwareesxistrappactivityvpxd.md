#### Parser Content
```Java
{
Name = vmware-esxi-str-app-activity-vpxd
  Vendor = VMware
  Product = VMware ESXi
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""] [""", """ vpxd """, """Event [""" ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)[^\s]+\s+({host}[^\s]+)\s""",
    """Event\s*(\[[^\]]*\]\s+){2}({additional_info}[^\]\}]+?)\s*$""",
    """Event\s*(\[[^\]]*\]\s+){8}\[({additional_info}[^\]]+?)\s*\]"""
    """Event\s*(\[[^\]]*\]\s+){8}\[({event_name}[^"]+)\s+for user"""
    """Event\s*(\[[^\]]*\]\s+){8}\[([^"]+)for user\s(({domain}[^\\\s]+)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s"""
    """Event\s*(\[[^\]]*\]\s+){8}\[({event_name}[^\]]+)\s(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)(?<!local)(?<!loc)(?<!localdomain))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^,]+))?)\sfrom\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
  ]


}
```