#### Parser Content
```Java
{
Name = cisco-asa-cef-vpn-login-success-722051
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
  """|CISCO|ASA|"""
  """|722051|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\sdvchost=({dest_host}[^\s]+)"""
  """\sduser=({full_name}(\w+\s+)+\w+)\s+(\w+=|$)"""
  """\sduser=({user}[^\s@]+)\s+(\w+=|$)"""
  """\sduser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)"""
  """\sdhost=(?: |<?({src_ip}[a-fA-F\d.:]+)|({src_host}[^\s]+)>?)\s+\w+="""
  """\ssrc=({src_translated_ip}[a-fA-F\d.:]+)"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sc6a3=(?: |0:0:0:0:0:0:0:0|({src_translated_ip}.+?))\s+\w+="""
]
DupFields = [
  "user->account"
]
ParserVersion = "v1.0.0"


}
```