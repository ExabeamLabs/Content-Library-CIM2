#### Parser Content
```Java
{
Name = "zscaler-pa-json-vpn-authentication-success-authenticated"
Vendor = "Zscaler"
Product = "Zscaler Private Access"
ParserVersion = "v1.0.0"
TimeFormat = "MMM dd HH:mm:ss yyyy"
Conditions = [
  """"ZEN":""",
  """"SessionStatus":""",
  """"ZPN_STATUS_AUTHENTICATED""""
]
Fields = [
  """"LogTimestamp":\s*"\S{3}\s({time}\w{3}\s*\d+\s+\d\d:\d+:\d+\s\d\d\d\d)"""",
  """"SessionID":\s*"({session_id}[^"]+)"""",
  """"PublicIP":\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""",
  """PrivateIP=({src_translated_ip}[A-Fa-f\d:.]+)""",
  """"TotalBytesRx":\s*({bytes_in}\d+),""",
  """"TotalBytesTx":\s*({bytes_out}\d+)""",
  """"SessionStatus":\s*\"({event_name}[^\"]+)""""
]


}
```