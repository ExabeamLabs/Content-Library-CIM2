#### Parser Content
```Java
{
Name = cisco-ise-cef-endpoint-login-success-authsuccess
Vendor = "Cisco"
Product = "Cisco ISE"
TimeFormat = "epoch"
Conditions = [
  """|CISCO|Cisco Secure ACS|"""
  """|Authentication succeeded|"""
  """ad.Action=Login"""
]
Fields = [
  """\srt=({time}\d+)"""
  """\sdvc=({host}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\sshost=(?:|({src_host}.+?))\s\w+="""
  """\ssrc=(?:|({src_ip}.+?))\s\w+="""
  """\ssuser=(({domain}[^\\]+)\\+)?({user}[^=]+)\s\w+="""
  """\sdst=(?:|({dest_ip}.+?))\s\w+="""
  """AuthenticationMethod=(?:|({auth_method}.+?))\s[\w.]+="""
]
ParserVersion = "v1.0.0"


}
```