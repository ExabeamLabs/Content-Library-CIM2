#### Parser Content
```Java
{
Name = cisco-acs-cef-endpoint-authentication-success-login
Product = "Cisco ACS"
Conditions = [
  """|Cisco Secure ACS|"""
  """categoryOutcome=/Success"""
  """destinationServiceName =Login"""
]
ParserVersion = "v1.0.0"

s-cisco-amp-alert.Fields}[
    """"short_description":"({alert_name}[^"]+)""",
    """file_name":"({process_name}[^\.]+\.exe)"""
  
}
```