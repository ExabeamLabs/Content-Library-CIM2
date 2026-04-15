#### Parser Content
```Java
{
Name = "dell-ppdm-kv-app-activity-success-catchall"
Vendor = "Dell"
Product = "PowerProtect Data Manager"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
    """user-""",
    """ monitoring """,
    """[]""",
    """ Details:"""
  ]
Fields = [
    """\s+({time}\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}\.\d{3}Z)\s+"""
    """\[TRACE_ID:({tracking_id}[^\]]+)\]"""
    """\d\d:\d\d:\d\d\s({host}[\w_\-\.]+)\s\w"""
    """\sDetails:\s({operation_details}[^;]+);"""
    """\sSummary:\s({description}[^;]+);"""
    """virtual machine\s'({vm_host_name}[^;']+)"""
    """Recommended Action:\s({additional_info}[^;]+);"""
]
ParserVersion = "v1.0.0"


}
```