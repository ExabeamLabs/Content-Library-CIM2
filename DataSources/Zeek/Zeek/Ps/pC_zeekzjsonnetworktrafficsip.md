#### Parser Content
```Java
{
Name = zeek-z-json-network-traffic-sip
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """ zeek_sip """, """id.""" ]
  Fields = [
    """"ts"+:({time}\d{10})""",
    """"uid"+:"+({user_uid}[^"]+)""",
    """"id\.orig_h"+:"+({src_ip}[^"]+)""",
    """"id\.orig_p"+:({src_port}\d+)""",
    """"id\.resp_h"+:"+({dest_ip}[^"]+)""",
    """"id\.resp_p"+:({dest_port}\d+)""",
    """"trans_depth"+:({trans_depth}\d+)""",
# response_from is removed
# response_to is removed
# request_path is removed
# response_path is removed
    """"status_code"+:({status_code}\d+)""",
    """"status_msg"+:"+({status_msg}[^"]+)""",
# response_body_len is removed
# content_type is removed
  ]
  ParserVersion = "v1.0.0"


}
```