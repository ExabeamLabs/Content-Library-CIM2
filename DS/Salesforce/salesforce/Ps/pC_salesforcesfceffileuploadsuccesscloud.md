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
    """([^\|]*\|){5}({operation}[^\|]+)""",
    """({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\S+""",
    """\Wsuser=(({domain}[^\\\s@;=]+)\\+)?(system|({user}[\w\.\-]{1,40}\$?))\s+(\w+=|$)""",
    """\Wsuser=({email_address}[^@\s;]+?@[^@\s;]+)\s*(\w+=|$)""",
    """\Wfname=({file_name}.+?(?:\.({file_ext}[^".]+?))?)\s+(\w+=|$)""",
    """\WoldFileName =({src_file_name}.+?)\s*(\w+=|$)"""
    """\WfileType=({file_type}.+?)\s+(\w+=|$)""",
    """\WdestinationServiceName =({app}.+?)\s*(\w+=|$)""",
    """filePath=({file_path}[^=]+?)\s+\w+="""
    """dproc=({action}[\w-]+)"""
    """([^\|]*\|){5}({access}resource-uploaded)"""
    """Owner\.Name\\?=({full_name}({first_name}[^\s]+)\s({last_name}[^;]+))"""
   ]
  DupFields = [
    "host->dest_host"
  ]
  ParserVersion = "v1.0.0"


}
```