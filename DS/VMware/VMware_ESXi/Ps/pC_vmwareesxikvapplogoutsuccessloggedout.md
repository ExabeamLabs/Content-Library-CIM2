#### Parser Content
```Java
{
Name = vmware-esxi-kv-app-logout-success-loggedout
  ParserVersion = "v1.0.0"
  Vendor = VMware
  Product = VMware ESXi
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """][""", """ User """, """ logged out """, """ESX""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d).+?\s+({host}[^\s]+)\s""",
    """User\s+((({domain}[^\\\s@]+)\\+)?({user}[^\s\\@]+)).+?\s*logged""",
    """({event_name}logged out)""",
    """user agent:\s*({user_agent}.+?)\s*$"""
    """user agent:\s*(?:-|Mozilla\/.+\(({os}iOS|Android|BlackBerry|Windows Phone|BeOS|(?:X|x)11|(?:W|w)indows|(?:L|l)inux|(?:M|m)acintosh|(?:D|d)arwin).+?({browser}Chrome|Safari|Opera|(?:F|f)irefox|MSIE|Trident))"""
    """({additional_info}User.+?logged out\s.+?)\s*$""",
    """({app}ESX)"""
  ]
  DupFields = [ "event_name->operation", "host->dest_host" ]


}
```