#### Parser Content
```Java
{
Name = dell-sonicwallaventail-cef-vpn-logout-success-sessionend
  Vendor = Dell
  Product = SonicWALL Aventail
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM""", """Aventail Session End"""]
  Fields = [
    """\srt=({time}\d+)""",
    """shost=({host}[^\s]+)""",
    """nitroSource_UserID=({user}[^\r\n]+?)(\s+\w+=|\s*$)""",
    """suser=({user}[^\r\n]+?)(\s+\w+=|\s*$)"""
    """deviceTranslatedAddress=({src_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""", 
    """src=({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""", 
  ]
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"


}
```