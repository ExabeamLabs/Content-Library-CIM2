#### Parser Content
```Java
{
Name = cisco-asa-cef-endpoint-authentication-success-611101
Vendor = "Cisco"
Product = "Cisco Adaptive Security Appliance"
TimeFormat = "epoch"
Conditions = [
  """|CISCO|ASA|"""
  """|611101|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\|({event_code}611101)"""
  """\sduser=(?:({domain}[^\s]+?)\\+)?({user}[\w\.\-]{1,40}\$?)\s+([\w.]+=|$)"""
  """\sad\.Username=<?(?:({domain}[^\s]+?)\\+)?({user}[\w\.\-]{1,40}\$?)>?\s+([\w.]+=|$)"""
  """\sdhost=({dest_host}.+?)\s+([\w.]+=|$)"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sdvc=({host}.+?)\s+([\w.]+=|$)"""
  """\sdvchost=({host}.+?)\s+([\w.]+=|$)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```