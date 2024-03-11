#### Parser Content
```Java
{
Name = servicenow-s-cef-file-syscreated
  ParserVersion = v1.0.0
  Vendor = ServiceNow
  Product = ServiceNow
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = ["""destinationServiceName =ServiceNow""", """"sys_created_on"""", """"sys_created_by""""]
  Fields = [
    """"sys_created_on"+:"+({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """({app}ServiceNow)""",
    """"srcip"+:"+({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"name"+:"+({event_name}[^",]+)""",
    """"user(_name)?"+:"+(({email_address}[^@"]+@({email_domain}[^.]+\.[^"]+))|({user}[^",]+))""",
    """"queue"+:"+({operation}[^",]+)""",
    """"parm1"+:"+\s*(|-|({resource}[^"]+?))\s*"+,""",
    """"(instance|documentkey)"+:"+({object}[^"]+?)"+,""",
    """"tablename"+:"+({table_name}[^"]+)"+,""",
    """"table"+:"+({table}[^"]+)"+,""",
    """"parm2"+:"+\s*({action}[^"]+?)\s*"+,""",
    """"file_name"+:"+({file_name}[^"]+?(\.({file_ext}[^\."]+))?)"+,""",
    """"size_bytes"+:"+({bytes}\d+)""",
    """"content_type"+:"+({file_type}[^"]+?)"+,""",
    """"oldvalue"+:"+\s*({old_value}[^"]+?)\s*",""",
    """newvalue"+:"\s*({new_value}[^"]+?)\s*"+,""",
    """dproc=({dproc}[^=]+)\s+\w+"""
  ]
  DupFields = [ "file_name->object", "operation->access" ]


}
```