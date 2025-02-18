#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-traffic-packet
  ParserVersion = v1.0.0 
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSZ","yyyy/MM/dd HH:mm:ss"]
  Conditions = [
""",THREAT,packet,""",
""",client""",
""",,"""
  ]
  Fields = [
    """THREAT,([^,]*,){27}("[^"]+")?,([^,]*,){27}({device_name}({host}[^",]+))""",
    """\w+\s+\d+\s+\d+:\d+:\d+\s+({host}[\w\-.]+)\s+\d+,""",
    """,({time}\d+\/\d+\/\d+\s+\d+:\d+:\d+),({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),""",
    """,\d+\/\d+\/\d+\s+\d+:\d+:\d+,\d+,\d+,({src_port}\d+),({dest_port}\d+),\d*,\d*,\w*,({protocol}[^\s,]+),({result}[^,]+),[^,]*,({additional_info}[^,]+),[^,]*,({severity}[^,]*),({direction}[^,]*),""",
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))""",
    """THREAT,([^,]*,){4}({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?,""",
    """THREAT,([^,]*,){5}({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_translated_port}\d+))?,""",
    """THREAT,([^,]*,){10}(not-applicable|({network_app}[^,]+)),""",
    """THREAT,([^,]*,){12}({src_network_zone}[^,]+),""",
    """THREAT,([^,]*,){13}({dest_network_zone}[^,]+),""",
    """THREAT,([^,]*,){14}({src_interface}[^,]+),""",
    """THREAT,([^,]*,){15}({dest_interface}[^,]+),""",
    """({serial_num}[^,]+),THREAT,"""
  ]


}
```