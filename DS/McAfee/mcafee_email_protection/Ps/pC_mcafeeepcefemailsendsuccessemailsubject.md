#### Parser Content
```Java
{
Name = mcafee-ep-cef-email-send-success-emailsubject
Vendor = "McAfee"
Product = "McAfee Email Protection"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|McAfee|Email Gateway|"""
  """Label=email-subject """
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}[\d.]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\sshost=({src_host}[^\s]+)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sdhost=({dest_host}[^\s]+)"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\seventId=({alert_id}\d+)"""
  """\smsg=({alert_name}.+?)\s+\w+="""
  """CEF:([^|]+?\|){6}({alert_severity}[^|]+)"""
  """CEF:([^|]+?\|){5}({alert_type}[^|]+)"""
  """\ssuser=(?:<>|<?({orig_user}.+?)>?)\s+\w+="""
  """\sduser=(?:<>|({recipients_unfixed}.+?))\s+\w+="""
  """\sduser=<?({dest_email_address}[^\s>,]+)"""
  """\sapp=({protocol}.+?)\s+\w+="""
  """\sdeviceDirection=({direction_code}\d+)"""
  """\scs6=({email_subject}.+?)\s+(?:cs6Label=email-subject|\w+=.*cs6Label=email-subject)"""
  """cs6Label=email-subject.*\scs6=({email_subject}.+?)\s+\w+="""
  """\scs4=({email_attachment}.+?)\s+(?:cs4Label=email-attachments|\w+=.*cs4Label=email-attachments)"""
  """cs4Label=email-attachments.*\scs4=({email_attachment}.+?)\s+\w+="""
  """\sflexNumber1=({outcome_code}.+?)\s+(?:flexNumber1Label=reason-id|\w+=.*flexNumber1Label=reason-id)"""
  """flexNumber1Label=reason-id.*\sflexNumber1=({outcome_code}.+?)\s+\w+="""
  """\sfsize=({bytes}\d+)"""
  """\scn3=({num_recipients}\d+)"""
  """\sfilePath=(({file_path}[^\s]+\\)?({file_name}[^\s]+\.({file_ext}[^\s]+)))"""
]
DupFields = [
  "orig_user->email_address"
  "orig_user->user"
]
ParserVersion = "v1.0.0"


}
```