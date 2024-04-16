#### Parser Content
```Java
{
Name = cisco-umbrella-json-dns-response-success-responsecode
  Vendor = Cisco
  Product = Cisco Umbrella
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """,EventType":"""", """,Identities":"""", """,ResponseCode":"""", """,BlockedCategories":"""",""",QueryType":"""" ]
  Fields = [
    """,Timestamp":"({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d),""",
    """,Identities":"({identities}[^,]+),""",
    """,InternalIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,""",
    """,ExternalIp":"({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?,""",
    """,Action":"({result}[^,]+),""",
    """,QueryType":"({dns_query_type}[^,]+),""",
    """,ResponseCode":"({dns_response_code}[^,]+),""",
    """,Domain":"({dns_query}[^,]+),""",
    """,Categories":"({categories}({category}[^,"]+)[^"]*),""",
    """,Identities":"(({user}[^\s,"\(]+)\s\(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\),)?(({src_network_zone}[^,]+),)?(({src_host}[\w\-\.]+),)InternalIp.*?IdentityTypes":"AD Users,(Networks,)?Anyconnect Roaming Client,BlockedCategories"""",
    """,Identities":"({user}[^\s,"\(]+)\s\(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\),({dest_host}[\w\-\.]+),({src_location}[^,]+),({src_network_zone}[^,]+),InternalIp.*?IdentityTypes":"AD Users,AD Computers,Sites,Networks,BlockedCategories"""",
	  """,Identities":"(({user}[^\s,"\(]+)\s\(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\),)?({src_location}[^,]+),({src_network_zone}[^,]+),InternalIp.*?IdentityTypes":"(AD Users,)?Sites,Networks,BlockedCategories"""",
	  """,Identities":"({src_host}[\w\-\.]+),(({src_network_zone}[^,]+),)?InternalIp.*?IdentityTypes":"Anyconnect Roaming Client(,Networks)?,BlockedCategories"""",
	  """,Identities":"({src_network_zone}[^,]+),InternalIp.*?IdentityTypes":"Networks,BlockedCategories""""
  ]
  ParserVersion = "v1.0.0"


}
```