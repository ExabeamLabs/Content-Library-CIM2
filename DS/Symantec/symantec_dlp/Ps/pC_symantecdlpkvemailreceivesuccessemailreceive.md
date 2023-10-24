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
  """, data-sent=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+(\+|\-)\d+)"""
  """^.*?, Last Name =(|({last_name}[^,]+?))(,|\})"""
  """^.*?, First Name =(|({first_name}[^,]+?))(,|\})"""
  """, attachment-name1=(|({email_attachment}[^,]+?))(,|\})"""
  """, sender-email=(|(\w+:/+)?({src_email_address}[^,:@]+?@[^@,:]+?))(,|\})"""
  """, monitor-host=(|({host}[^,]+?))(,|\})"""
  """, subject=(|({email_subject}[^,]+?))\s*(,|\})"""
  """, protocol=(|({protocol}[^,]+?))(,|\})"""
  """, recipient-email1=(|(\w+:/+)?({dest_email_address}[^,:@]+?@[^,:@]+?))(,|\})"""
  """\+\d+;\w+;({email_attachments}[^;]+;([^;]*;){3}([^;]+;)*)"""
]
DupFields = [
  "src_email_address->external_address"
]
ParserVersion = "v1.0.0"


}
```