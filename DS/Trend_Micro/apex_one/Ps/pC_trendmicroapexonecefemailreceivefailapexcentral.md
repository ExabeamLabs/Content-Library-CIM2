#### Parser Content
```Java
{
Name = "trendmicro-apexone-cef-email-receive-fail-apexcentral"
Vendor = "Trend Micro"
Product = "Apex One"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Trend Micro|Apex Central|"""
  """filePath=SMTP"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """dvc=({host}[^=]+?)\s+\w+="""
  """dvchost=+({host}[^=]+?)\s+\w+="""
  """ahost=({host}[^=]+?)\s+\w+="""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\w+="""
  """agt=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+\w+="""
  """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+\w+="""
  """dhost=({dest_host}[^=]+?)\s+\w+="""
  """suser=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """shost=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
  """act=(Unknown|({result}[^=]+?))\s+\w+="""
  """fname=({email_attachments}[^=]+)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```