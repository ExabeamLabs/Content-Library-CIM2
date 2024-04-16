#### Parser Content
```Java
{
Name = juniper-srx-str-network-traffic-success-sessioncreated
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "MMM dd yyyy HH:mm:ss Z"
  Conditions = [ """RT_FLOW_SESSION_CREATE: session created""", """ testbed-untrust """, """ testbed-trust """ ]
  Fields = [
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d \+\d\d:\d\d)\s+RT_FLOW_SESSION_CREATE:\s+({event_name}session created)\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)->({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)\s+(None|junos-({protocol}[^\s]+))\s+({src_translated_ip}[\da-fA-F.:]+)\/({src_translated_port}\d+)->({dest_translated_ip}[\da-fA-F.:]+)\/({dest_translated_port}\d+)\s+({rule}[^\s]+\srule)(\s+\S+){4}\s({policy_name}[^\s]+)(\s+\S+){4}\s+({src_interface}[^\s]+)""",
  ]


}
```