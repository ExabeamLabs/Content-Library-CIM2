#### Parser Content
```Java
{
Name = symantec-esc-str-email-deliveryfailure
    ParserVersion = v1.0.0
    Vendor = Symantec
    Product = Symantec Email Security
    TimeFormat = "epoch_sec"
    Conditions = [
"""|DELIVERY_FAILURE|"""
    ]
    Fields = [
      """\s({host}[\w\.-]+)\s+\w+\[\d+\]:""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|(|({action}[^\|]+))\|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}:\d+\|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""",
      """\s*({time}\d{10})\|(|({alert_id}[^\|]+))\|(|({action}[^\|]+))\|\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}:\d+\|(|({failure_reason}[^\|]+))\|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
      """DELIVERY_FAILURE\|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    ]
  

}
```