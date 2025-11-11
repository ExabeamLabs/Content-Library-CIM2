#### Parser Content
```Java
{
Name = microsoft-exchange-str-email-send-success-outbound
  Vendor = Microsoft
  Product = Microsoft Exchange
  TimeFormat = "epoch_sec"
  Conditions = [ """archive[""", """ outbound """ ]
  Fields = [
    """archive\[\d+\]:\s+({message_id}\S+)\s+({time}\d{10}).*?<({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))>\s+({email_recipients}({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s+\S+\s+({direction}outbound)"""
  ]
  ParserVersion = "v1.0.0"


}
```