#### Parser Content
```Java
{
Name = cisco-asa-cef-radius-traffic-success-113004
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|CISCO|ASA|"""
  """|113004|"""
  """AAA user authentication Successful"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sdhost=({dest_host}[^\s]+)"""
  """\sduser=({full_name}(\w+\s+)+\w+)\s+(\w+=|$)"""
  """\sduser=({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
  """\sduser=({email_address}[^\s@]+@[^\s@]+)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```