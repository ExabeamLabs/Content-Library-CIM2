#### Parser Content
```Java
{
Name = "okta-amfa-csv-app-login-success-securitycontext"
Vendor = "Okta"
Product = "Okta Adaptive MFA"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""""eventType""""
""""client""""
""""target""""
"""securityContext"""
"""actor"""
]
Fields = [
""""published"+:"+({time}[^",]+)"+"""
"""({app}(?i)Okta)"""
""""+target"+:\[?\{[^\{\}]*?"+alternateId"+:"+(system@okta\.com|(({dest_user}[\w\.\-]{1,40})@({dest_domain}[^\s",]+?\.corp))|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(unknown|({=dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)))"+,[^\{\}]*?("type"+:\s*"+(SystemPrincipal|User)")"""
""""+actor"+:\{[^\{\}]*?("type"+:\s*"+(SystemPrincipal|User)")[^\{\}]*?"+alternateId"+:"+(system@okta\.com|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s",]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(unknown|({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))"+,"""
""""+actor"+:\{[^\{\}]*?"+alternateId"+:"+(system@okta\.com|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^\s",]+?\.corp))|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|(unknown|({=user}[\w\.\-\!\#\^\~]{1,40}\$?)))"+,[^\{\}]*?("type"+:\s*"+(SystemPrincipal|User)")"""
""""+actor"+:\{[^\{\}]*?"+displayName"+:"+(Okta System|Okta Admin|(unknown|({full_name}[^",]+)))"+,"""
""""policyType"+:"+({alert_type}[^",]+)"""
""""eventType"+:"+({operation}[^",]+)"""
""""legacyEventType"+:"+({operation_details}[^",]+)"""
""""+result"+:"+({result}[^"]+)""""
""""reason"+:"+({additional_info}[^",]+)"+"""
""""severity"+:"+({alert_severity}[^",]+)"+"""
""""+userAgent"+:(null|"+({user_agent}[^"]+))"+"""
""""outcome"+:[^\]]*?"+result"+:"+FAILURE"+,"+reason"+:"+({failure_reason}[^"]+)"+"""
""""displayMessage"+:"+({alert_name}[^"]+)"""
""""city"+:"+({location_city}[^",]+)"""
""""state"+:"+({location_state}[^",]+)"""
""""country"+:"+({location_country}[^",]+)"""
""""type"+:"+AppInstance"+[^\}\]]*"displayName"+:"+({app}[^"]+?)\s*""""
""""outcome"+:[^\]]*?"+result"+:"+({result}[^",]+)""""
""""client"+:[^\]]*?"+ipAddress"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""client"+:[^\]]*?"+rawUserAgent"+:"+((?i)unknown|({user_agent}[^"]+?))""""
""""target"+:\[\{[^\}\]]+"+type"+:"+({object_type}[^",]+)""""
]
DupFields = [
"operation->event_name"
"app->object"
]
ParserVersion = "v1.0.0"


}
```