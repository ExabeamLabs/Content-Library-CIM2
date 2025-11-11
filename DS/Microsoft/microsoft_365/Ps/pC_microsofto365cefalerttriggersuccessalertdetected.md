#### Parser Content
```Java
{
Name = microsoft-o365-cef-alert-trigger-success-alertdetected
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss", "yyyy-MM-dd HH:mm:ss.SSS","yyyy-MM-dd'T'HH:mm:ssZ"]
Conditions = [ """"Operation":"DlpRuleMatch"""", """"UserId":"""" ]
Fields = [
""""CreationTime":"({time}\d\d\d\d-\d\d-\d\d(T|\s)\d\d:\d\d:\d\d(\.\d{1,3})?)""",
""""UserId":"({email_address}[^"\\,]+@({email_domain}[^",]+))"""",
"""suser=((anonymous)|({email_address}[^"@\s]+@[^".\s]+\.[^"\s]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""",
""""ObjectId":"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.({file_ext}[^\\\."]+))?))"""",
""""SensitiveInfoTypeName":"({additional_info}[^"]+)"""",
""""FromPerson":"({email_address}[^\@]+\@[^"]+)""""
""""Id":"({user_id}[^"]+)""""
"""({alert_type}DlpRuleMatch)"""
""""PolicyName":"({alert_subject}({event_name}({alert_name}[^"]+)))""""
""""ToPerson":"({target}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))""""
""""RuleName":"({additional_info}[^"]+)""""
""""Location":"(Message Body|({file_name}[^"]+))""""
""""IncidentId":"({alert_id}[^"]+)""""
""""Severity":"({alert_severity}[^"]+)""""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
""""DeviceName":"({src_host}[^"]+)"""",
""""Application":"({process_name}[^"]+)"""",
""""EndpointOperation":"({operation}[^"]+)"""",
""""ClientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?""""
""""Workload":\s*"({app}[^"]+)""""
""""TimeGenerated":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""""
]
ParserVersion = "v1.0.0"


}
```