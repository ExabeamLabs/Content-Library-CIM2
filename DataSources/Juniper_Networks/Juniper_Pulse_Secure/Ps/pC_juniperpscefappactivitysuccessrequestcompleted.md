#### Parser Content
```Java
{
Name = juniper-ps-cef-app-activity-success-requestcompleted
Vendor = Juniper Networks
Product = Juniper Pulse Secure
TimeFormat = "epoch"
Conditions = [
  """|Juniper|Pulse Secure"""
  """|Request Completed|"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\sdvc=({host}[\w.\-]+)"""
  """\ssrc=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\ssuser=({user}[^\s]+)"""
  """\sspriv=({app}.+?)\s+\w+="""
  """\sdhost=({dest_host}[^\s]+)"""
  """\sdst=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sout=({bytes}\d+)"""
  """&Cmd\\=({operation}[^\s&]+)"""
  """&DeviceType\\=({additional_info}[^&]+)"""
]
ParserVersion = "v1.0.0"


}
```