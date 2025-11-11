#### Parser Content
```Java
{
Name = microsoft-exchange-cef-email-receive-incoming
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|Exchange Server|"""
  """flexString1=Incoming"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}[\d.]+)"""
  """\sdvchost=\[?({host}[^\s\]]*)"""
  """\scs6=({return_path}.+?)\s+\w+="""
  """\ssuser=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@([^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+\w+="""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[1-9]|)\d)\.?\b){4}))"""
  """\sduser=(({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))|({orig_user}({user}[\w\.\-\!\#\^\~]{1,40}\$?)))"""
  """\sduser=({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)).*?)\s+\w+="""
  """\smsg=({email_subject}.+?)\s+\w+="""
  """\|RECEIVE\|RECEIVE\|.+?in=({bytes}\d+)"""
  """\|SEND\|SEND\|.+?out=({bytes}\d+)"""
  """\seventId=({alert_id}\d+)"""
  """\ssourceServiceName =({alert_name}[^\s]+)"""
  """\ssourceServiceName =({alert_type}[^\s]+)"""
  """CEF([^\|]*\|){6}({alert_severity}[^|]+)"""
  """CEF([^\|]*\|){5}({action}[^|]+)"""
  """({direction}i)"""
  """\scategoryOutcome=(\/)?({result}[^\s]*)"""
]
ParserVersion = "v1.0.0"


}
```