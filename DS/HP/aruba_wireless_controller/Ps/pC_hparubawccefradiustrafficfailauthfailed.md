#### Parser Content
```Java
{
Name = "hp-arubawc-cef-radius-traffic-fail-authfailed"
Vendor = "HP"
Product = "Aruba Wireless controller"
TimeFormat = ["epoch", "epoch_sec", "MMM dd yyyy HH:mm:ss"]
Conditions = [
  """|Aruba Networks|ClearPass|"""
  """|Failed Authentications|"""
]
Fields = [
  """rt=({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d)"""
  """\Wrt=({time}\d{10,13})"""
  """\Wdvc=({host}.+?)\s+(w+=|$)"""
  """\Wdvchost=({host}.+?)\s+([\w\.]+=|$)"""
  """\Wreason=({failure_reason}.+?)\s+([\w\.]+=|$)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wcs1=({auth_server}.+?)\s+([\w\.]+=|$)"""
  """\Wduser=(host\/({src_host}[\w\-.]+)|({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({dest_mac}(((\w\d)|(\d\w))\-){5}((\w\d)|(\d\w)))|({=dest_mac}((\w\d)|(\d\w))(\w){10})|({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^=]+)|(({=domain}[^\\\s]+)\\+)?({=user}[^\s]+))\s+\w+="""
  """\Wdpriv=({access_type}.+?)\s+([\w\.]+=|$)"""
  """\Wdmac=({dest_mac}.+?)\s+([\w\.]+=|$)"""
]
ParserVersion = "v1.0.0"


}
```