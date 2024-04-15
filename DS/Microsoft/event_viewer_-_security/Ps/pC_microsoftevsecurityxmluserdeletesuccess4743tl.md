#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-user-delete-success-4743-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
    Conditions = [
      "a computer account was deleted"
      "<eventid>4743</eventid>"
    ]
    Fields = [
      "(?i)({event_name}A computer account was deleted)"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d\\d\\d)"
      "(?i)({event_code}4743)"
      "(?i)Subject:[^=]+?\\sAccount Name:\\s*(|-|({user}[^=]+?))\\s*Account Domain:\\s*(|-|({domain}[^=]+?))\\s*Logon ID:\\s*(|-|({login_id}[^=]+?))\\s*Target Computer:[^=]+?\\sAccount Name:\\s*(|-|({dest_user}[^=]+?))\\s*Account Domain:\\s*(|-|({object_dn}[^\\\"]+?))\\s*Additional Information:"
      "(?i)\\sTarget Computer:[^=]+?Account Name:\\s*({src_host}[^$:]+?)\\$"
    ]
    DupFields = [
      "host->dest_host"
    ]
    ParserVersion = "v1.0.0"
  

}
```