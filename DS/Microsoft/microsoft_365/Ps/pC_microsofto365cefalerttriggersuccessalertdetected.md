#### Parser Content
```Java
{
Name = microsoft-o365-cef-alert-trigger-success-alertdetected
Vendor = "Microsoft"
Product = "Microsoft 365"
TimeFormat = "yyyy-MM-dd HH:mm:ss.SSS"
Conditions = [
""""Operation":"DlpRuleMatch""""
"""destinationServiceName =Office 365"""
]
Fields = [
""""CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)"""",
"""suser=((anonymous)|({email_address}[^"@\s]+@[^".\s]+\.[^"\s]+)|({user}[^"\s]+))""",
""""ObjectId":"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.({file_ext}[^\\\."]+))?))"""",
""""SensitiveInfoTypeName":"({additional_info}[^"]+)"""",
""""CreationTime":"({time}\d\d\d\d-\d\d-\d\d\s*\d\d:\d\d:\d\d\.\d\d\d)""""
""""FromPerson":"({email_address}[^\@]+\@[^"]+)""""
""""Id":"({user_id}[^"]+)""""
"""({alert_type}DlpRuleMatch)"""
""""PolicyName":"({alert_name}[^"]+)""""
""""ToPerson":"({dest_email_address}[^\@]+\@[^"]+)""""
""""RuleName":"({additional_info}[^"]+)""""
""""Location":"(Message Body|({file_name}[^"]+))""""
""""IncidentId":"({alert_id}[^"]+)""""
""""Severity":"({alert_severity}[^"]+)""""
"""src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
""""DeviceName":"({src_host}[^"]+)"""",
""""Application":"({process_name}[^"]+)"""",
""""EndpointOperation":"({operation}[^"]+)""""
]
DupFields = [
"dest_email_address->target"
"alert_name->event_name"
"alert_name->alert_subject"
]
ParserVersion = "v1.0.0"


}
```