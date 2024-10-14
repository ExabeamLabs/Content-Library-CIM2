#### Parser Content
```Java
{
Name = "dell-oim-cef-app-activity-success-appactivity"
Vendor = "Dell"
Product = "One Identity Manager"
TimeFormat = "epoch"
Conditions = [
  """CEF:"""
  """|SCB|PAM|"""
]
Fields = [
  """\|SCB\|PAM\|([^\|]*\|){2}({operation}[^\|]+)"""
  """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)"""
  """\sdhost=({dest_host}.+?)(\s+\w+=|\s*$)"""
  """\sOtherInfo:\s*({object}[^\s]+?)(\s+\w+=|\s*$)"""
  """\sduser=({object}.+?)(\s+\w+=|\s*$)"""
  """\sdvc=({host}.+?)(\s+\w+=|\s*$)"""
  """\sdvchost=({host}.+?)(\s+\w+=|\s*$)"""
  """\srt=({time}\d{13})"""
  """\sOtherInfo:\s*({additional_info}.+?)(\s+\w+=|\s*$)"""
  """({app}PAM)"""
]
ParserVersion = "v1.0.0"


}
```