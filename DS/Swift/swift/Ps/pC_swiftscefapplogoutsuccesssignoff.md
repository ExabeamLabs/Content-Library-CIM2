#### Parser Content
```Java
{
Name = swift-s-cef-app-logout-success-signoff
    Vendor = Swift
    Product = Swift
    TimeFormat = "epoch"
    Conditions = [ """|SWIFT|""", """|Signoff|"""]
    Fields = [
      """\srt=({time}\d{13})""",
      """\Wdvc=({host}[A-Fa-f:\d.]+)""",
      """\Wdvchost=({host}[\w\-.]+)""",
      """suid=({user}[\w\.\-\!\#\^\~]{1,40}\$?)""",
      """({app}SWIFT)""",
      """\Wsrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
      """({operation}Signoff)""",
      """msg=({additional_info}.+?)\s*\.(\s*\w+=|\s*$)""",
      """dtz=({dtz}[^\s]+)"""
    ]
  ParserVersion = "v1.0.0"
  

}
```