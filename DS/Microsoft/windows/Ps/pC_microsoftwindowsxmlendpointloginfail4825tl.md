#### Parser Content
```Java
{
Name = "microsoft-windows-xml-endpoint-login-fail-4825-tl"
    Vendor = "Microsoft"
    Product = "Windows"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "<eventid>4825</eventid>"
      "<provider>microsoft windows security auditing.</provider>"
      "<message>a user was denied the access to remote desktop."
    ]
    Fields = [
      "(?i)TimeCreated SystemTime(\\\\)?='({time}\\d+-\\d+-\\d+T\\d+:\\d+:\\d+\\.\\d{9})Z"
      "(?i)<Computer>({host}({dest_host}[\\w\\-\\.]+)[^<]*)</Computer>"
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)<Data Name(\\\\)?='AccountName'>(?=\\w)?(-|({user}[^<]+))<\\/Data>"
      "(?i)<Data Name(\\\\)?='AccountDomain'>(-|({domain}[^<]+))<\\/Data>"
      "(?i)<Data Name(\\\\)?='LogonID'>({login_id}\\w+)<\\/Data>"
      "(?i)<Data Name(\\\\)?='ClientAddress'>({src_ip}[a-fA-F0-9\\.:]+)<\\/Data>"
      "(?i)<Message>({event_name}A user was denied the access to Remote Desktop)."
    ]
    ParserVersion = "v1.0.0"
  

}
```