#### Parser Content
```Java
{
Name = mcafee-wg-kv-http-session-success-mwg
  Vendor = Skyhigh Security
  Product = Secure Web Gateway
  TimeFormat = "epoch_sec"
  Conditions = [ """ mwg:""", """ McAfee|""", """|cs-uri=""", """|src=""" ]
  Fields = [
    """\|devicetime=({time}\d{10})""",
    """\|host=({host}[\w\-.]+)\|""",
    """\|src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\|""",
    """\|srcport=({src_port}\d+)\|""",
    """\|dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\|""",
    """\|dstport=({dest_port}\d+)\|""",
    """\|username=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\|""",
    """\|cs-method=({method}[^\|]+)\|""",
    """\|time-taken=({duration}\d+)\|""",
    """\|sc-bytes=({bytes_in}\d+)\|""",
    """\|cs-bytes=({bytes_out}\d+)\|""",
    """\|pxy=({proxy_ip}(\d{1,3}\.){3}\d{1,3})\|""",
    """\|cs-uri=({url}[^\s\|]+?({uri_path}\/[^?\s\|]+?)?({uri_query}\?[^\s"\|]+)?)(\|[\w\.]+=|\s*$)"""
  ]
  ParserVersion = "v1.0.0"


}
```