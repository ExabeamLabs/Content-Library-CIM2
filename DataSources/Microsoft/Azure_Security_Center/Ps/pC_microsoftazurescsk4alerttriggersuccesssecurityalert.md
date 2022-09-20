#### Parser Content
```Java
{
Name = microsoft-azuresc-sk4-alert-trigger-success-securityalert
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Azure Security Center
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"ProductName":"Azure Security Center"""", """destinationServiceName =Azure""", """dproc=Log Analytics OMS Workspace""", """"Type":"SecurityAlert"""" ]
  Fields=[
    """"AlertName":"({alert_name}[^"]+)""",
    """"AlertSeverity":"({alert_severity}[^"]+)""",
    """"SystemAlertId":"({alert_id}[^"]+)""",
    """"Description":"({additional_info}[^".]+?)\.?"""",
    """"AlertType":"({alert_type}[^"]+)""",
    """"TimeGenerated":"({time}[^"]+)""",
    """"CompromisedEntity":"({src_host}[^"]+)""",
    """"Address":\s*"({src_ip}[a-fA-F:\d.]+)""",
    """"User agent":\s*"({user_agent}[^"]+)""",
    """"Azure AD user":\s*"(N\/A\s+\(Azure AD authentication was not used\)|({user}[^"]+))""",
    """"CountryName":\s*"({location_country}[^"]+)""",
    """"City":\s*"({location_city}[^"]+)""",
    """"AlertLink":"({malware_url}[^"]+)"""
    ]


}
```