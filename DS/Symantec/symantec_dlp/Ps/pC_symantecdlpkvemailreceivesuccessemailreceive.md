#### Parser Content
```Java
{
Name = "symantec-dlp-kv-email-receive-success-emailreceive"
Vendor = "Symantec"
Product = "Symantec DLP"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """, attachment-name"""
  """, recipient-email1="""
  """, sender-email="""
]
Fields = [
  """, date-sent=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d+)"""
  """^.*?, Last Name =(|({last_name}[^,]+?))(,|\})"""
  """^.*?, First Name =(|({first_name}[^,]+?))(,|\})"""
  """, attachment-name1=(|({email_attachment}[^,]+?))(,|\})"""
  """, sender-email=(|(\w+:/+)?({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))(,|\})"""
  """, monitor-host=(|({host}[^,]+?))(,|\})"""
  """, subject=(|({email_subject}[^,]+?))\s*(,|\})"""
  """, protocol=(|({protocol}[^,]+?))(,|\})"""
  """, recipient-email1=(|(\w+:/+)?({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))(,|\})"""
  """\+\d+;\w+;({email_attachments}[^;]+;([^;]*;){3}([^;]+;)*)"""
]
ParserVersion = "v1.0.0"


}
```