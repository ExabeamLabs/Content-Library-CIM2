#### Parser Content
```Java
{
Name = "microsoft-o365-json-email-send-receive-advancedhuntingemailurlinfo"
Vendor = "Microsoft"
Product = "Microsoft Defender"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ssZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"]
Conditions = [
  """EmailUrlInfo""""
  """"UrlDomain":"""
  """"Url":"""
  """"NetworkMessageId":"""
]
Fields = [
  """"Timestamp":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
  """"Url":\s*"({url}[^"]+?)""""
  """"UrlDomain":\s*"(\w+:\/\/)?({web_domain}[^\s"]+)\s*""""
  """({event_name}AdvancedHunting-EmailUrlInfo)"""
  """"NetworkMessageId":\s*"({message_id}[^"]+?)""""
 
]
ParserVersion = "v1.0.0"


}
```