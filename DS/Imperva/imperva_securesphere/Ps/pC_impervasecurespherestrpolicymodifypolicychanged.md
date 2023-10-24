#### Parser Content
```Java
{
Name = imperva-securesphere-str-policy-modify-policychanged
  Vendor = Imperva
  Product = Imperva SecureSphere
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""|Imperva Inc""" , """SecureSphere""" , """cat=SystemEvent""" , """Policy changed|"""]
  Fields = [
    """\(({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d)""",
    """SecureSphere\|[^|]+?\|({operation}[^\|]+)\|({event_name}[^\|]+)\|({severity}[^\|]+)\|\s*suser=(({last_name}[^,]+),\s*({first_name}.+?)|({user}[\w\.\-]{1,40}\$?))\srt"""
  ]
  ParserVersion = "v1.0.0"


}
```