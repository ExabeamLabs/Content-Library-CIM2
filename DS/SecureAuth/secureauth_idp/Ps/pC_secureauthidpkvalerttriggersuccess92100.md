#### Parser Content
```Java
{
Name = secureauth-idp-kv-alert-trigger-success-92100
  ParserVersion = "v1.0.0"
  Conditions = [ """EventID="92100"""", """AE.IP.threatCategory=""", """AE.IP.threatType=""", """Appliance=""" ]
  Fields = ${SecureAuthAAParsersTemplates.secureauth-idp-events.Fields} [
    """\sAE.IP.threatCategoryDescription="({alert_name}[^"]+)"""",
    """\sAE.IP.threatTypeDescription="(No Threat Found|({alert_type}[^"]+))"""",
    """\sAE.IP.RiskScore="({alert_severity}\d+)""""
    """Check IP Risk action:([^,]+,){2}\s*ip:'({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
  ]

secureauth-idp-events = {
    Vendor = SecureAuth
    Product = SecureAuth IDP
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields =[
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s""",
      """\WUserHostAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """\WRealm="({realm}[^"]+)""",
      """\WAppliance="({host}({dest_host}[\w\-.]+))""",
      """\WHostName ="({host}[\w\-.]+)"""",
      """\WUserID="(({email_address}[^@"]+@[^\."]+\.[^"]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""",
      """\WEventID="({event_code}\d+)""",
      """UserAgent="({user_agent}[^"]+)"""",
      """\WEventID="[^\]]*?\]\s({additional_info}[^"]+)\s*"""",
      """\WPriority="({priority}\d+)""",
      """\WCategory="({category}[^"]+)""""
    
}
```