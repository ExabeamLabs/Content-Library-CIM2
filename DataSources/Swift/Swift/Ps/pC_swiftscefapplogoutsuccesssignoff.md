#### Parser Content
```Java
{
Name = swift-s-cef-app-logout-success-signoff
    Vendor = Swift
    Product = Swift
    TimeFormat = "epoch"
    Conditions = [ """|SWIFT|""", """|Signoff|"""]
    Fields = [
      """rt=({time}\d+)""",
      """\Wdvc=({host}[A-Fa-f:\d.]+)""",
      """\Wdvchost=({host}[\w\-.]+)""",
      """suid=({user}[^\s]+)""",
      """({app}SWIFT)""",
      """\Wsrc=({src_ip}[A-Fa-f:\d.]+)""",
      """({operation}Signoff)""",
      """msg=({additional_info}.+?)\s*\.(\s*\w+=|\s*$)""",
      """dtz=({dtz}[^\s]+)"""
    ]
  ParserVersion = "v1.0.0"
  

}
```