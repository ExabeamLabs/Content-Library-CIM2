#### Parser Content
```Java
{
Name = cisco-ie-cef-email-send-receive-success-subject
Vendor = "Cisco"
Product = "IronPort Email"
TimeFormat = "epoch"
Conditions = [
  """|CISCO|IronPort|"""
  """cs6Label=Subject"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\ssuser=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\ssuser=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+(\w+=|$)"""
  """\sduser=({email_recipients}[^\s]+)\s+(\w+=|$)"""
  """\sduser=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """\sout=({bytes}\d+)"""
  """\|CISCO\|([^\|]*\|){2}({alert_type}[^\|]+)"""
  """\|CISCO\|([^\|]*\|){3}({alert_name}[^\|]+)"""
  """\|CISCO\|([^\|]*\|){4}({alert_severity}[^\|]+)"""
  """\scn1=({alert_id}\d+)"""
  """MID\s*\d+\s*attachment\s*'({email_attachment}[^']+?(\.({file_ext}[^\.']+))?)'"""
  """\Wfname=({email_attachment}[^\=]+\.({file_ext}[^\=]+))\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```