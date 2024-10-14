#### Parser Content
```Java
{
Name = tenable-tcs-json-app-notification-success-ermetic
  Vendor = Tenable
  Product = Tenable Cloud Security
  TimeFormat = [ """yyyy-MM-dd'T'HH:mm:ss.SSSZ""", """yyyy-MM-dd'T'HH:mm:ss.SSS""", """yyyy-MM-dd'T'HH:mm:ss.SSZ""", """yyyy-MM-dd'T'HH:mm:ss""" ]
  Conditions = [ """"accountName":""", """"accountId":""", """"findingType":""", """"remediation":""", """"console":""", """"steps":""", """"source":""", """"Ermetic""" ]
  Fields = [
    """"source":\s*"({log_source}[^"]+)"""", 
		""""accountName":\s*"({account_name}[^"]+)"""", 
		""""accountId":\s*"({account_id}[^"]+)"""", 
		""""description":\s*"({description}[^"]+)"""", 
		""""link":\s*"({link}[^"]+)"""", 
		""""severity":\s*"({severity}[^"]+)"""", 
		""""title":\s*"({event_name}[^"]+)"""", 
		""""creationTime":\s*"({time}[^"]+)"""", 
		""""status":\s*"({status_msg}[^"]+)"""", 
		""""type":\s*"({event_subtype}[^"]+)"""",
		""""labels":\s*\[\s*({additional_info}[^\]]+?)\s*\]"""
  ]
  ParserVersion = "v1.0.0"


}
```