#### Parser Content
```Java
{
Name = "cisco-acs-cef-app-activity-success-appactivity"
Product = "Cisco ACS"
Conditions = [
  """|Cisco Secure ACS|"""
  """categoryOutcome=/Success"""
]
ParserVersion = "v1.0.0"

s-cisco-amp-alert.Fields}[
    """"short_description":"({alert_name}[^"]+)""",
    """file_name":"({process_name}[^\.]+\.exe)"""
  
}
```