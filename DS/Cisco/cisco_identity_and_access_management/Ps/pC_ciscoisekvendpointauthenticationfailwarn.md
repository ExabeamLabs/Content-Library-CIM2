#### Parser Content
```Java
{
Name = cisco-ise-kv-endpoint-authentication-fail-warn
  ParserVersion = "v1.0.0"
  Vendor = Cisco
  Product = Cisco Identity and Access Management
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS Z"
  Conditions = [""" CISE_RADIUS_Diagnostics """,""" WARN """]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d\.\d\d\d\s[+-]\d\d:\d\d)""",
    """({host}[\w\-.]+)\s({additional_info}CISE_RADIUS_Diagnostics)""",
    """\s({event_code}\d+)\sWARN""",
    """User-Name =(({domain}[^\\=]+)\\\\)?(({email_address}[^@=]+?@[^\.]+\.[^,]+)|([^\/=]+\/({src_host}[^,]+))|(USERNAME|INVALID|Anonymous identity|([\da-fA-F]{2}-){5}[\da-fA-F]{2}|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),""",
    """WARN\s+({event_name}[^=]+),\s\w+=""",
    """Device IP Address=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """Device Port=({src_port}\d+)""",
    """DestinationIPAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """DestinationPort=({dest_port}\d+)""",
# radius_packet_type is removed
  ]


}
```