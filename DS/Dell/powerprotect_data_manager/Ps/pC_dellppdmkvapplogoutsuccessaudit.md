#### Parser Content
```Java
{
Name = "dell-ppdm-kv-app-logout-success-audit"
Vendor = "Dell"
Product = "PowerProtect Data Manager"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
    """user-audit""",
    """monitoring""",
    """AUDIT""",
    """logged out""",
    """ Details:"""
  ]
Fields = [
    """\s+({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3}Z)\s+"""
    """Details:\s({user}[\w\.\-\!\#\^\~]{1,40}\$?) logged out\.;"""
    """\[TRACE_ID:({tracking_id}[^\]]+)\]"""
    """\d\d:\d\d:\d\d\s({host}[\w_\-\.]+)\s\w"""
    """\sDetails:\s({operation_details}[^;]+);"""
    """({operation}logged out)"""
]
ParserVersion = "v1.0.0"


}
```