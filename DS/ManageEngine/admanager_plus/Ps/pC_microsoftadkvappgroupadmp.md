#### Parser Content
```Java
{
Name = microsoft-ad-kv-app-group-admp
  Vendor = ManageEngine
  Product = ADManager Plus
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """ADMP""", """Status=""" ]
  Fields = [
    """({time}\d+-\d+-\d+T\d+:\d+:\d+.\d+Z)\s*({host}[^\s]+)""",
    """\[Status=({result}[^]]+)\]""",
    """\[TechnicianName =(\([^[\)]+\)\s*)?({user}[^]]+)\]""",
    """\[Task=({operation}[^]]+)\]""",
    """\[ACTION=({action}[^]]+)\]""",
    """\[accountExpires=({account}[^]]+)\]""",
    """\[Template Name =({event_name}[^]]+)\]""",
    """\[Object Name =({object}[^]]+)\]""",
# domain_name is removed
    """\[memberOf=\[({group_name}[^]]+)]]""",
    """\[Object Name =(\([^[\)]+\)\s*)?({account}[^]]+)\]""",
  ]


}
```