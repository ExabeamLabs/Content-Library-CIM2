#### Parser Content
```Java
{
Name = zeek-z-json-alert-trigger-notice
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch"
  Conditions = [ """ zeek_notice """, """id.""" ]
  Fields = [
    """"ts"+:({time}\d+)""",
    """"uid"+:"+({user_uid}[^"]+)""",
    """"id\.orig_h"+:"+({src_ip}[^"]+)""",
    """"id\.orig_p"+:({src_port}\d+)""",
    """"id\.resp_h"+:"+({dest_ip}[^"]+)""",
    """"id\.resp_p"+:({dest_port}\d+)""",
# fuid is removed
    """"proto"+:"+({protocol}[^"]+)""",
# note is removed
    """"msg"+:"+({failure_reason}[^"]+)""",
    """"sub"+:"+({email_subject}[^"]+)""",
    """"src"+:"+({src_ip}[^"]+)""",
    """"dst"+:"+({dest_ip}[^"]+)""",
    """"peer_descr"+:"+({dest_interface}[^"]+)""",
    """"actions"+:\["+({action}[^"]+)""",
# suppress_for is removed
  ]
  ParserVersion = "v1.0.0"


}
```