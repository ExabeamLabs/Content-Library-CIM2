#### Parser Content
```Java
{
Name = juniper-srx-str-network-session-fail-sessionclosed
  ParserVersion = v1.0.0
  Vendor = Juniper Networks
  Product = Juniper SRX Series
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ 
"""RT_FLOW_SESSION_CLOSE:"""
"""session closed"""
]
  Fields = [
    """\w+ \d+ \d\d:\d\d:\d\d\s+(|({host}\S+)\s+)RT_FLOW:\s+RT_FLOW_SESSION_CLOSE:\s+({failure_reason}[^:]+):\s+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({src_port}\d+)\->({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))\/({dest_port}\d+)(\s+({result}[^\s]+))?\s+(?:None|({protocol}\S+))\s+({src_translated_ip}[a-fA-F\d.:]+)\/({src_translated_port}\d+)((\S+\s+){7}|(\S+\s+){4})({rule}\S+)\s+(\S+\s+){3,4}\d+\(({bytes_in}\d+)\)\s+\d+\(({bytes_out}\d+)\)\s+({session_duration}\d+)\s+(\S+\s+){2}(?:N\/A|unknown-user|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\S+\s+({dest_interface}\S+)"""
  ]


}
```