#### Parser Content
```Java
{
Name = rsa-r-cef-network-traffic-success-flowdata
Vendor = "RSA"
Product = "RSA"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
  """|flowdata|"""
  """|RSA|"""
  """src="""
  """dst="""
]
Fields = [
  """({time}\w{3}\s\d{2}\s\d{4}\s\d{2}:\d{2}:\d{2})"""
  """src=({src_ip}[^\s]+)\s"""
  """dst=({dest_ip}[^\s]+)\s"""
  """spt=({src_port}\d+)\s"""
  """dpt=({dest_port}\d+)\s"""
  """proto=({protocol}[^\s]+)\s"""
  """InPackets=({packets}\d+)"""
  """FirstSwitched=({time_start}\d+)"""
  """LastSwitched=({time_end}\d+)"""
  """in=({bytes}\d+)"""
  ]
ParserVersion = "v1.0.0"


}
```