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
"""archive\[\d+\]:\s+({message_id}\S+)\s+({time}\d{10}).*?<({src_email_address}[^\s@]+@.+?)>\s+({dest_email_address}\S+)\s+\S+\s+({direction}inbound)"""
]
DupFields = [
"dest_email_address->email_recipients"
]
ParserVersion = "v1.0.0"


}
```