#### Parser Content
```Java
{
Name = cisco-umbrella-sk4-dns-response-success-dns
Vendor = Cisco
Product = Cisco Umbrella
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """"src-endpoint":"DNS""""
  """"src-application-name":"Cisco Umbrella""""
  """"action":"""
  """"queryType":"""
]
Fields = [
  """"mostGranularIdentity":"({host}[^"]+)""""
  """"timestamp":"({time}\d\d\d\d-\d\d-\d\d\s\d\d:\d\d:\d\d)""""
  """"responseCode":"({dns_response_code}[^"]+)""""
  """"action":"({action}[^"]+)""""
  """"queryType":"({dns_query_type}[^"]+)""""
  """"domain":"({dns_query}[^"]+)""""
  """"categories":\[(|""|({categories}[^\]]+))\]"""
  """"categories":\["({category}[^"]+)""""
  """"internalIp":"({dest_ip}[a-fA-F:\d.]+)"""
  """"externalIp":"({src_ip}[a-fA-F:\d.]+)"""
  """"identities":\[({identities}[^\[\]]+)\]"""
  """src-account-name":"({account_name}[^"]+)"""
]
DupFields = [
  "host->src_host"
]
ParserVersion = "v1.0.0"


}
```