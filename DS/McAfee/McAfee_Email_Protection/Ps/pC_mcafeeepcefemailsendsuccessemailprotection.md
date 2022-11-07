#### Parser Content
```Java
{
Name = mcafee-ep-cef-email-send-success-emailprotection
Vendor = "McAfee"
Product = "McAfee Email Protection"
TimeFormat = "epoch"
Conditions = [
  """McAfee|Data Loss Prevention"""
  """|DLP: Email Protection|"""
]
Fields = [
  """(\s|\|)rt=({time}.+?)\s+([\w\.-]+=|$)"""
  """\|DLP: Email Protection\|({alert_severity}.+?)\|"""
  """(\s|\|)deviceSeverity=({alert_severity}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)shost=({src_host}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)src=({src_ip}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)suser=({user}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)sntdom=({domain}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)sproc=({process_name}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)cs1=({alert_name}.+?)\s+cs2="""
  """(\s|\|)cs2=.*?({email_address}[^<\s@']+?@[^<>\s;']+).*?\s+cs3="""
  """(\s|\|)cs5=Recipients:\s*'*({dest_email_address}[^;']+).*?\s+Recipients Cc:"""
  """(\s|\|)cs5=Recipients:[^;]+?<({dest_email_address}[^>]+)>.*?Recipients Cc:"""
  """(\s|\|)cs5=Recipients:\s*({email_recipients}.+?)\s+Recipients Cc:"""
  """(\s|\|)cs6=({email_subject}.+?)\s+([\w\.-]+=|$)"""
  """(\s|\|)fname=({file_name}[^\.]+({file_ext}.+?))\s+([\w\.-]+=|$)"""
  """(\s|\|)fsize=({bytes}\d+)\s+([\w\.-]+=|$)"""
  """(\s|\|)eventId=({alert_id}\d+)\s"""
  """({direction}OUTGOING)_EMAIL"""
  """({alert_type}DLP: Email Protection)"""
  """(\s|\|)act=({action}[^=]+?)\s+([\w\.-]+=|$)"""
]
DupFields = [
  "dest_email_address->target"
  "file_name->email_attachments"
]
ParserVersion = "v1.0.0"


}
```