#### Parser Content
```Java
{
Name = "citrix-cgateway-cef-vpn-logout-success-netscaler"
Vendor = "Citrix"
Product = "Citrix Gateway"
TimeFormat = "epoch"
Conditions = [
  """|Citrix|NetScaler|"""
  """LOGOUT|"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\s(s|d)user=(-|({email_address}[^@"\s]+@[^@"\s]+)|((({domain}[^\s]+?)[\\]+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)))\s+\w+="""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\sshost=({src_host}[^\s]+)"""
  """\sdhost=({dest_host}[^\s]+)"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}[^\s]+)"""
  """SessionId:\s+({session_id}\d+)"""
  """cn1=({session_id}\d+)"""
]
ParserVersion = "v1.0.0"


}
```