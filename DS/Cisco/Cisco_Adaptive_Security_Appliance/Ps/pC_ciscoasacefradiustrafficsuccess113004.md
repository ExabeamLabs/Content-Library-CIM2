#### Parser Content
```Java
{
Name = cisco-asa-cef-radius-traffic-success-113004
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|CISCO|ASA|"""
  """|113004|"""
  """AAA user authentication Successful"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\sdvc=({host}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\sdst=({dest_ip}[^\s]+)"""
  """\sdhost=({dest_host}[^\s]+)"""
  """\sduser=({full_name}(\w+\s+)+\w+)\s+(\w+=|$)"""
  """\sduser=({user}[^\s@]+)\s+(\w+=|$)"""
  """\sduser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```