#### Parser Content
```Java
{
Name = "pan-gp-csv-endpoint-authentication-success-panoramaauthsuccess"
  Vendor = "Palo Alto Networks"
  Product = "GlobalProtect"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy/MM/dd HH:mm:ss"]
  Conditions = [
"""panorama-auth-success""",
""",SYSTEM,tls,"""
  ]
  Fields = [
"""\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),"""
"""Client IP:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""Server IP:\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
"""((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
"""({serial_num}\d+),SYSTEM,tls,"""
""",SYSTEM,tls,([^,]*,){17}({device_name}({host}[^,"]+))"""
  ]
  ParserVersion = "v1.0.0"


}
```