#### Parser Content
```Java
{
Name = microsoft-exchange-str-email-send-success-outbound
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "epoch_sec"
  Conditions = [ """archive[""", """ outbound """ ]
  Fields = [
    """archive\[\d+\]:\s+({message_id}\S+)\s+({time}\d{10}).*?<({src_email_address}.+?)>\s+({dest_email_address}[^\s@]+@.+?)\s+\S+\s+({direction}outbound)"""
  ]
  DupFields = [ "dest_email_address->email_recipients" ]
  ParserVersion = "v1.0.0"


}
```