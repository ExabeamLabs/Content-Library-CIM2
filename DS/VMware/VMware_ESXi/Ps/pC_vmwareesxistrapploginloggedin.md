#### Parser Content
```Java
{
Name = vmware-esxi-str-app-login-loggedin
  ParserVersion = v1.0.0
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [""" logged in """, """ : User """, """ hostd[""", """ Hostd:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d.\d+Z)\s+({host}[^\s]+)\sHostd:""",
    """User\s+((({domain}[^\\\s@]+)\\+)?({user}[^\s\\@]+))[^$]+?\s*logged""",
    """({event_name}logged in)""",
    """logged in as ({user_agent}\S+)""",
    """user agent:\s+({user_agent}[^)]+)""",
    """: User\s\w+@({src_ip}[A-Fa-f:\d.]+)"""
  ]
  DupFields = [ "host->dest_host" ]


}
```