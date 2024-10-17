#### Parser Content
```Java
{
Name = cisco-secureemail-cef-email-send-success-logevent
Vendor = "Cisco"
Product = "Cisco Secure Email"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """CEF"""
  """ Email Security Appliance|"""
  """ ESAMID="""
]
Fields = [
  """suser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """\sduser=({email_recipients}[^\s]+)\s+(\w+=|$)"""
  """\sduser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """sourceAddress=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """ESAMID=({alert_id}\d+)"""
  """\|Cisco\|([^\|]*\|){2}({alert_type}[^\|]+)"""
  """\|Cisco\|([^\|]*\|){3}({alert_name}[^\|]+)"""
  """\|Cisco\|([^\|]*\|){4}({alert_severity}[^\|]+)"""
  """deviceDirection=({direction}\d)"""
  """\Wact=({action}[^=]+?)\s*\w+="""
  """msg='({email_subject}[^~]+?)'\s\w+?="""
  """ESAAttachmentDetails=\{'({attachment}[^']+?)'"""
]
ParserVersion = "v1.0.0"


}
```