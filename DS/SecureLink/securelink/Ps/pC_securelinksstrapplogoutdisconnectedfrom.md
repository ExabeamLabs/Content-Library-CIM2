#### Parser Content
```Java
{
Name = securelink-s-str-app-logout-disconnectedfrom
    ParserVersion = "v1.0.0"
    Vendor = SecureLink
    Product = SecureLink
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Conditions = [ """SecureLink""", """ AUDIT""", """ disconnected from """]
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s+({host}[\w\-\.]+)\s""",
      """Application ({app}[^,\(]+?)\s*(\(|,)""",
      """\sAUDIT.+?\(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))\)""",
      """duration ({duration}\w+)""",
      """({event_name}disconnected)"""
    ]
  

}
```