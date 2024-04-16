#### Parser Content
```Java
{
Name = "microsoft-nps-cef-endpoint-login-success-accessrequest"
Vendor = "Microsoft"
Product = "Microsoft Network Policy Server"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Microsoft|Microsoft NPS"""
  """ act=Access-Request"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\sdvc=({host}[a-fA-F\d.:]+)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sdst=({auth_server}[a-fA-F\d.:]+)"""
  """\sdvchost=({host}.+?)(\s+\w+=|\s*$)"""
  """\sshost=({src_host}.+?)(\s+\w+=|\s*$)"""
  """\sdhost=({auth_server}.+?)(\s+\w+=|\s*$)"""
  """\ssourceTranslatedAddress=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """\ssuser=({user}[\w\.\-]{1,40}\$?)(\s+\w+=|\s*$)"""
  """\sdntdom=({domain}.+?)(\s+\w+=|\s*$)"""
  """\sapp=({protocol}.+?)(\s+\w+=|\s*$)"""
  """\ssourceGeoCountryCode=({src_country_code}\w+)"""
]
ParserVersion = "v1.0.0"


}
```