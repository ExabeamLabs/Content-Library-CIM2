#### Parser Content
```Java
{
Name = "juniper-ps-kv-vpn-logout-success-juniper"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """Juniper:"""
  """NWC23465"""
  """Session ended"""
]
Fields = [
  """({host}[\w\-\.]+)\s*Juniper:"""
  """\stime=\"{1,20}({time}\d+-\d+-\d+ \d+:\d+:\d+).+?user"""
  """user=([^\\]+\\)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+realm"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s"""
  """with IP(v4 address)?\s+({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
]
ParserVersion = "v1.0.0"


}
```