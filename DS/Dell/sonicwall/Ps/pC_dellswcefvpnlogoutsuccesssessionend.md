#### Parser Content
```Java
{
Name = dell-sw-cef-vpn-logout-success-sessionend
  Vendor = Dell
  Product = Sonicwall
  TimeFormat = "epoch"
  Conditions = [ """|McAfee|ESM""", """Aventail Session End"""]
  Fields = [
    """\srt=({time}\d{13})""",
    """shost=({host}[^\s]+)""",
    """nitroSource_UserID=({user}[^\r\n]+?)(\s+\w+=|\s*$)""",
    """suser=({user}[^\r\n]+?)(\s+\w+=|\s*$)"""
    """deviceTranslatedAddress=({src_translated_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})""", 
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""", 
  ]
  DupFields = ["user->account"]
  ParserVersion = "v1.0.0"


}
```