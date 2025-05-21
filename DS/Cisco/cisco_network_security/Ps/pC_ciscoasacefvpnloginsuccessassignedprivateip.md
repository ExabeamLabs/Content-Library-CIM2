#### Parser Content
```Java
{
Name = cisco-asa-cef-vpn-login-success-assignedprivateip
Vendor = "Cisco"
Product = Cisco Network Security
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|CISCO|ASA|"""
  """|Assigned private IP address|"""
  """sourceTranslatedAddress"""
]
Fields = [
  """\srt=({time}\d{13})"""
  """\ssourceTranslatedAddress=({src_translated_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sdvc=({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})"""
  """\sdvchost=({host}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```