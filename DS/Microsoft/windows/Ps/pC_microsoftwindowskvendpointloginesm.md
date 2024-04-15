#### Parser Content
```Java
{
Name = "microsoft-windows-kv-endpoint-login-esm"
Vendor = "Microsoft"
Product = "Windows"
TimeFormat = "epoch"
Conditions = [
  "|McAfee|ESM"
  "43-21100680"
]
Fields = [
  """\|McAfee\|[^|]+?\|[^|]+?\|43-21100({event_code}\d+)(0|1)\|"""
  """({event_name}Logon attempt)"""
  """\srt=({time}\d{13})"""
  """src=({host}[a-fA-F:\d.]+)"""
  """nitroCommandID=({result_code}.+?)\s+\w+="""
  """sntdom=({domain}[^\s]+)"""
  """suser=({user}.+?)\s+\w+="""
  """shost=({dest_host}.+?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```