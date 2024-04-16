#### Parser Content
```Java
{
Name = darktrace-darktrace-mix-email-send-receive-direction
  Vendor = Darktrace
  Product = Darktrace
  TimeFormat = "yyyy-MM-dd HH:mm:ss.SSSSSSZ"
  Conditions = [ """ darktrace """, """"from":""", """"recipients":""", """"direction":""", """"message_id":""" ]
  Fields = [
    """"timestamp":"({time}\d\d\d\d-\d\d-\d\d\s+\d\d:\d\d:\d\d\.\d+((\+|\-)\d\d:\d\d)?)""",
    """"direction":"({direction}[^"]+?)"""",
    """"from":"(|({src_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({src_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)))"""",
    """"message_id":"<({message_id}[^"]+?)>""""
    """"recipients":\["({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))[^\]]*?)"\]""",
    """"subject":"(|({email_subject}[^"]+?))\s*"""",
    """"actions":\[({action}[^\]]+)\]""",
    """"tags":\[({additional_info}[^\]]+)\]"""
  ]
  ParserVersion = "v1.0.0"


}
```