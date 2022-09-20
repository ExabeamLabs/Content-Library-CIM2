#### Parser Content
```Java
{
Name = hornet-email-kv-email-receive-success-1
  Conditions = [ """main_domain=""", """owner=""", """smtp_code=""", """crypt_type=""", """from_hdr=""", """update_nr=""", """type=1""" ]
  ParserVersion = "v1.0.0"

hornet-dlp-email = {
    Vendor = Hornet
    Product = Hornet Email
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
    Fields = [
      """date=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
      """dir=({direction}1|2)""",
      """main_domain=({domain}[^=]+?)\s*(\w+=|$)""",
      """from=({email_address}[^@\s]+?@[^\s]+)""",
      """to=({dest_email_address}[^@\s]+?@[^\s]+)""",
      """\stype=({result}\d+)""",
      """reason="({additional_info}[^"]+)""",
      """src_host=((?i)unknown|({src_host}[^\s]+))""",
      """src_ip=({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
      """dst_ip=(({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({dest_host}[^\s]+))""",
      """msgid="({message_id}[^"]+)""",
      """subject="[\s ]*({email_subject}[^"]+?)[\s ]*"""",
      """attachments="[^0"]#({email_attachments}[^"]+)""",
    
}
```