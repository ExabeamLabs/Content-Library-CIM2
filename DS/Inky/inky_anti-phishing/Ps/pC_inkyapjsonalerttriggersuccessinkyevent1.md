#### Parser Content
```Java
{
Name = "inky-ap-json-alert-trigger-success-inkyevent-1"
Vendor = "Inky"
Product = "Inky Anti-Phishing"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
""" inky """
""""threat_level":2"""
""""identifier":"inky-event""""
""""message_id":"""
]
Fields = [
""""reason_htmls\":\s*\[\"({additional_info}[^\]]+?)(\",|\"\])"""
""""reason_titles\":\s*\[\"({alert_name}[^\"]+)"""
""""result_bucket\":\s*\"({alert_severity}[^\"]+)\""""
""""short_reasons\":\s*\s*\[\"({alert_type}[^\"]+)"""
""""client_ip\":\s*\"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
"""\d\d:\d\d:\d\d\.\S+\s({host}[^\s]+)\s+inky"""
""""rcpt_to_addresses\":\s*\[\"({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\""""
""""mail_from\":\s*\"<?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>?""""
""""sender_IP\":\s*\"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\""""
""""subject\":\s*\"({alert_subject}[^\"]+?)\s*\""""
"""({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s\S+\s+inky"""
""""original_url\":\s*\"({malware_url}[^\"]+)\""""
""""tracking_id\":({alert_id}\d+)"""
""""threat_level\":({threat_level}\d+)"""
]
ParserVersion = "v1.0.0"


}
```