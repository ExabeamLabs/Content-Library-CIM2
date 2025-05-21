#### Parser Content
```Java
{
Name = "zscaler-pa-json-vpn-logout-success-username"
Vendor = "Zscaler"
Product = "Zscaler Private Access"
TimeFormat = "MMM  dd HH:mm:ss yyyy"
Conditions = [
  """"ZPN_STATUS_DISCONNECTED""""
  """"Username":"""
]
Fields = [
  """({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)"""
  """"Hostname":\s*\"({host}[^\"]+)""""
  """"PublicIP":\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  """"Username":\s*\"(({email_address}[^@\"\s]+@[^\s\"]*)|((({domain}[^@\"]+)@)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))|({full_name}[^\"@]+))""""
  """"TotalBytesRx":\s*({bytes_in}\d+),"""
  """"TotalBytesTx":\s*({bytes_out}\d+),"""
  """"SessionStatus":\s*\"({event_name}[^\"]+)"""",
  """"PrivateIP":\s*"({src_translated_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""",
  """"FQDNRegisteredError":\s*"(|({error_code}.+?))"""",
  """"SessionStatus":\s*(\\)?"({result}[^\"]+)"""",
  """"Platform":\s*"({os}.+?)""""
]
ParserVersion = "v1.0.0"


}
```