#### Parser Content
```Java
{
Name = beyondtrust-powerbroker-json-process-create-success-28692
  Vendor = BeyondTrust
  Product = BeyondInsight
  TimeFormat = ["MM/dd/yyyy HH:mm:ss a","M/dd/yyyy HH:mm:ss a"]
  Conditions = [ """EventMessage":"Application Launched""","""EventName":"28692""", """Category":"pbw""" ]
  Fields = [
    """TimeCreated":"({time}\d+\/\d+\/\d\d\d\d\s\d+:\d+:\d+\s(am|AM|pm|PM))""",
    """EventName":"({event_code}\d+)"""",
    """AssetName":"({dest_host}[^"]+?)"""",
    """UserName":"({domain}[^\\\/]+?)[\\\/]+({user}[\w\.\-]{1,40}\$?)"""",
    """Path":"({process_path}({process_dir}(?:[^"]+)?[\\\/])?({process_name}[^\\\/"]+?))"""",
    """Arguments":"({process_command_line}[^"]+?)"""",
    """EventDesc":"({event_name}[^"]+?)"""",
    ]
	ParserVersion = "v1.0.0"


}
```