#### Parser Content
```Java
{
Name = "microsoft-evsecurity-xml-endpoint-login-4776-tl"
    Vendor = "Microsoft"
    Product = "Event Viewer - Security"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<eventid>4776</eventid>"
      "'status'>"
    ]
    Fields = [
      "(?i)SystemTime(\\\\)?=\\'({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d)"
      "(?i)({event_name}The (computer|domain controller) attempted to validate the credentials for an account)"
      "(?i)<Data Name(\\\\)?='Workstation'>(\\\\+)?(({src_ip}(((\\d{1,3}\\.){1,3}\\d{1,3})|([A-Fa-f0-9]*:[A-Fa-f0-9:.]+)))|(?:(?!NULL)({src_host}[^\\s.]+)(\\.[^\\s]+)?))</Data>"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)The ({login_type_text}computer|domain)(\\s\\w+)? attempted to validate the credentials"
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)<Computer>(?!(?:[A-Fa-f:\\d.]+))[^<.]+(\\.({domain}[^<.]+)[^<]*)?</Computer>"
      "(?i)<Data Name(\\\\)?='TargetUserName'>(({email_address}[^@<]+@[^\\.<]+\\.[^<]+)|(({domain}[^<\\\\]+)\\\\+)?({user}[^<]+)|({=user}[^@<]+?)(?:@({=domain}[^<.]+)[^<]*)?)</Data>"
      "(?i)<Data Name(\\\\)?='Status'>({result_code}[^<]+)</Data>"
      "(?i)<Keywords><Keyword>({result}[^<]+)<"
      "(?i)Workstation:\\s*({src_host}[^\"\\s]+)"
    ]
    ParserVersion = "v1.0.0"
    DupFields = ["host->dest_host"]
  

}
```