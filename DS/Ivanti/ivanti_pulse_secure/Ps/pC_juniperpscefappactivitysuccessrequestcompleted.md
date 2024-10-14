#### Parser Content
```Java
{
Name = juniper-ps-cef-app-activity-success-requestcompleted
Vendor = Ivanti
Product = Ivanti Pulse Secure
TimeFormat = "epoch"
Conditions = [
  """|Juniper|Pulse Secure"""
  """|Request Completed|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}[\w.\-]+)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """\sspriv=({app}.+?)\s+\w+="""
  """\sdhost=({dest_host}[^\s]+)"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sout=({bytes}\d+)"""
  """&Cmd\\=({operation}[^\s&]+)"""
  """&DeviceType\\=({additional_info}[^&]+)"""
]
ParserVersion = "v1.0.0"


}
```