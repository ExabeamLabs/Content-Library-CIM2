#### Parser Content
```Java
{
Name = "salesforce-sf-cef-file-download-success-cloud"
  Vendor = "Salesforce"
  Product = "Salesforce"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
    """|resource-downloaded|"""
    """destinationServiceName =Sales Cloud"""
  ]
  Fields = [
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ) \S+ """,
    """([^\|]*\|){5}({action}[^\|]+)""",
    """\Wsuser=(({domain}[^\\\s@;=]+)\\+)?(system|({user}[\w\.\-]{1,40}\$?))\s+(\w+=|$)""",
    """\Wsuser=({email_address}[^@\s;]+?@[^@\s;]+)\s*(\w+=|$)""",
    """\Wfname=({file_name}.+?(?:\.(null|({file_ext}[^.]+?)))?)\s+(\w+=|$)""",
    """\WfileType=({file_type}.+?)\s+(\w+=|$)""",
    """\WdestinationServiceName =({app}.+?)\s*(\w+=|$)"""
    """filePath=({file_path}[^=]+?)\s+\w+="""
    """Owner\.Name\\?=({full_name}({first_name}[^\s]+)\s({last_name}[^;]+))"""
  ]
   DupFields = [
    "host->dest_host"
   ]
  ParserVersion = "v1.0.0"


}
```