#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-4769-2-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>4769</eventid>"
      "a kerberos service ticket was requested"
      "account name"
      "microsoft-windows-security-auditing"
    ]
    Fields = [
      "(?i)({event_name}A Kerberos service ticket was requested)"
      "(?i)TimeCreated SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d.\\d\\d\\d\\d\\d\\d\\d\\d\\dZ)'\\/>"
      "(?i)Computer>({host}[^<]+)<\\/Computer"
      "(?i)({event_code}4769)"
      "(?i)Account Name(:|=)\\s*({user}[^@:\\s;]+)(@({domain}[\\w._\\-]+))?[\\s;]*Account Domain(:|=)"
      "(?i)Service Name(:|=)\\s*({dest_host}[^\\s;]+\\$)[\\s;]*Service ID"
      "(?i)Service Name(:|=)\\s*({service_name}[^\\s;]+)[\\s;]*Service ID"
      "(?i)Client Address(:|=)\\s*(::[\\w]+:)?({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)Failure Code(:|=)\\s*({result_code}.+?)[\\s;]*Transited Services(:|=)"
      "(?i)Ticket Options(:|=)\\s*({ticket_options}.+?)[\\s;]*Ticket Encryption Type(:|=)"
      "(?i)Ticket Encryption Type(:|=)\\s*({ticket_encryption_type}.+?)[\\s;]*Failure Code(:|=)"
    ]
    DupFields = [
      "result_code->failure_code"
    ]
    ParserVersion = "v1.0.0"
  

}
```