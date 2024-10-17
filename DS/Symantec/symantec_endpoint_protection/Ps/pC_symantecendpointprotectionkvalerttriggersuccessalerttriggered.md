#### Parser Content
```Java
{
Name = symantec-endpointprotection-kv-alert-trigger-success-alerttriggered
  Vendor = Symantec
  Product = Symantec Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """ SymantecServer: """, """"Event Description:""", """,Local Host IP: """, """,Intensive Protection Level: """ ]
  Fields = [
    """Begin:\s({time}\d{4}-\d{1,2}-\d{1,2} \d{1,2}:\d{1,2}:\d{1,2})""",
    """\d\d:\d\d:\d\d\s({host}[\w.\-]+)\s+SymantecServer:\s*({src_host}[\w\-\.]+)""",
    """"Event Description:\s*({alert_name}[^"]+)"""",
    """,\s*Event Type:\s*({alert_type}[^,]+)""",
    """,\s*User( Name)?:\s*(none|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """,\s*Local Host MAC:\s*({src_mac}[^,]+)""",
    """,\s*Local Host IP:\s*(0.0.0.0|({local_host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""",
    """,\s*Remote Host IP:\s*(0.0.0.0|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))""",
    """,\s*Remote Host MAC:\s*({dest_mac}[^,]+)""",
    """,\s*Remote Host MAC:([^,]+),[^,]+,({protocol}[^,]+)"""
    """,\s*Occurrences:\s*({occurrences}[^,]+)""",
    """,\s*Application:\s*({process_path}({process_dir}[^,]*?[\\\/]+)({process_name}[^,\\\/]+)),""",
    """,\s*Location:\s*({location}[^,]+)""",
    """,\s*Domain( Name)?:\s*({domain}[^\s,]+)""",
    """,\s*Local Port:\s*(0|({src_port}\d+))""",
    """,\s*Remote Port:\s*(0|({dest_port}\d+))"""
  ]
  ParserVersion = "v1.0.0"


}
```