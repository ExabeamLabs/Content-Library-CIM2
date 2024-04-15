#### Parser Content
```Java
{
Name = "hp-arubawc-kv-endpoint-login-success-loggedin"
Product = "Aruba Wireless controller"
Conditions = [
  """|Aruba Networks|ClearPass|"""
  """|Logged in users|"""
]
Vendor = "HP"
TimeFormat = "epoch"
Fields = [
  """\Wrt=({time}\d{13})"""
  """\Wdvc=({host}.+?)\s+(w+=|$)"""
  """\Wdvchost=({host}.+?)\s+([\w\.]+=|$)"""
  """\Wsrc=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\Wduser=(?:({user_type}host)/)?(({domain}[^\\=]+)\\+)?({user}[^\s\\\/=\.]+)?\s+([\w\.]+=|$)"""
  """\Wdpriv=({access_type}.+?)\s+([\w\.]+=|$)"""
  """\Wdmac=({dest_mac}.+?)\s+([\w\.]+=|$)"""
  """\Wad\.ArubaClearpassRADIUSAcctNASPortType=({network}.+?)\s+([\w\.]+=|$)"""
  """\Wad\.ArubaClearpassRADIUSAcctSessionId=({session_id}.+?)\s+([\w\.]+=|$)"""
  """\Wdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\s+([\w\.]+=|$)"""
  """\Wcs1=({session_id}[^\s]+).*?cs1Label=Session Id"""
  """cs1Label=Session Id.*?\Wcs1=({session_id}[^\s]+)"""
  """\Wcs3=({network}[^\s]+).*?cs3Label=Port Type"""
  """cs3Label=Port Type.*?\Wcs3=({network}[^\s]+)"""
]
DupFields = [
  "dest_ip->auth_server"
]
ParserVersion = "v1.0.0"


}
```