#### Parser Content
```Java
{
Name = zeek-z-json-alert-trigger-notice
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch"
  Conditions = [ """ zeek_notice """, """id.""" ]
  Fields = [
    """"ts"+:({time}\d{13})""",
    """"uid"+:"+({user_uid}[^"]+)""",
    """"id\.orig_h"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.orig_p"+:({src_port}\d+)""",
    """"id\.resp_h"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"id\.resp_p"+:({dest_port}\d+)""",
# fuid is removed
    """"proto"+:"+({protocol}[^"]+)""",
# note is removed
    """"msg"+:"+({failure_reason}[^"]+)""",
    """"sub"+:"+({email_subject}[^"]+)""",
    """"src"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"dst"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"peer_descr"+:"+({dest_interface}[^"]+)""",
    """"actions"+:\["+({action}[^"]+)""",
# suppress_for is removed
  ]
  ParserVersion = "v1.0.0"


}
```