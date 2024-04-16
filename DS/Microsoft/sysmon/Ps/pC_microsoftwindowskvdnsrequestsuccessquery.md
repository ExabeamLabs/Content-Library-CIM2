#### Parser Content
```Java
{
Name = microsoft-windows-kv-dns-request-success-query
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = [ "yyyy-MM-dd HH:mm:ss.SSS", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ" ]
  Conditions = [
"""QueryName:""",
"""QueryResults:""",
"""ProcessGuid:""",
"""Image:"""
  ]
  Fields = [
    """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{6}[\+\-]\d{1,2}:\d{1,2})\s({host}[\w\-.]+)\s""",
    """UtcTime:\s*({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)\s""",
    """QueryName:\s*({dns_query}[^\\\s]+)""",
    """ProcessGuid:\s*\{({process_guid}[A-F0-9a-f-]+)\}""",
    """ProcessId:\s*({process_id}\d+)""",
    """QueryResults:\s({dns_response}.+?)\sImage:""",
    """Image:\s*(?:<unknown process>|({process_path}({process_dir}[^\"]*[\\/]+)?({process_name}[^\"\\/]+)))\s"""
  ]


}
```