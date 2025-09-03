#### Parser Content
```Java
{
Name = "egnyte-e-cef-file-permission-modify-success-assigner"
  Vendor = "Egnyte"
  Product = "Egnyte"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
     """destinationServiceName =Egnyte"""
     """dproc=permissions-audit-report"""
     """time"""
     """assigner""" 
  ]
  Fields = [
    """"time":"({time}\d+-\d+-\d+T\d+:\d+:\d+Z)""",
    """"assigner":"[^"\(]+\(\s*({email_address}[^@\(\)]+@[^\.\s@\(\)]+\.[^"\)]+?)\s*\)?"""",
    """"assignee":"({object}[^"]+)""",
    """"folder":"({file_path}({file_dir}[^"]*?[\\\/]+)({file_name}[^"\\\/]+?(\.({file_ext}[^"\.\\\/]+))?)?)\s*"""",
    """({access}ACL was.*?with permission\s+\[[^\]]*\])""",
    """destinationServiceName =({service_name}[^"]+?)\s+(\w+=|$)""",
    """({app}Egnyte)"""
  ]
  DupFields = [
    "dproc->category"
  ]
  ParserVersion = "v1.0.0"


}
```