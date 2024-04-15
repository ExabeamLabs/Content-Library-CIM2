#### Parser Content
```Java
{
Name = "zscaler-ia-json-app-login-success-sessionstatus"
  ParserVersion = "v1.0.0"
  Vendor = "Zscaler"
  Product = "Zscaler Internet Access"
  TimeFormat = "MMM dd HH:mm:ss yyyy"
  Conditions = ["""SessionStatus""" , """TimestampAuthentication""" , """CertificateCN"""]
  Fields = [
     """({time}\w{3}\s+\d+\s\d\d:\d\d:\d\d\s\d\d\d\d)""",
     """"SessionStatus":\s*"({result}[^"]+)""",
     """Username":\s*"(({email_address}[^@"\s]+@[^\s"]*)|((({domain}[^@"]+)@)?({user}[^\s"@]+))|({full_name}[^"@]+))"""",
     """TotalBytesRx":\s*({bytes_in}\d+),""",
     """TotalBytesTx":\s*({bytes_out}\d+),""",
     """"PublicIP":\s*"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
     """Hostname"+:\s*"+({host}[^,"]+)"*,""",
     """ClientType"+:\s*"+({client_type}[^,"]+)"*,"""
  ]


}
```