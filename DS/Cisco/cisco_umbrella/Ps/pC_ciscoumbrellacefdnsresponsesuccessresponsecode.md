#### Parser Content
```Java
{
Name = cisco-umbrella-cef-dns-response-success-responsecode
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Umbrella
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"queryType":"""", """"responseCode":"""", """"mostGranularIdentityType":""","""destinationServiceName =Cisco Umbrella""" ]
  Fields = [
    """\"timestamp\":\"({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """\"identities\":\[[^\]]*?\"({host}[\w\-\.]+)\"""",
    """\"identities\":\[\"({full_name}[^\(\"]+?)?(?:\s*\(\w+\)\s*)?(\s+\((({email_address}[^@"]+@({email_domain}[^\."]+\.[^"]+))(?<!local)|(({user}[\w\.\-]{1,40}\$?)(@({domain}[^"]+)?)))\))?\"?,(\"({host}[\w\-\.]+)\")?"""
    """\"action\":\"({result}[^\"]+)\"""",
    """\"queryType\":\"[^\"]*\(({dns_query_type}[^\"\)]+)\)\"""",
    """\"responseCode\":\"({dns_response_code}[^\"]+)\"""",
    """\"domain\":\"({dns_query}[^\"]*?)\.?\"""",
    """\"categories\":\s*\[({categories}\"*({category}[^\"\],]+)[^\]]*)\]""",
    """\"externalIp\"+:\"+({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_translated_port}\d+))?""",
    """"internalIp":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
  ]


}
```