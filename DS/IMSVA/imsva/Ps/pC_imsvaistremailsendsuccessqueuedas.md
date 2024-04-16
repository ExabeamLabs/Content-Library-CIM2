#### Parser Content
```Java
{
Name = imsva-i-str-email-send-success-queuedas
Vendor = "IMSVA"
Product = "IMSVA"
TimeFormat = ["yyyy MMM dd HH:mm:ss", "yyyy/MM/dd HH:mm:ss Z"]
Conditions = [
  """ imsva"""
  """: queued as"""
  """sent"""
]
Fields = [
  """\simsva\d+\s+({host}[\w.\-]+)"""
  """({time}\d+\s+\w+\s+\d+\s+\d+:\d+:\d+)"""
  """(\d+\s+\w+\s+\d+\s+\d+:\d+:\d+)(\s*(\+|\-)\d\d:\d\d)?\s+([^\s]+)(\s+[^\s]+){7,9}\s+({src_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))\s+(({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))[^\s]*)\s+)?\s*(|({email_subject}.+?))\s+(#null#|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+(.+?\[({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\])?"""
  """\s({bytes}\d+)\s+bytes in """
  """\d\d\d\d \w+ \d\d \d\d:\d\d:\d\d (\+|\-)\d\d:\d\d\s+(?!\d\d\d\d \w+ \d\d)\d+\s+({email_attachments}({email_attachment}[^.]+\.({file_ext}[^\s;]+))(;\s+[^;]+?)*?)\s*$"""
]
DupFields = [ "dest_email_address->external_address" ]
ParserVersion = "v1.0.0"


}
```