#### Parser Content
```Java
{
Name = microsoft-windows-kv-dns-request-success-query
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Sysmon
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
  Conditions = [
"""QueryName:""",
"""QueryResults:""",
"""ProcessGuid:""",
"""Image:"""
  ]
  Fields = [
    """UtcTime:\s*({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d)\s""",
    """QueryName:\s*({dns_query}[^\\\s]+)""",
    """ProcessGuid:\s*\{({process_guid}[A-F0-9a-f-]+)\}""",
    """ProcessId:\s*({process_id}\d+)""",
    """QueryResults:\s({dns_response}.+?)\sImage:""",
    """Image:\s*(?:<unknown process>|({process_path}({process_dir}[^\"]*[\\/]+)?({process_name}[^\"\\/]+)))\s"""
  ]


}
```