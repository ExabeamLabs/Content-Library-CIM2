#### Parser Content
```Java
{
Name = "microsoft-exchange-str-email-receive-success-inbound"
Vendor = "Microsoft"
Product = "Microsoft Exchange"
TimeFormat = "epoch_sec"
Conditions = [
"""archive["""
""" inbound """
]
Fields = [
"""archive\[\d+\]:\s+({message_id}\S+)\s+({time}\d{10}).*?<({email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>\s+({email_recipients}({dest_email_address}[A-Za-z0-9!#$%&'+\/=?^_`~.-]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s+\S+\s+({direction}inbound)"""
]
ParserVersion = "v1.0.0"


}
```