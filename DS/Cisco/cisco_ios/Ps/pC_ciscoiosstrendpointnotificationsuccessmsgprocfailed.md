#### Parser Content
```Java
{
Name = cisco-ios-str-endpoint-notification-success-msgprocfailed
  Vendor = Cisco
  Product = Cisco IOS
  TimeFormat = "MMM dd HH:mm:ss"
  Conditions = [ """: %MM_INFRA_LOG-3-MSG_PROC_FAILED: """, """: mobilityd: """, """ reason:""" ]
  ParserVersion = "v1.0.0"
  Fields = [
    """({time}\w{3}\s\d\d\s\d\d:\d\d:\d\d)\s({host}[\w\-\.]+)\s\d+:""",
    """\sfrom ipv4:\s({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s""",
    """\sreason:\s*({failure_reason}[^"$]+)\s*$"""
    """%MM_INFRA_LOG-3-MSG_PROC_FAILED:\s*({additional_info}[^"$]+?)\s*$"""
  ]


}
```