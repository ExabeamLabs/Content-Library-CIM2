#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-notification-success-general
  ParserVersion = "v1.0.0"
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
  Conditions = [ """,SYSTEM,""", """,general,"""]
  Fields = [
    """,general,([^,]*,){9}({host}[\w\-.]+)""",
    """({host}[\w\-\.]+)[\s\-]+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,SYSTEM,.*?,""",
    """Client\s'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """,SYSTEM,([^,]*,){3},({operation}[^,]+),""",
    """,general,(|({log_severity}[^,]+)),"*({additional_info}[^",]+?)"*,""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    """({serial_num}\d+),SYSTEM,"""
    """,SYSTEM,([^,]*,){18}({device_name}[^",]+)"""
  ]


}
```