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
    """CEF:([^\|]*\|){5}({operation}[^\|]+)""",
    """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\\s@;=]+)\\+)?(system|anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+(\w+=|$)""",
    """\Wfname=({file_name}.+?(?:\.(null|({file_ext}[^.\s=]+?)))?)\s+(\w+=|$)""",
    """\WfileType=({file_type}.+?)\s+(\w+=|$)""",
    """\WdestinationServiceName =({app}.+?)\s*(\w+=|$)"""
    """filePath=({file_path}[^=]+?)\s+\w+="""
    """Owner\.Name\\?=({full_name}({first_name}[^\s]+)\s({last_name}[^;]+))"""
    """msg=({additional_info}[^=]+?)\s\w+="""
  ]
  ParserVersion = "v1.0.0"


}
```