#### Parser Content
```Java
{
Name = "proofpoint-tap-cef-email-receive-messageblocked"
Vendor = "Proofpoint"
Product = "Targeted Attack Platform"
TimeFormat = "epoch"
Conditions = [
"""|Proofpoint|TAP|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""^([^|]*\|){4}({action}[^|]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser=({src_email_address}\S+)"""
"""\sduser=({user}\S+)"""
"""({alert_name}Proofpoint)"""
"""\"threatType\":\"({alert_type}[^\"]+)"""
"""\"threatID\":\"({alert_id}[^\"]+)"""
"""\scs6=\[({additional_info}[^\]]+)"""
]
DupFields = [
"user->email_recipients"
"email_address->external_address"
]
ParserVersion = "v1.0.0"


}
```