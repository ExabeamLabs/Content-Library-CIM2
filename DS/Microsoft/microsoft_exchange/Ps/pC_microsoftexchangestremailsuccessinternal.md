#### Parser Content
```Java
{
Name = microsoft-exchange-str-email-success-internal
  Vendor = Microsoft
  Product = Microsoft Exchange
  ParserVersion = "v1.0.0"
  TimeFormat = "epoch_sec"
  Conditions = [ """archive[""", """ internal """ ]
  Fields = [
   """archive\[\d+\]:\s+({message_id}\S+)\s+({time}\d{10}).*?<({src_email_address}[^\s@]+@.+?)>\s+({dest_email_address}[^\s@]+@.+?)\s+\S+\s+({direction}internal)"""
  ]
  DupFields = [ "dest_email_address->email_recipients" ]


}
```