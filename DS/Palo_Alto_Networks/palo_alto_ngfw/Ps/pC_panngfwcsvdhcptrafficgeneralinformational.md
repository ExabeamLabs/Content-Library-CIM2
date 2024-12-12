#### Parser Content
```Java
{
Name = pan-ngfw-csv-dhcp-traffic-generalinformational
  ParserVersion = v1.0.0
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
  Conditions = [ """,SYSTEM,dhcp,""", """,general,informational,"""]
  Fields = [
    """({host}[\w\-\.]+)[\s\-]+\d+,({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d),[^,]*,SYSTEM,dhcp""",
    """,SYSTEM,dhcp,([^,]+,){2},({operation}[^,]+)""",
    """,general,informational,"+({event_name}DHCP lease)\s+started ip\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+-->\s+mac\s+({src_mac}[^\s]+)\s+-\s+hostname\s+({device_name}[^\s]+),\s+interface\s+({interface_name}[^"]+)""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
    """({serial_num}\d+),SYSTEM,dhcp"""
    """SYSTEM,([^,]*,){17,18},({device_name}({host}[^",]+))"""
  ]


}
```