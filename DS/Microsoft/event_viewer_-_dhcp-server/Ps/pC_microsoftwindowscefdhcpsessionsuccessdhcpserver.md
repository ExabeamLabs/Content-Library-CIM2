#### Parser Content
```Java
{
Name = "microsoft-windows-cef-dhcp-session-success-dhcpserver"
Vendor = "Microsoft"
Product = "Event Viewer - DHCP-Server"
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|DHCP|"""
  """|Dhcp_Server|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\sdhost=({dest_host}[\w\-.]+)"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
]
DupFields = [
  "dest_host->user"
]
ParserVersion = "v1.0.0"


}
```