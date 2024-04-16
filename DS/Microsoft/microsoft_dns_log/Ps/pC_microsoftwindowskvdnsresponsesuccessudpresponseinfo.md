#### Parser Content
```Java
{
Name = microsoft-windows-kv-dns-response-success-udpresponseinfo
Vendor = Microsoft
Product = Microsoft DNS Log
TimeFormat = "MM/dd/yyyy HH:mm:ss a"
Conditions = [
  """UDP response info at """
  """Buf length ="""
]
Fields = [
  """({time}\d+\/\d+\/\d\d\d\d \d+:\d+:\d+ (AM|am|PM|pm))"""
  """({protocol}UDP)\s+({operation}Snd)\s+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """Remote addr\s*({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),\s*port\s*({dest_port}\d+)"""
  """XID\s+0x({query_id}[\da-fA-F]+)"""
  """QTYPE\s+({dns_query_type}\w+)"""
  """RCODE\s+[^(]*?\(({dns_response_code}[^(]+)\)"""
  """QUESTION SECTION:.*?Name\s+"({dns_query}[^"]+)""""
  """Buf length\s*=\s*\S+\s*\(({bytes}\d+)"""
  """ANSWER SECTION:(\s*empty|.+?DATA\s+({dns_response}\S+))"""
]
ParserVersion = "v1.0.0"


}
```