#### Parser Content
```Java
{
Name = dell-oim-cef-user-switch-success-retrievepassword
  Vendor = Dell
  Product = One Identity Manager
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""", """|SCB|PAM|""", """|Retrieve Password|""" ]
  Fields = [
    """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)(\s+\w+=|\s*$)""",
    """\sdhost=({dest_host}.+?)(\s+\w+=|\s*$)""",
    """\sduser=({dest_user}.+?)(\s+\w+=|\s*$)""",
    """\sdvc=({host}.+?)(\s+\w+=|\s*$)""",
    """\sdvchost=({host}.+?)(\s+\w+=|\s*$)""",
    """\srt=({time}\d+)""",
  ]
  DupFields = [ "dest_user->account" ]
  ParserVersion = "v1.0.0"


}
```