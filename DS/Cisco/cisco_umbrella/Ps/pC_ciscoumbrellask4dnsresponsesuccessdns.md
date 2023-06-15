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
  """"action":"({result}[^"]+)""""
  """"queryType":"({dns_query_type}[^"]+)""""
  """"domain":"({dns_query}[^"]+)""""
  """"categories":\[(|""|({categories}[^\]]+))\]"""
  """"categories":\["({category}[^"]+)""""
  """"internalIp":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """"externalIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"identities":\[({identities}[^\[\]]+)\]"""
  """src-account-name":"({account_name}[^"]+)"""
]
DupFields = [
  "host->src_host"
]
ParserVersion = "v1.0.0"


}
```