#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-file-success-4663"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """|Microsoft|Microsoft Windows|"""
  """|Microsoft-Windows-Security-Auditing:4663|"""
]
Fields = [
  """({event_name}An attempt was made to access an object)"""
  """\sexternalId=({event_code}\d+)"""
  """\srt=({time}\d{13})"""
  """\sdntdom=({domain}[^\s]+)"""
  """\sduser=({user}[\w\.\-]{1,40}\$?)\s+\w+="""
  """\sduid=({login_id}[^\s]+)"""
  """\scs1=({access}.+?)\s+\w+="""
  """\sdvc=({host}[a-fA-F:\d.]+)"""
  """\sdvchost=({host}[\w\-.]+)"""
  """\sfname=({file_path}.+?)(?:$|\s*\w+=)"""
  """\sfname=({file_dir}.+?)\\+(?:[^\\=]+?)\s+(?:$|\w+=)"""
  """\sfname=[^=]*\\({file_name}.*?(\.({file_ext}[^\\:\s.]+))?)\s+(?:$|\w+=)"""
  """\scs3=({access_mask}\w+)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```