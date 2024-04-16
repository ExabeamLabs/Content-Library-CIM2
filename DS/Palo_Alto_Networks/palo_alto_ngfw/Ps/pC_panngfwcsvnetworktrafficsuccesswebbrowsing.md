#### Parser Content
```Java
{
Name = pan-ngfw-csv-network-traffic-success-webbrowsing
  Vendor = Palo Alto Networks
  Product = Palo Alto NGFW
  ParserVersion = "v1.0.0"
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """,DECRYPTION,""" ]
  Fields = [
   """:\d\d:\d\d\s+({host}[\w\-\.]+)\s"""
   """({event_category}DECRYPTION)""" 
   """,DECRYPTION,([^,]*,){3}({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})),({src_translated_ip}[a-fA-F\d.:]+),""",
   """,DECRYPTION,([^,]*,){6,9}(({domain}[^\\,]+)\\+)({user}[\w\.\-]{1,40}\$?)"""
   """,DECRYPTION,([^,]*,){20}(?:|({src_port}\d+)),(?:|({dest_port}\d+)),(?:[^,]*,){3}(?:|({protocol}[^,]+)),({result}[^,]+),"""
   """DECRYPTION,([^,]*,){39}({policy_name}[^,]+),"""
   """DECRYPTION,([^,]*,){92}({src_host}[\w\-\.]+),"""
   """,DECRYPTION,([^,]*,){10}({app}[^,]+),"""
   """,DECRYPTION,([^,]*,){7}({rule}[^,]+),"""
   """,DECRYPTION,([^,]*,){12}({src_network_zone}[^,]+),({dest_network_zone}[^,]+),"""
  ]


}
```