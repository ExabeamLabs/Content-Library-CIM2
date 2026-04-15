#### Parser Content
```Java
{
Name = tanium-cpp-kv-app-login-success-createobject
  Vendor = Tanium
  Product = Tanium Cloud Platform
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """type_name=""", """"CreateObject"""", """object_type_name=""", """"authentication"""", """object_name=""", """audit_name=""", """details=""" ]
  ParserVersion = v1.0.0
  Fields = [
    """\Wcreation_time="\w+ ({time}\w{3} \d\d \d\d\d\d \d\d:\d\d:\d\d)\s""",  
    """\Wdetails\s*=\s*"({additional_info}[^"]+)"""",
    """\Wobject_type_name\s*=\s*"({object_type}[^"]+)"""",
    """IP Address\s*:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?(\s|"|;)""",
    """\Wtype_name\s*=\s*"({operation}[^"]+)"""",
    """\Waudit_name\s*=\s*"({event_name}[^"]+)"""",
    """Session ID:\s({session_id}\d+)""",
    """\Waudit_type\s*=\s*"({audit_subcategory}[^"]+)""""
  ]


}
```