#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-group-create-4754-tl"
    ParserVersion = "v1.0.0"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "<message>a security-enabled universal group was created"
      "<eventid>4754</eventid>"
    ]
    Fields = [
      "(?i)<Message>({event_name}[^\\.:]+?)\\."
      "(?i)<Computer>(::ffff:)?({host}[^<]+)</Computer>"
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d+Z)"
      "(?i)({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+\\.\\d+)"
      "(?i)<EventID>({event_code}\\d+)"
      "(?i)Subject:.+?Security ID:\\s*(|-|({user_sid}.+?))\\s*Account Name:\\s*(|-|({user}.+?))\\s*Account Domain:\\s*(|-|({domain}.+?))\\s*Logon ID:\\s*(|-|({login_id}\\S+))\\s"
      "(?i)Group:\\s*(|-|({group_name}.+?))\\s*Security ID:\\s*(|-|({group_id}.+?))\\s*Group Name:\\s*(|-|({=group_name}.+?))\\s*Group Domain:\\s*(|-|({group_domain}.+?))\\s"
      "(?i)Changed Attributes:\\s*(|-|(.+?))\\s*SAM Account Name:\\s*(|-|(.+?))\\s*SID History:\\s*(|-|({sid_history}.+?))\\s*Additional Information:"
      "(?i)Additional Information:\\s*(|-|({additional_info}.+?))\\s*Privileges:\\s*(|-|({privileges}.+?))\\s*($|<)"
      "(?i)EventID=\"*({event_code}\\d+)"
      "(?i)EventType=\"*({result}[^\"\\s]+)"
    ]
    DupFields = [
      "host->dest_host"
    ]
  

}
```