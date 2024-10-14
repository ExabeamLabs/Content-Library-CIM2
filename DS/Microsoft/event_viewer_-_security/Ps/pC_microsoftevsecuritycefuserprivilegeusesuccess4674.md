#### Parser Content
```Java
{
Name = "microsoft-evsecurity-cef-user-privilege-use-success-4674"
Vendor = "Microsoft"
Product = "Event Viewer - Security"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|Microsoft|Microsoft Windows|"""
  """|An operation was attempted on a privileged object"""
]
Fields = [
  """({event_name}An operation was attempted on a privileged object)"""
  """\srt=({time}\d{13})"""
  """\sdeviceSeverity=({result}[^\s]+)"""
  """\sdhost=({host}[\w\-.]+?)(\s+[^\s]+=|\s*$)"""
  """\sexternalId=({event_code}\d+)"""
  """\sduser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+[^\s]+=|\s*$)"""
  """\sdntdom=({domain}.+?)(\s+[^\s]+=|\s*$)"""
  """\sdproc=({process_path}(({process_dir}.+?)({process_name}[^\\\/]+?)))(\s+\S+=|\s*$)"""
  """Object_\,Server=({object_server}.+?)(\s+[^\s]+=|\s*$)"""
  """\sduid=({login_id}[^\s]+)"""
  """Desired_\,Access=({access}[^\d]+?)(\s+[^\s]+=|\s*$)"""
  """\sdpriv=({privileges}.+?)(\s+[^\s]+=|\s*$)"""
]
DupFields = [
  "host->dest_host"
]
ParserVersion = "v1.0.0"


}
```