#### Parser Content
```Java
{
Name = "fortinet-utm-kv-email-receive-success-emailreceived"
Vendor = "Fortinet"
Product = "Fortinet UTM"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """from="""
  """to="""
  """subject="""
  """message_name="""
  """folder_description="""
  """action="""
]
Fields = [
  """({time}\d+-\d+-\d+T\d+:\d+:\d+\.\d+Z)\s+({host}[\w\-.]+)"""
  """\Waction=({action}[^;]+)"""
  """\Wfrom=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """\Wto=({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^;]*)"""
  """\Wsubject=({email_subject}.*?);\s+(\w+=|$)"""
  """\Wmessage_name=({message_name}.*?);\s+(\w+=|$)"""
  """\Wmessage_size=({bytes}\d+)"""
  """\Wfolder_description=({additional_info}.*?);\s+(\w+=|$)"""
  """\Wfilename=({file_name}[^\.]+\.({file_ext}.*?));\s+(\w+=|$)"""
  """\Wfiletype=({file_type}.*?);\s+(\w+=|$)"""
  """({direction}Outbound|Inbound)"""
  """Sent To:\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
  """\Wtz="?({tz}[+-]\d+)"""
]
DupFields = [
  "file_name->email_attachments"
]
ParserVersion = "v1.0.0"


}
```