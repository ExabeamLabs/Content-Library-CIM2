#### Parser Content
```Java
{
Name = "okta-amfa-sk4-app-appactivity"
Vendor = "Okta"
Product = "Okta Adaptive MFA"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
"""destinationServiceName =Okta"""
""""targets":"""
""""eventId":"""
]
Fields = [
""""published":"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
"""\Wfname=({object}(?![\w\-]{25}).+?)\s+(\w+=|$)"""
"""\Wmsg=({additional_info}[^=]+?)\s+(\w+=|$)"""
""""action":[^}]+?"message":"({additional_info}[^"]+)"""
""""action":[^}]+?"objectType":"({operation}[^"]+)"""
""""(targets|actors)":[^\]]+?"objectType":"User"[^\]\}]+?"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))"""
""""(targets|actors)":[^\]]+?"displayName":"((?i)Unknown|RSA-OKTA Admin|AD-OKTA Admin|({full_name}[^"]+))[^\]\}]+?"objectType":"User""""
"""(s|d)?user\\*=({email_address}[^\s@,]+@({email_domain}[^\s@,]+))"""
"""(s|d)?user\\*=(anonymous|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s|\||,)"""
""""(targets|actors)":[^\]]+?"objectType":"User"[^\]\}]+?"login":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
""""(targets|actors)":[^\]]+?"login":"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\]\}]+?"objectType":"User""""
""""actors":[^\]]+?"objectType":"Client"[^\]\}]+?"displayName":"(UNKNOWN|({browser}[^"]+))"""
""""actors":[^\]]+?"displayName":"(UNKNOWN|({browser}[^"]+))[^\]\}]+?"objectType":"Client""""
""""ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
""""actors":[^\]]+?"objectType":"Client"[^\]\}]+?"ipAddress":"(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)"""
""""actors":[^\]]+?"ipAddress":"(|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)[^\]\}]+?"objectType":"Client""""
""""target(s)?":[^\]]+?"objectType":"User"[^\]\}]+?"displayName":"(({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+))"""
""""target(s)?":[^\]]+?"displayName":"(({dest_user}[\w\.\-\!\#\^\~]{1,40}\$?)|({dest_user_full_name}\w+(\s+\w+)+))","login":"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))","objectType":"User""""
""""target":.+?"type":"User".+?"displayName":"({dest_user_full_name}\w+(\s+\w+)+)"""
""""target(s)?":[^\]\}]+?"objectType":"({object_type}[^"]+)"""
""""actors":[^\]]+?"objectType":"Client"[^\]\}]+?"id":"({user_agent}[^"]+)"""
""""actors":[^\]]+?"id":"({user_agent}[^"]+)[^\]\}]+?"objectType":"Client""""
"""({app}Okta)"""
""""id":"({object}[^"]+)"[^\}\]]*"objectType":"AppInstance""""
""""objectType":"AppInstance"[^\}\]]*"id":"({object}[^"]+)""""
"""destinationServiceName({app}[^=]+?)\s*\w+="""
"""\Wsuid=(anonymous|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))(\s+\w+=|\s*$)"""
"""requestUri":\s*"({uri_path}[^"]+?)\s*""""
]
ParserVersion = "v1.0.0"


}
```