#### Parser Content
```Java
{
Name = "delinea-ss-cef-app-login-fail-userloginfail"
Vendor = "Delinea"
Product = "Thycotic Software Secret Server"
TimeFormat = ["MMM dd yyyy HH:mm:ss","epoch_sec"]
Conditions = [
  """|Thycotic Software|Secret Server|"""
  """|USER - LOGINFAILURE|"""
  """ Item Name:"""
]
Fields = [
  """\d{2}:\d{2}:\d{2} ({host}[\w\-.]+) CEF:"""
  """\srt=({time}\w{3}\s\d\d\s\d\d\d\d\s\d\d:\d\d:\d\d)""",
  """\srt=({time}\d{10})"""
  """\sdvc=({host}[^\s]+)"""
  """\sdvchost=({host}[^\s]+)"""
  """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """\sduser=(({domain}[^\\=]+)[\\\/]+)?(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|({user}[\w\.\-]{1,40}\$?))"""
  """Details:\s*({failure_reason}.+?)\s\w+="""
  """Details:\s*({additional_info}({failure_reason}[^:=]+?)(?:\sExpected:[^=]+?)?)\s+\w+=""",
  """({app}Thycotic Software)"""
]
ParserVersion = "v1.0.0"


}
```