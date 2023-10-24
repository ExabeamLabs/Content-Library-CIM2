#### Parser Content
```Java
{
Name = cisco-ise-cef-endpoint-login-fail-loginfailed
Vendor = Cisco
Product = Cisco ISE
TimeFormat = "epoch"
Conditions = [
  """|CISCO|Cisco Secure ACS|"""
  """|Authentication failed|"""
  """ad.Action=Login"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\ssrc=(?:|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s\w+="""
  """\ssuser=(({domain}[^\\]+)\\+)?({user}[\w\.\-]{1,40}\$?)\s\w+="""
  """\sdst=(?:|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)\s\w+="""
  """\sdhost=(?:|({dest_host}.+?))\s\w+="""
  """AuthenticationMethod=(?:|({auth_method}.+?))\s[\w.]+="""
  """FailureReason=(?:|({failure_reason}.+?))\s[\w.]+="""
]
ParserVersion = "v1.0.0"


}
```