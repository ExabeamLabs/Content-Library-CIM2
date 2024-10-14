#### Parser Content
```Java
{
Name = accellion-kw-kv-email-send-success-draftcreated
  Product = Kiteworks
  Conditions = [ """Activity: Created draft""", """with files""" ]
  ParserVersion = "v1.0.0"

q-kiteworks-email = {
  Vendor = Accellion
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """\w+\s+\d+ \d+:\d+:\d+\s+({host}[\w.\-]+)\s+""",
    """({email_address}[^@\s]+@[^\s]+)\s+id=[^,]+,\s*({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?,\s*Activity:""",
    """\sSubject:\s*"*\s*({email_subject}[^"]+)\s*"*""",
    """\sTo:\s*({email_recipients}.+?)\s*with files \[({email_attachments}.+?)\]""",
    """\sTo:\s*({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",

  
}
```