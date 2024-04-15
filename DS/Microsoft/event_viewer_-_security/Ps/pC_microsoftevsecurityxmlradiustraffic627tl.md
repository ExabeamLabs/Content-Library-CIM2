#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-radius-traffic-627-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    ParserVersion = "v1.0.0"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>627"
      "network policy server"
    ]
    Fields = [
      "(?i)<Computer>({host}[^<]+)<"
      "(?i)SystemTime=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)<EventID>({event_code}[^<]+)<\\/EventID>"
      "(?i)Account Name:\\s*({user}[^\\s]+)(\\/?)"
      "(?i)Account Domain:\\s*({domain}[^\\s]+)\\s*"
      "(?i)Account Name:\\s*({user_type}[^\\s:]+?)\\/({user}[^\\.\\s\\/:]+?)(\\.[^:\\.\\s]+?)*\\s*Account Domain"
      "(?i)Connection Request Policy Name:\\s*({policy_name}.+?)\\s*Network Policy"
      "(?i)User:\\s*Security ID:\\s*({user_sid}.+?)\\s*Account Name:"
      "(?i)({event_name}Network Policy Server\\s({result}\\w+)\\s.+?)\\s*User:"
      "(?i)Reason:\\s*({failure_reason}[^<]+)\\.\\s"
      "(?i)NAS IPv4 Address:\\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?\\s"
      "(?i)NAS IPv6 Address:\\s*({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({dest_port}\\d+))?\\s"
      "(?i)NAS Identifier:\\s*({location}[^\\s]]+)\\s"
    ]
  

}
```