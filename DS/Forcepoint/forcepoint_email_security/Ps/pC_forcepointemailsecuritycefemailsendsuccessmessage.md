#### Parser Content
```Java
{
Name = forcepoint-emailsecurity-cef-email-send-success-message
Vendor = "Forcepoint"
Product = "Forcepoint Email Security"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Forcepoint|Email Security|"""
  """msg="""
]
Fields = [
  """\Wmsg=({email_subject}[^=]+?)\s+\w+="""
  """\Wmsg=\[({email_subject}[^\]]+)"""
  """\Win=({bytes}\d+)"""
  """\Wrt=({time}\d{13})"""
  """\WtrueSrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdvc=(ConnectorIP|({host}[a-fA-F\d.:]+))"""
  """\Wdvchost=({host}[^\s]+)"""
  """\WmessageId=({alert_id}[^\s]+)"""
  """\|Forcepoint\|Email Security\|[^\|]*\|({alert_name}[^\|]*)\|({alert_type}[^\|]*)\|({alert_severity}[^\|]*)\|"""
  """suser=({sender}[^@=]+?@[^\s>]+?)(>)?(\s|\s*$)"""
  """\Wsuser=\s*([^<]+<)?(<)?({sender}[^@=>]+?@[^@=>]+?)(>)?(\s+\w+=|\s*$)"""
  """duser=({dest_email_address}[^@=]+?@[^\s>]+?)(>)?(\s|\s*$)"""
  """\Wduser=\s*([^<]+<)?(<)?({dest_email_address}[^@=>]+?@[^@=>]+?)(>)?(\s+\w+=|\s*$)"""
  """ad.fnameAndfileHash=({email_attachments}[^|]+?)\s*\|\s*({file_hash}[^|\s]+)"""
  """ad.cc=\s*(Email_in_CC|({email_recipients}[^=]+))\s+[\w.\-]+="""
]
ParserVersion = "v1.0.0"


}
```