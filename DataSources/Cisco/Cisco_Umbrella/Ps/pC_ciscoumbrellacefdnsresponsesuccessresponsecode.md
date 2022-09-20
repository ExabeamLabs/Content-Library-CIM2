#### Parser Content
```Java
{
Name = cisco-umbrella-cef-dns-response-success-responsecode
  ParserVersion = v1.0.0
  Vendor = Cisco
  Product = Cisco Umbrella
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """"queryType":"""", """"responseCode":"""", """"mostGranularIdentityType":""", """destinationServiceName =Cisco Umbrella""" ]
  Fields = [
    """\"timestamp\":\"({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)""",
    """\"identities\":\[[^\]]*?\"({host}[\w\-\.]+)\"""",
    """\"identities\":\[\"({full_name}[^\(\"]+?)(?:\s*\(\w+\)\s*)?(\s+\(({email_address}[^@\"]+@[^@\"]+)\))\",(\"({host}[\w\-\.]+)\")?""",
    """\"action\":\"({action}[^\"]+)\"""",
    """\"queryType\":\"[^\"]*\(({dns_query_type}[^\"\)]+)\)\"""",
    """\"responseCode\":\"({dns_response_code}[^\"]+)\"""",
    """\"domain\":\"({query}[^\"]*?)\.?\"""",
    """\"categories\":\s*\[({categories}\"*({category}[^\"\],]+)[^\]]*)\]""",
    """\"externalIp\"+:\"+({src_ip}[^\"]+)""",
    """"internalIp":"({dest_ip}[^"]+)""""
  ]


}
```