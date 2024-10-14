#### Parser Content
```Java
{
Name = microsoft-o365-sk4-alert-trigger-success-urlclicked
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
Conditions = [ """"Operation":"TIUrlClickData"""", """"Workload":""" ]
Fields = [
""""CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""""
""""Id":"({alert_id}[^"]+)""""
""""EventDeepLink":"\s*({additional_info}[^"]+)""""
""""Workload":"({alert_type}[^"]+)"""
""""Operation":"({alert_name}[^"]+)"""
"""\Wsuser=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)\s(\w+=|$)"""
""""+UserId"+:"+((\w{1,5}:\w{1,5}:[^\#]+\#)?({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({full_name}({first_name}[^"\s]+)\s({last_name}[^"]+))|(Unknown|({user_sid}[^"]+)))"+"""
""""UserIp":"({src_ip}(\d{1,3}\.){3}\d{1,3}|([A-Fa-f0-9%.]*:[A-Fa-f0-9%.:]+(th0)?))""""
""""Url":"({malware_url}[^"]+?)""""
""""UserType":\s*"*({user_type}[^\}"]+)\s*"*(,|\})"""
]
ParserVersion = "v1.0.0"
DupFields = [ "alert_name->alert_subject", "alert_type->alert_source"]


}
```