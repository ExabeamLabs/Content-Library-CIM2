#### Parser Content
```Java
{
Name = "fortinet-utm-kv-email-receive-success-dlp"
Vendor = "Fortinet"
Product = "Fortinet UTM"
TimeFormat = "yyyy-MM-dd' time='HH:mm:ss"
Conditions = [
  """subtype=dlp"""
  """service=SMTP"""
]
Fields = [
  """\Wdate=({time}\d\d\d\d-\d\d-\d\d time\=\d\d:\d\d:\d\d)"""
  """\Wdevname="*({host}[^\s"]+)"*(\s|")"""
  """\Wsubtype="({alert_type}[^"]+)""""
  """\Waction=({action}.+?)\s+\w+="""
  """\Wsrcip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wdstip=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\Wrcvdbyte=({bytes_in}\d+)"""
  """\Wsentbyte=({bytes_out}\d+)"""
  """\Wsrcport=({src_port}\d+)"""
  """\Wdstport=({dest_port}\d+)"""
  """\Wseverity=({alert_severity}.*?)\s+\w+="""
  """\Wfiltercat="*(none|({category}.*?))"*\s+\w+="""
  """\Wfrom="\(*({src_email_address}.*?@.*?)\)*"\s+\w+="""
  """\Wfilesize=({bytes}\d+)\s+\w+="""
  """\Wfilename="({email_attachments}.*?)"\s+\w+="""
  """\Wrecipient="({dest_email_address}.*?@.*?)"\s+\w+="""
  """\Wsubject="\s*({email_subject}.*?)\s*"\s+\w+="""
  """\Weventtype=({alert_type}[^\s]+?)\s+\w+="""
  """\Wsubtype=({alert_name}[^\s]+?)\s+\w+="""
  """\Wsessionid=({alert_id}\d+)"""
  """\Wdirection=({direction}[^\s]+?)\s""",
  """\Wtz="?({tz}[+-]\d+)"""
]
DupFields = [
  "bytes_out->bytes"
  "dest_email_address->email_recipients"
]
ParserVersion = "v1.0.0"


}
```