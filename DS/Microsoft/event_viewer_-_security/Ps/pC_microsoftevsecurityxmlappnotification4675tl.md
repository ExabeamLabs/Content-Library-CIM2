#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-app-notification-4675-tl"
    Vendor = "Microsoft"
    ParserVersion = "v1.0.0"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "sids were filtered"
      "4675"
    ]
    Fields = [
      "(?i)({event_name}SIDs were filtered)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)({event_code}4675)"
      "(?i)\\sTarget Account:\\s*(|-|(.+?))\\s*Security ID:\\s*(|-|({user_sid}.+?))\\s*Account Name:\\s*(|-|({user}.+?))\\s*Account Domain:\\s*(|-|({domain}.+?))\\s*Trust Information:\\s*(|-|(.+?))\\s*Trust Direction:\\s*(|-|(.+?))\\s*Trust Attributes:\\s*(|-|(.+?))\\s*Trust Type:\\s*(|-|({trust_type}.+?))\\s*TDO Domain SID:\\s*(|-|(.+?))\\s*Filtered SIDs:\\s*(|-|(.+?))\\s*($|<)"
    ]
    DupFields = [
      "host-> dest_host"
    ]
  

}
```