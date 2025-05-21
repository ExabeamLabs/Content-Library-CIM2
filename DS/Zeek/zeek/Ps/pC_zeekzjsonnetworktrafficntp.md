#### Parser Content
```Java
{
Name = zeek-z-json-network-traffic-ntp
  Vendor = Zeek
  Product = Zeek
  TimeFormat = "epoch_sec"
  Conditions = [ """ zeek_ntp """, """id.""" ]
  Fields = [
    """"ts"+:({time}\d{10})""",
    """"uid"+:"+({user_uid}[^"]+)""",
    """"id\.orig_h"+:"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """"id\.orig_p"+:({src_port}\d+)""",
    """"id\.resp_h"+:"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """"id\.resp_p"+:({dest_port}\d+)""",
    """"version"+:({version}\d+)""",
# mode is removed
# stratum is removed
# poll is removed
# precision is removed
# root_delay is removed
# root_disp is removed
# ref_id is removed
# ref_time is removed
# org_time is removed
# rec_time is removed
# xmt_time is removed
# num_exts is removed
  ]
  ParserVersion = "v1.0.0"


}
```