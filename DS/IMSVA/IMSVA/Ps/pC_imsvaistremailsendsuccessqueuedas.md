#### Parser Content
```Java
{
Name = imsva-i-str-email-send-success-queuedas
Vendor = "IMSVA"
Product = "IMSVA"
TimeFormat = "yyyy/MM/dd HH:mm:ss Z"
Conditions = [
  """ imsva"""
  """: queued as"""
  """sent"""
]
Fields = [
  """\s({host}imsva\d+\s+[\w.\-]+)"""
  """({time}\d\d\d\d\/\d\d\/\d\d \d\d:\d\d:\d\d (\+|\-)\d\d:\d\d)\s+([^\s]+)(\s+[^\s]+){7,9}\s+({email_address}[^\s@]+@[^\s@;]+)\s+(({email_recipients}({dest_email_address}[^\s@;]+@[^\s@;]+)[^\s]*)\s+)?\s*(|({email_subject}.+?))\s+(#null#|({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))\s+(.+?\[({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\])?"""
  """\s({bytes}\d+)\s+bytes in """
  """\d\d\d\d \w+ \d\d \d\d:\d\d:\d\d (\+|\-)\d\d:\d\d\s+(?!\d\d\d\d \w+ \d\d)\d+\s+({email_attachments}({email_attachment}[^.]+\.({file_ext}[^\s;]+))(;\s+[^;]+?)*?)\s*$"""
]
ParserVersion = "v1.0.0"


}
```