#### Parser Content
```Java
{
Name = unix-unix-cef-user-switch-success-executecommand
    Vendor = Unix
    Product = Unix
    ParserVersion = "v1.0.0"
    TimeFormat = "epoch"
    Conditions = [ """CEF:""", """|Unix|Unix|""", """|User Executed Command|""", """ deviceProcessName =sudo """ ]
    Fields = [
      """\srt=({time}\d{13})""",
      """\sdvc=({host}\S+)(\s+\w+=|\s*$)""",
      """\sdvchost=({host}\S+)(\s+\w+=|\s*$)""",
      """\sdhost=({dest_host}\S+)(\s+\w+=|\s*$)""",
      """\sdst=({dest_ip}\S+)(\s+\w+=|\s*$)""",
      """\ssuser=(|({user}[\w\.\-]{1,40}\$?))(\s+\w+=|\s*$)""",
      """\ssuid=(|({user_uid}.+?))(\s+\w+=|\s*$)""",
      """\sfname=((/usr)?/bin/)?su(\s+((-\w*[csgG]\s+("([^"\\]|\\\\|\\")+"|'.+?'|\S+))|-\w+|--(session-command|command|group|supp-group|shell)\s+("([^"\\]|\\\\|\\")+"|'.+?'|\S+)|--\w+|-))*\s+(?!-+)["']?({dest_user}[\w\.\-]{1,40}\$?)["']?(\s+\w+=|\s*$)""",
      """\sduser=(|({account}.+?))(\s+\w+=|\s*$)""",
      """({event_code}sudo)"""
    ]
  

}
```