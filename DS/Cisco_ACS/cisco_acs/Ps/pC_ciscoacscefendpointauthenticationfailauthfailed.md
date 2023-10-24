#### Parser Content
```Java
{
Name = cisco-acs-cef-endpoint-authentication-fail-authfailed
Product = "Cisco ACS"
Conditions = [
  """|Cisco Secure ACS|"""
  """|Authentication failed|"""
]
ParserVersion = "v1.0.0"

s-cisco-amp-alert.Fields}[
    """"short_description":"({alert_name}[^"]+)""",
    """file_name":"({process_name}[^\.]+\.exe)"""
  
}
```