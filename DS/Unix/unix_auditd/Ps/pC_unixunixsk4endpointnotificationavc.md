#### Parser Content
```Java
{
Name = unix-unix-sk4-endpoint-notification-avc
  ParserVersion = v1.0.0
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"type":"AVC"""", """:"avc:  denied """, """"message":""", """"logger.account":""" ]
  Fields = ${DLUnixParsersTemplates.unix-template-dl.Fields} [
    """"type":"({event_name}[^"]+)"""",
    """pid\\?=({process_id}\d+)""",
# src_context is removed
# target_context is removed
    """tclass\\?=({file_type}[^=]+)\s+\w+\\?=""",
    """"+avc:\s+({access}denied)\s+\{\s+({permission}[^\}]+)\s+\}""",
# target_name is removed
# inode_number is removed
  ]
  DupFields = [ "target_name->file_name" ]

unix-template-dl = {
    Vendor = Unix
    Product = Unix Auditd
    TimeFormat = epoch
    Fields = [
      """\Wrt=({time}\d{13})""",
      """\Wdvc=({host}[^\s]+)""",
      """\Wdvchost=({host}[^\s]+)""",
      """CEF:([^\|]*\|){4}({additional_info}[^\|]+)""",
      """CEF:([^\|]*\|){5}({event_code}[^\|]+)""",
      """\WeventId=({alert_id}\d+)""",
      """\Wsuser=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))""",
    
}
```