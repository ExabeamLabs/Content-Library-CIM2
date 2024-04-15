#### Parser Content
```Java
{
Name = "mcafee-dlp-cef-email-alert-trigger-success-iguard"
Vendor = "McAfee"
Product = "McAfee DLP Endpoint"
TimeFormat = "MMM dd yyyy HH:mm:ss"
Conditions = [
"""CEF:"""
"""|McAfee|iGuard"""
]
Fields = [
"""\send=({time}\w{3} \d+ \d+ \d\d:\d\d:\d\d)"""
"""\d\d:\d\d:\d\d ({host}[^\s]+)"""
"""CEF([^\|]*\|){5}({alert_name}[^|]+)"""
"""CEF([^\|]*\|){6}({alert_severity}[^|]+)"""
"""cs1=({alert_type}.+?)\s+cs1Label"""
"""src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
"""dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
"""fsize=({bytes}\d+)"""
"""app=({protocol}.+?)\s+\w+="""
"""app=SMTP.+?suser=({src_email_address}[^\s]+)"""
"""app=SMTP.+?duser=({email_recipients}.*?)\s+\w+="""
"""app=SMTP.+?duser=({external_address}[^\s,]+)"""
"""app=SMTP.+?cs2="*({email_subject}[^"]*)"""
"""app=SMTP.+?fname=(?:Unknown|({email_attachment}[\s\w.\d]+))\s+\w+"""
"""app=HTTP.+?fname=({target}[^"\s]+)"""
]
ParserVersion = "v1.0.0"


}
```