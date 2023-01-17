#### Parser Content
```Java
{
Name = exabeam-search-kv-app-notification-serverhealth
  ParserVersion = "v1.0.0"
  Conditions = [ """ Exabeam """, """exabeam-lms-server-health""" ]

exabeam-system-health-alert {
    Vendor = Exabeam
    Product = Search
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields = [
      """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)""",
      """\d\d.\d\d\dZ\s+({event_name}[^\s]+)\s""",
      """app":"({app}[^"]+)""",
      """event_subtype":"({event_subtype}[^"]+)""",
      """src_ip":"({src_ip}[\da-fA-F.:]+)"""",
      """user":"(Unknown|({user}[^"]+))""",
      """host":"({host}[^"]+)""",
      """activity":"({operation}[^"]+)""",
      """additional_info":"({additional_info}.+?)\s*"}}\s"*""",
      """exa_jdbc_database:({db_name}[^\\"\]]+)"""
    
}
```