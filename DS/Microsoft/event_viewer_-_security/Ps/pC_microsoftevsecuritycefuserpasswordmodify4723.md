#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-password-modify-4723"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|Microsoft Windows|"""
  """An attempt was made to change"""
  """externalId=4723"""
]
Fields = [
  """({event_name}An attempt was made to change an account's password)"""
  """\sexternalId=({event_code}\d+)"""
  """\srt=({time}\d{13})"""
  """\sdvc=({host}[a-fA-F:\d.]+)"""
  """\sdvchost=({host}[\w\-.]+)"""
  """\ssuser=({user}[\w\.\-]{1,40}\$?)\s+\w+="""
  """\sduser=({dest_user}.+?)\s+\w+="""
  """Security_,ID=({user_sid}[^\s]+?)(\s|\||$)"""
  """\ssntdom=({domain}.+?)\s\w+="""
  """\sdeviceSeverity=({result}.+?)\s\w+="""
  """\sdntdom=({dest_domain}.+?)\s\w+="""
  """\sduid=({login_id}[^\s]+)"""
  """\sdvc=(?:-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?)\s+\w+="""
]
ParserVersion = "v1.0.0"


}
```