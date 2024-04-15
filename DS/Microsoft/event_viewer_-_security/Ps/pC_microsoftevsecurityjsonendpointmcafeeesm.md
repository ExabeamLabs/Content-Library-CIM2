#### Parser Content
```Java
{
Name = "microsoft-evsecurity-json-endpoint-mcafeeesm"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|McAfee|ESM"""
  """43-26304768"""
]
Fields = [
  """\|McAfee\|[^|]+?\|[^|]+?\|43-2630({event_code}\d+)(0|1)\|"""
  """({event_name}A Kerberos authentication ticket \(TGT\) was requested)"""
  """\srt=({time}\d{13})"""
  """shost=({host}[^\s]+)"""
  """nitroCommandID=({result_code}.+?)\s+\w+="""
  """src=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """sntdom=({domain}[^\s]+)"""
  """suser=({user}.+?)\s+\w+="""
  """nitroService_Name =({service_name}\S+)"""
]
ParserVersion = "v1.0.0"


}
```