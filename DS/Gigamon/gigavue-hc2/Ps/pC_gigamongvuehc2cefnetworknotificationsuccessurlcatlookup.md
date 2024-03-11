#### Parser Content
```Java
{
Name = gigamon-gvuehc2-cef-network-notification-success-urlcatlookup
  Conditions = [ """CEF:""", """|Gigamon|HC2_REF|""", """|URLCAT_LOOKUP|""" ]
  Fields = ${DLGigamonParsersTemplates.gigamon-system-info.Fields} [
    """ cs1=({host}[\w.-]+)\s"""
  ]
  ParserVersion = "v1.0.0"

gigamon-system-info = {
    Vendor = Gigamon
    Product = GigaVUE-HC2
    TimeFormat = "MMM dd HH:mm:ss yyyy"
    Fields = [
      """:\d\d:\d\d \d\d\d\d\s({host}[\w.-]+)""",
      """\s({time}\w{3} \d\d \d\d:\d\d:\d\d \d\d\d\d)\s""",
      """\|Gigamon\|HC2_REF\|([^\|]+\|){2}({operation}[^\|]+)""",
      """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))\s""",
      """\sdst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))\s""",
      """\sspt=({src_port}\d+)""",
      """\sdpt=({dest_port}\d+)""",
      """\sdhost=({dest_host}[^\s]+)""",
      """\svlan=({response}[^\s]+)""",
      """\sproto=({protocol}[^=]+?)\s+(\w+=|$)""",
      """\scs2=({categories}[^="]+?)"?\s+(\w+=|$)"""
    ]
    DupFields = [ "operation->event_name" 
}
```