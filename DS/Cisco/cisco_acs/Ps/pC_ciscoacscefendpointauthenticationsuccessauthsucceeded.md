#### Parser Content
```Java
{
Name = cisco-acs-cef-endpoint-authentication-success-authsucceeded
Product = "Cisco ACS"
Conditions = [
  """|Cisco Secure ACS|"""
  """|Authentication succeeded|"""
]
ParserVersion = "v1.0.0"

s-cisco-amp-alert.Fields}[
    """"short_description":"({alert_name}[^"]+)""",
    """file_name":"({process_name}[^\.]+\.exe)"""
  
}
```