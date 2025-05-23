#### Parser Content
```Java
{
Name = microsoft-azuresc-sk4-alert-trigger-success-securityalert
  ParserVersion = v1.0.0
  Vendor = Microsoft
  Product = Microsoft Defender
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"ProductName":"Azure Security Center"""", """"Type":"SecurityAlert"""" ]
  Fields=[
    """"AlertName":"({alert_name}[^"]+)""",
    """"AlertSeverity":"({alert_severity}[^"]+)""",
    """"SystemAlertId":"({alert_id}[^"]+)""",
    """"Description":"({additional_info}[^".]+?)\.?"""",
    """"AlertType":"({alert_type}[^"]+)""",
    """"TimeGenerated":"({time}[^"]+)""",
    """"CompromisedEntity":"({src_host}[^"]+)""",
    """"Address":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"User agent":\s*"({user_agent}[^"]+)""",
    """"Azure AD user":\s*"(N\/A\s+\(Azure AD authentication was not used\)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
    """"CountryName":\s*"({location_country}[^"]+)""",
    """"City":\s*"({location_city}[^"]+)""",
    """"AlertLink":"({malware_url}[^"]+)"""
    ]


}
```