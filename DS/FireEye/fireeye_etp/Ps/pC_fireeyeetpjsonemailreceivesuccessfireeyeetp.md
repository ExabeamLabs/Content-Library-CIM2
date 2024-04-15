#### Parser Content
```Java
{
Name = "fireeye-etp-json-email-receive-success-fireeyeetp"
Vendor = "FireEye"
Product = "FireEye ETP"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
Conditions = [
  """"alert_type":"""
  """"malware_md5":""""
  """"rcpt_to":""""
  """"mail_from":""""
  """"subject":""""
  """FireEyeETP"""
]
Fields = [
  """"timestamp":"({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+)"""
  """"alert_type":\[?"({alert_type}[^"]+)"""
  """"product":"({alert_name}[^"]+)"""
  """"malware_md5":"({hash_md5}[^"]+)"""
  """"email":\{[^\}]*?"status":"({action}[^"]+)"""
  """"source_ip":"({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """"rcpt_to":"({email_recipients}({dest_email_address}[^"\s@;,]+@[^"\s@;,]+)[^"]*)"""
  """"mail_from":"({src_email_address}[^"\s@;,]+@[^"\s@;,]+)"""
  """"subject":"({email_subject}[^"]+)"""
  """"attachment":"({email_attachments}({email_attachment}[^",]+)[^"]*)"""
  """"last_malware":"({malware_name}[^"]+)"""
  """"id":"({alert_id}[^"]+)"""
]
ParserVersion = "v1.0.0"


}
```