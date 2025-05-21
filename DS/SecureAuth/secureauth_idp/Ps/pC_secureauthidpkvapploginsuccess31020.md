#### Parser Content
```Java
{
Name = secureauth-idp-kv-app-login-success-31020
  ParserVersion = "v1.0.0"
  Conditions = [ """EventID="31020"""", """ApplianceID=""", """Realm=""", """RequestID="""", """UserHostAddress=""" ]
  Fields = ${SecureAuthAAParsersTemplates.secureauth-idp-events.Fields} [
    """\sSAMLConsumerURL="({url}[^"]+)"""",
    """\starget:({target}[^"]+)\s*"*$"""
  ]

secureauth-idp-events = {
    Vendor = SecureAuth
    Product = SecureAuth IDP
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
    Fields =[
      """\s({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)\s""",
      """\WUserHostAddress="({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
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