#### Parser Content
```Java
{
Name = imperva-securesphere-cef-app-activity-systemevent
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
  event_timeFormat = ["yyyy-MM-dd'T'HH:mm:ss"]
  Conditions = [
    """|Imperva Inc""",
    """SecureSphere""",
    """cat=SystemEvent"""
  ]
  Fields = ${ImpervaParserTemplates.securesphere-system.Fields}[
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d\d:\d\d)\s+({host}[\w.\-]+)\s*""",
    """cat=({category}\S+)""",
    """requestIP=(?:"|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\|SecureSphere\|({version}[^|]+)\|({event_category}[^|]+)\|({event_name}[^|]+)\|""",
# session_info is removed
    """rt=({event_time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""
  ]
  ParserVersion = "v1.0.0"

securesphere-system = {
  Vendor = Imperva
  Product = Imperva SecureSphere
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
     """\(({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)""",
     """SecureSphere\|[^|]+?\|({operation}[^\|]+)\|({event_name}[^\|]+)\|({severity}[^\|]+)\|\s*suser=(({last_name}[^,]+),\s*({first_name}.+?)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\srt"""
  ]
 
}
```