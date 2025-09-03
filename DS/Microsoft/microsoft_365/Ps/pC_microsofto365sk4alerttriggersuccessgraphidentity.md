#### Parser Content
```Java
{
Name = microsoft-o365-sk4-alert-trigger-success-graphidentity
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss","yyyy-MM-dd'T'HH:mm:ss.SSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
Conditions = [
"""destinationServiceName =Office 365"""
""""detectedDateTime":""""
"""dproc=graph-identity-protection-risk-detection"""
]
Fields = [
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)\.\d+Z\s+[\w\-.]+\s+"""
"""({alert_type}({alert_name}IdentityProtection))"""
"""({alert_type}({alert_name}graph-identity-protection-risk-detection))"""
""""source":"(generic|({alert_source}({alert_type}[^"]+)))""""
""""riskType":"(generic|({alert_name}[^"]+))""""
""""id":"({alert_id}[^"]+)""""
""""requestId":"({alert_id}[^"]+)""""
""""riskLevel":"({alert_severity}[^"]+)""""
""""riskType":"({threat_category}[^"]+)""""
""""f3u\\*"*:\\*"*({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
"""\ssuser=({email_address}[^@]+@[^\s]+)\s"""
""""userDisplayName":"({full_name}[^"]+?)\s*""""
""""userPrincipalName":\s*"(-|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@({domain}[^"]+))?))"""",
"""msg=({additional_info}[^=]+?)\s+(\w+=|$)"""
"""activity":"({operation}[^"]+)"""
""""userAgent\\?",[^,]*?"Value\\?":\\?"(|({user_agent}[^"\\]+?))\s*\\?"""",
"""destinationServiceName =({app}[^=]+?)\s*\w+="""
""""detectedDateTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+(\.\d{1,7})?Z)"""
""""lastUpdatedDateTime":"({time}\d+-\d+-\d+T\d+:\d+:\d+(\.\d{1,7})?Z)"""
""""tokenIssuerType":"({token_issuer_type}[^"]+)"""
""""+activity":"({action}[^"]+)"""
""""+additionalInfo":"\[\{+({more_info}[^]]+?)\s*\}\]""",
"""flexString1=({action}[^=]+?)\s*\w+=""",
""""Name":"({alert_name}[^"]+)"""
"""request=({result}[^=]+?)\s*\w+="""
""""Severity":"({alert_severity}[^"]+)"""
""""sev\\*":\\*"({alert_severity}[^"\\]+)"""
""""riskLevel":"({alert_severity}[^"]+)"""
""""AlertType":"({alert_type}[^"]+)"""
""""tsd\\*"+:\\*"+({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
""""sip\\*"+:\\*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""clientIP\\*":\\*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\\*""""
""""ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
""""city":"({location_city}[^"]+)"""
""""countryOrRegion":"({country_code}[^"]+)"""
""""state":"({location_state}[^"]+)"""
""""suid":"(anonymous|\\|({email_address}[^@="\\]+@({email_domain}[^"\\]+?))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))\\?""""
""""PolicyName":"({alert_type}[^"]+)""""
""""RuleName":"({alert_name}[^"]+)""""
""""Id":"({alert_id}[^"]+)""""
""""riskEventType":"({alert_name}[^"]+)"""
""""riskState":"({action}[^"]+)"""
""""op\\*"*:\\*"*({operation}[^",\\\s]+)"""
""""wl\\*"*:\\*"*({app}[^",\\\s]+)"""
""""von\\*"*:\\*"*({alert_subject}[^",\\]+)""",
""""correlationId":\s*"({correlation_id}[^"]+)""""
]
DupFields = [ "alert_name->alert_subject" ]
ParserVersion = "v1.0.0"


}
```