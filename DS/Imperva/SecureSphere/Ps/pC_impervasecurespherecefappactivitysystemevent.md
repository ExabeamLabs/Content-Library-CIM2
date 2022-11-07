#### Parser Content
```Java
{
Name = imperva-securesphere-cef-app-activity-systemevent
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  Conditions = [
    """|Imperva Inc""",
    """SecureSphere""",
    """cat=SystemEvent"""
  ]
  Fields = ${ImpervaParserTemplates.securesphere-system.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)\s*""",
    """cat=({category}\S+)""",
    """requestIP=(?:"|({src_ip}[A-Fa-f:\d.]+))""",
    """\|SecureSphere\|({version}[^|]+)\|({event_category}[^|]+)\|({event_name}[^|]+)\|""",
# session_info is removed
    """rt=({event_time}\S+)"""
  ]
  ParserVersion = "v1.0.0"

securesphere-system = {
  Vendor = Imperva
  Product = SecureSphere
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
     """\(({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)""",
     """SecureSphere\|[^|]+?\|({operation}[^\|]+)\|({event_name}[^\|]+)\|({severity}[^\|]+)\|\s*suser=(({last_name}[^,]+),\s*({first_name}.+?)|({user}[^\s].+?))\srt"""
  ]
 
}
```