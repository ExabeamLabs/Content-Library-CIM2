#### Parser Content
```Java
{
Name = "proofpoint-tap-cef-email-receive-messageblocked"
Vendor = "Proofpoint"
Product = "Targeted Attack Platform"
TimeFormat = ["epoch","yyyy-MM-dd'T'HH:mm:ssZ"]
Conditions = [
"""|Proofpoint|TAP|"""
]
Fields = [
"""\srt=({time}\d{13})"""
"""^([^|]*\|){4}({result}[^|]+)"""
"""\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""\ssuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
"""\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
"""({alert_name}Proofpoint)"""
"""\"threatType\":\"({alert_type}[^\"]+)"""
"""\"threatID\":\"({alert_id}[^\"]+)"""
"""\scs6=\[({additional_info}[^\]]+)"""
"""eventTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
]
DupFields = [
"user->email_recipients"
]
ParserVersion = "v1.0.0"


}
```