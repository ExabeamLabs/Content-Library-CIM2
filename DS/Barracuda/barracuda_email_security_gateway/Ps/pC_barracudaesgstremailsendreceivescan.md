#### Parser Content
```Java
{
Name = barracuda-esg-str-email-send-receive-scan
  ParserVersion = v1.0.0
  Vendor = Barracuda
  Product = Barracuda Email Security Gateway
  TimeFormat = "epoch_sec"
  Conditions = [ 
"""scan: """
""" SCAN """ 
]
  Fields = [
    """\Wscan:\s+(?:-|({host}[\w\-\.]+))\[({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\]\s+(?:-|({alert_id}[^\s]+)\-\S+)\s+({time}\d{10})\s+\d+\s+SCAN\s+\S+\s+(?:-|({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s+(?:-|({dest_email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({dest_email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+)))\s+(?:-|({spam_score}\S+))\s+({result}\d+)\s+(?:-|({failure_code}[^\s]+))\s+\S+\s+SZ:({bytes}\d+)\s+SUBJ:(|({email_subject}.+?))\s"""
  ]
  DupFields = [ "email_address->email_user" ]


}
```