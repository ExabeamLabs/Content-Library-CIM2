#### Parser Content
```Java
{
Name = "hp-arubawc-cef-radius-traffic-fail-authfailed"
Vendor = "HP"
Product = "Aruba Wireless controller"
TimeFormat = "epoch"
Conditions = [
  """|Aruba Networks|ClearPass|"""
  """|Failed Authentications|"""
]
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}.+?)\s+(w+=|$)"""
  """\Wdvchost=({host}.+?)\s+([\w\.]+=|$)"""
  """\Wreason=({failure_reason}.+?)\s+([\w\.]+=|$)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wcs1=({auth_server}.+?)\s+([\w\.]+=|$)"""
  """\Wduser=(?:({user_type}host)/)?(({domain}[^\\]+)\\+)?({user}[^\s\\\/]+)\s+([\w\.]+=|$)"""
  """\Wdpriv=({access_type}.+?)\s+([\w\.]+=|$)"""
  """\Wdmac=({dest_mac}.+?)\s+([\w\.]+=|$)"""
]
ParserVersion = "v1.0.0"


}
```