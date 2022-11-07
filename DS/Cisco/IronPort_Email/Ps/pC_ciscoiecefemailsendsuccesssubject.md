#### Parser Content
```Java
{
Name = cisco-ie-cef-email-send-success-subject
Vendor = "Cisco"
Product = "IronPort Email"
TimeFormat = "epoch"
Conditions = [
  """|CISCO|IronPort|"""
  """cs6Label=Subject"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """\scs1=({user}.+?)\s+(\w+=|$)"""
  """\ssuser=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\ssuser=({email_address}[^\s]+)\s+(\w+=|$)"""
  """\sduser=({email_recipients}[^\s]+)\s+(\w+=|$)"""
  """\sduser=({dest_email_address}[^,\s]+)"""
  """\scs6=({email_subject}.+?)\s+(\w+=|$)"""
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