#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-alert-trigger-success-symanteceprisk
  ParserVersion = v1.0.0
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """ SymantecServer: """, """Event Description:""", """Web Attack:""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """Begin:\s*({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""",
    """\d\d:\d\d:\d\d\s({host}[\w.\-]+)\s+SymantecServer:\s*({src_host}[^,]+)""",
    """\s*\w+,({host}[\w\-.]+),"*Event Description:""",
    """,\s*Event Description:\s*({event_name}[^,]+)""",
    """,\s*User( Name)?:\s*(none|({user}[\w\.\-]{1,40}\$?))""",
    """,\s*Local Host IP:\s*(0.0.0.0|({local_host_ip}[^,]+))""",
    """,\s*Local Host MAC:\s*({local_host_mac}[^,]+)""",
    """,\s*Remote Host IP:\s*(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)""",
    """,\s*Remote Host MAC:\s*({dest_mac}[^,]+)""",
    """,\s*Occurrences:\s*({occurrences}[^,]+)""",
    """,\s*Application:\s*({process_path}({process_dir}[^,]*?[\\\/]+)({process_name}[^,\\\/]+)),""",
    """,\s*Location:\s*({location}[^,]+)""",
    """,\s*Domain( Name)?:\s*({domain}[^\s,]+)""",
    """,\s*Local Port:\s*(0|({src_port}\d+))""",
    """,\s*Remote Port:\s*(0|({dest_port}\d+))""",
    """,\s*CIDS Signature string:\s*({alert_name}[^,]+?)\s*,""",
    """,\s*Intrusion URL:\s*({malware_url}[^,\s]+?)\s*,""",
    """,\s*Event Type:\s*({alert_type}[^,]+?)\s*,"""
  ]


}
```