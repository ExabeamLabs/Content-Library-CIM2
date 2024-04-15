#### Parser Content
```Java
{
Name = "secureauth-login-xml-app-login-success-priority-tl"
    Vendor = "SecureAuth"
    Product = "SecureAuth Login"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [
      "<priority>"
      "success</message>"
    ]
    Fields = [
      "(?i)<UserHostAddress>({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\\d|[0-9]|)\\d)\\.?\b){4}))(:({src_port}\\d+))?"
      "(?i)<HostName>({host}[^<]+)"
      "(?i)<EventID>({event_code}\\d+)</EventID>"
      "(?i)<UserID>({user}[^<]+)"
      "(?i)<Realm>({app}[^<]+)"
      "(?i)<UserAgent>(?:-|({user_agent}[^<]+))"
    ]
    ParserVersion = "v1.0.0"
  

}
```