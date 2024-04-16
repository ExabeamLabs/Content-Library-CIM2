#### Parser Content
```Java
{
Name = "salesforce-sf-cef-file-upload-success-cloud-1"
  Vendor = "Salesforce"
  Product = "Salesforce"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ParserVersion = "v1.0.0"
  Conditions = [
     """type\=Document;"""
     """IsPublic\="""
     """Name\="""
  ]
  Fields = [
    """CreatedDate\\?=({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\S+""",
    """CreatedBy\.Username\\?=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|;]+\.[^\]\s"\\,\|;]+)|({user}[\w\.\-]{1,40}\$?);)""",
    """msg=({additional_info}[^=]+?)\s\w+="""
    """\Wfname=({src_file_name}.+?(?:\.({file_ext}[^".]+?))?)\s+(\w+=|$)""",
    """\WfileType=({file_type}.+?)\s+(\w+=|$)""",
    """\WdestinationServiceName =({app}.+?)\s*(\w+=|$)""",
    """CreatedBy.Name\\?=({full_name}[^=]+?);?\w+\\?=""",
    """dproc=({action}[\w-]+)"""
    """filePath=({file_path}[^=]+?)\s+\w+="""
    """CEF:([^\|]*\|){5}({operation}resource-uploaded)"""
   ]
  DupFields = [
    "src_file_name->file_name"
  ]


}
```