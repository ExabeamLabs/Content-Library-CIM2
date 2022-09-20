#### Parser Content
```Java
{
Name = dell-oim-cef-user-switch-success-retrievepassword
  Vendor = Dell
  Product = One Identity Manager
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|SCB|PAM|""", """|Retrieve Password|""" ]
  Fields = [
    """\ssuser=({user}.+?)(\s+\w+=|\s*$)""",
    """\sdhost=({dest_host}.+?)(\s+\w+=|\s*$)""",
    """\sduser=({dest_user}.+?)(\s+\w+=|\s*$)""",
    """\sdvc=({host}.+?)(\s+\w+=|\s*$)""",
    """\sdvchost=({host}.+?)(\s+\w+=|\s*$)""",
    """\srt=({time}\d+)""",
  ]
  DupFields = [ "account->dest_user" ]
  ParserVersion = "v1.0.0"


}
```