#### Parser Content
```Java
{
Name = dg-ep-leef-email-send-success-28
  Conditions = [ """LEEF:""", """|Digital Guardian|Digital Guardian|""", """DigitalGuardian-Events""", """|28|""" ]
  ParserVersion = "v1.0.0"

leef-digitalguardian-dlp-email-alert-out = {
  Vendor = Digital Guardian
  Product = Digital Guardian Endpoint Protection
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Fields = [
    """devTime=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w\-.]+) LEEF:""",
    """accountName =(({email_domain}[^\\]+)\\+)?({user}[^\\\s]+?)\s*(\w+=|$)""",
    """IdentHostName =(({email_domain}[^\\])+\\+)?({dest_host}[\w\-.]+?)\s*(\w+=|$)""",
    """src=({src_ip}[A-Fa-f:\d.]+)""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
    """EmailSender=({email_address}.+?)\s*(\w+=|$)""",
    """usrName =(?![^\s]+@[^\s]+)(({email_domain}[^\\]+)\\+)?({user}[^\\\s@]+)\s*(\w+=|$)""",
    """usrName =(?=[^\s]+@[^\s]+)({email_address}[^\s@]+@[^\s]+)""",
    """EmailRecipient=(|({dest_email_address}[^\s,;]+))""",
    """EmailRecipient=(|({email_recipients}.+?))\s*(\w+=|$)""",
    """EmailRecipient=({external_address}[^@]+@[^@\s,;]+).*?\s*(\w+=|$)""",
    """EmailSubject=(|({email_subject}.+?))\s*(\w+=|$)""",
    """sev=({alert_severity}\d+)""",
    """srcBytes=({bytes}\d+)""",
    """FileSizeMB=({bytes}\d+)""",
    """FileSize({bytes_unit}MB)""",
    """DestinationFile=(|({email_attachments}[^\.]+\.({file_ext}.+?)))\s*(\w+=|$)""",
  
}
```