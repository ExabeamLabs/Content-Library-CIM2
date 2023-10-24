#### Parser Content
```Java
{
Name = "clearswiftseg-cseg-str-email-send-receive-msgsiacpt"
Vendor = "Clearswift"
Product = "Clearswift Secure Email Gateway"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """msgs IACPT|"""
]
Fields = [
  """([^\|]*\|){3}({src_email_address}[^\|]+)"""
  """([^\|]*\|){4}({dest_email_address}[^\|,]+)"""
  """([^\|]*\|){4}({email_recipients}[^\|]+)"""
  """([^\|]*\|){5}({email_subject}[^\|]+)"""
  """([^\|]*\|){6}({result}[^\|]+)"""
  """([^\|]*\|){7}(|({email_attachment}[^.]+.({file_ext}[^,"|]+)[^\|]+))\|"""
]
ParserVersion = "v1.0.0"


}
```