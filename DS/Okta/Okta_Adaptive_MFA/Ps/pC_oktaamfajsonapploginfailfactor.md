#### Parser Content
```Java
{
Name = okta-amfa-json-app-login-fail-factor
  Conditions = [ """EventDetails":""", """Failed""", """ factor attempt""", """"DisplayName":"""]
  ParserVersion = "v1.0.0"

json-okta-failed-app-login = {
    Vendor = Okta
    Product = Okta Adaptive MFA
    TimeFormat = "yyyy-MM-dd HH:mm:ss"
    Fields = [
      """"IPAddress":"({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """"user":"({email_address}[^@"\s]+?@[^@"\s]+)""",
      """"EventDetails":(\[|")({failure_reason}.*?)(\]|"),"\w+":"""
      """Sign-in Failed\s+-\s+({failure_reason}[^":,]+)""",
      """"Source":"({additional_info}[^"]+?)"""",
      """"Source":\[({additional_info}[^\]]+)""",
      """"Host":"({host}[^"]+?)"""",
      """"Host":\["({host}[^",]+)""",
      """({app}(o|O)kta)""",
      """"DisplayName":"({full_name}[^"]+?\s[^"]+)""""
      """"DisplayName":\["({full_name}[^,"]+?\s[^,"]+)"""
    
}
```