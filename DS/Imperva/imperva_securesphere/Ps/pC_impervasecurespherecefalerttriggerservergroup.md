#### Parser Content
```Java
{
Name = imperva-securesphere-cef-alert-trigger-servergroup
  Vendor = Imperva
  Product = Imperva SecureSphere
 ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """CEF:""", """|Imperva Inc.|SecureSphere""", """cat=Alert""", """cs1Label=ServerGroup""" ]
  Fields = [
    """\Wrt=({time}\w+ \d+ \d{4} \d\d:\d\d:\d\d)""",
    """\Wsrc=\s*(0.0.0.0|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)""",
    """\Wdst=\s*(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """\Wduser=(?:n\/a|(({domain}[^\\\s"]+)\\+)?({user}[\w\.\-]{1,40}\$?))\s+(\w+=|$)""",
    """\Wcs1=(|({server_group}.+?))\s+(\w+=|$)""",
    """\Wcs2=(|({service_name}.+?))\s+(\w+=|$)""",
    """\Wcs3=(|({app}.+?))\s+(\w+=|$)""",
    """CEF:([^\|]*\|){5}({alert_name}[^\|]+)""",
    """CEF:([^\|]*\|){6}({alert_severity}[^\|]+)""",
  ]
  DupFields = [ "alert_name->alert_type" ]


}
```