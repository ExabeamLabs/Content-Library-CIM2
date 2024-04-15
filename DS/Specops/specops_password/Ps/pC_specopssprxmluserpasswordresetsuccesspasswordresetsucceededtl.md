#### Parser Content
```Java
{
Name = "specops-spr-xml-user-password-reset-success-passwordresetsucceeded-tl"
    Vendor = "Specops"
    Product = "Specops Password"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSSSZ"
    Conditions = [
      "specops password reset"
      "<event xmlns="
      "password reset succeeded"
    ]
    Fields = [
      "(?i)SystemTime='({time}\\d\\d\\d\\d-\\d\\d-\\d\\dT\\d\\d:\\d\\d:\\d\\d\\.\\d{9}Z)'"
      "(?i)({event_name}Password Reset Succeeded)"
      "(?i)<EventID Qualifiers='0'>({event_code}\\d+)</EventID>"
      "(?i)User:\\s+'(({dest_domain}[^\\\\\\/']+)[\\\\\\/])?({dest_user}[^']+)'"
      "(?i)<Computer>({host}[^<]+)</Computer>"
      "(?i)From client:\\s+'({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?'"
    ]
    ParserVersion = "v1.0.0"
  

}
```