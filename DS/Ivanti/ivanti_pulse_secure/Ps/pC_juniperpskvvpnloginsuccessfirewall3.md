#### Parser Content
```Java
{
Name = "juniper-ps-kv-vpn-login-success-firewall-3"
Vendor = "Ivanti"
Product = "Ivanti Pulse Secure"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """ PulseSecure:"""
  """ realm restrictions successfully passed"""
  """id=firewall"""
]
Fields = [
  """time="({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d)""""
  """vpn=({host}[^\s]+)"""
  """\suser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
  """realm="({realm}[^"]+)?""""
  """roles="({role}[^"]+)?""""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """msg="({event_code}\w+):\s*({additional_info}[^"]+)\s*""""
  ]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```