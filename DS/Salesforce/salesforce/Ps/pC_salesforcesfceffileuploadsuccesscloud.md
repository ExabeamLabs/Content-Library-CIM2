#### Parser Content
```Java
{
Name = "salesforce-sf-cef-file-upload-success-cloud"
  Vendor = "Salesforce"
  Product = "Salesforce"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [
     """attachment-upload"""
     """destinationServiceName =Sales Cloud"""
  ]
  Fields = [
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\S+""",
    """([^\|]*\|){5}({access}[^\|]+)""",
    """([^\|]*\|){5}({action}[^\|]+)""",
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\S+""",
    """\Wsuser=(({domain}[^\\\s@;=]+)\\+)?(system|({user}[^\\\=\s;@]+))\s+(\w+=|$)""",
    """\Wsuser=({email_address}[^@\s;]+?@[^@\s;]+)\s*(\w+=|$)""",
    """\Wfname=({src_file_name}.+?(?:\.({file_ext}[^".]+?))?)\s+(\w+=|$)""",
    """\WfileType=({file_type}.+?)\s+(\w+=|$)""",
    """\WdestinationServiceName =({app}.+?)\s*(\w+=|$)""",
   ]
  DupFields = [
    "host->dest_host"
    "src_file_name->file_name"
  ]
  ParserVersion = "v1.0.0"


}
```