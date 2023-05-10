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
    """({email_address}[^@\s]+@[^\s]+)\s+id=[^,]+,\s*({src_ip}[a-fA-F\d.:]+),\s*Activity:""",
    """\sSubject:\s*"*\s*({email_subject}[^"]+)\s*"*""",
    """\sTo:\s*({email_recipients}.+?)\s*with files \[({email_attachments}.+?)\]""",
    """\sTo:\s*({dest_email_address}[^,@]+@[^\s,]+)""",

  ]
  DupFields = [ "dest_email_address->external_address" 
}
```