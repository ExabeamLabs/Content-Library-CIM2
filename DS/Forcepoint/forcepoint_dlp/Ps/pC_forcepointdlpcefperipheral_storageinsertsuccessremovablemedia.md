#### Parser Content
```Java
{
Name = forcepoint-dlp-cef-peripheral_storage-insert-success-removablemedia
  ParserVersion = v1.0.0
  Vendor = Forcepoint
  Product = Forcepoint DLP
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """CEF:""","""|Websense|Data Security""", """sourceServiceName =Endpoint Removable Media""", """act=Permitted""" ]
  Fields = [
    """\ssuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """\sloginName =(({domain}[^\\]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=|$)""",
    """\sfname=(N\/A|({file_path}.*?[\/\\]+[^\\\/]+))\s+\- [\d.]+ """,
    """\sfname=(N\/A|.*?[\/\\]+({file_name}[^\\\/]+))\s+\- [\d.]+ """,
    """\smsg=({operation}.+?)\s+(\w+=|$)""",
    """\scat=({operation_details}.+?)\s+(\w+=|$)""",
    """\sfname=(N\/A|.*?[\/\\]+[^\\\/]+ - ({bytes}[\d.]+)\s+({bytes_unit}[^\s;]+))""",
    """\sduser=(?:|({device_id}.+?))\s+(\w+=|$)""",
    """({device_class}(USB|DVD|Removable Media))"""
  ]


}
```