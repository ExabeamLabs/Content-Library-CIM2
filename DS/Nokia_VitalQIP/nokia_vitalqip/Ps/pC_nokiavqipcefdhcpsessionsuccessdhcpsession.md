#### Parser Content
```Java
{
Name = "nokia-vqip-cef-dhcp-session-success-dhcpsession"
Vendor = "Nokia VitalQIP"
Product = "Nokia VitalQIP"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|QIP|DHCP|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sshost=({dest_host}.+?)\s+([\w\.]+=|$)"""
  """\ssrc=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sdvc=({host}.+?)\s+([\w\.]+=|$)"""
  """\ssntdom=({domain}.+?)\s+([\w\.]+=|$)"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```