#### Parser Content
```Java
{
Name = "accellion-kw-json-file-download-success-description"
Conditions = [
  """url_host"""
  """app_host"""
  """description"""
  """download_email_zip"""
  """event"""
]
ExtractionType = json
ParserVersion = "v1.0.0"

hornet-dlp-email = {
    Vendor = Hornet
    Product = Hornetsecurity Cloud Email Security Services
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Fields = [
      """date=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """dir=({direction}1|2)""",
      """main_domain=({domain}[^=]+?)\s*(\w+=|$)""",
      """from=({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """to=({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """\stype=({result}\d+)""",
      """reason="({additional_info}[^"]+)""",
      """src_host=((?i)unknown|({src_host}[^\s]+))""",
      """src_ip=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """dst_ip=(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+))""",
      """msgid="({message_id}[^"]+)""",
      """subject="[\s ]*({email_subject}[^"]+?)[\s ]*"""",
      """attachments="[^0"]#({email_attachments}[^"]+)""",
    
}
```