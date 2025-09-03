#### Parser Content
```Java
{
Name = pan-prismaaccess-leef-app-notification-userid
 Conditions = [ """LEEF:""", """|Palo Alto Networks|""", """|Prisma Access|""", """ cat=system""", """SubType=userid""" ]
 ParserVersion = "v1.0.0"
  Fields = ${PaloAltoParsersTemplates.leef-pan-events.Fields}[
    """({app}Prisma Access)""",
    """\|Prisma Access\|[^\|]+\|({event_name}[^\|]+)\|""",
    """VendorSeverity=({severity}[^\s]+)"""
 ]

leef-pan-events = {
  Vendor = "Palo Alto Networks"
  Product = "Prisma Access"
  TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"]
  Fields = [
  	"""\sSubType=({subtype}[^=]+?)\s\w+=""",
    """LogSourceName =({host}[\w\-\.]+)\s\w+="""
    """\sdevTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d{1,7}Z)""",
    """DeviceName =({host}[\w\-\.]+)\s\w+=""",
    """\ssrc=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """\sdst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """\ssrcPostNAT=({src_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\sdstPostNAT=({dest_translated_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """\ssrcPort=({src_port}\d+)""",
    """\sdstPort=({dest_port}\d+)""",
    """\sRule=({rule}[^=]+?)\s\w+=""",
    """usrName =(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+)|(({domain}[^\\\s,]+)\\+)?({user}[\w\.\-]{1,40}\$?))""",
    """URLCategoryList=({category}[^=,]+?)(,[^=]+?)?\s\w+=""",
    """URLCategory=({category}[^=]+?)\s\w+=""",
    """DirectionOfAttack=({direction}[^=]+?)\s\w+=""",
    """\sSessionID=({session_id}\d+)""",
    """\sproto=({protocol}[^\s]+)""",
    """\sAction=({result}[^=]+?)\s\w+=""",
    """\sURL=(\w+:\/\/)?({url}({web_domain}[^\/\s]+)({uri_path}\/[^\s\?]*?)?({uri_query}\?[^\s\/]+)?)""",
    """\sFromZone=({src_network_zone}[^\s]+)""",
    """\sToZone=({dest_network_zone}[^\s]+)""",
    """\sBytes=({bytes}\d+)""",
    """\ssrcBytes=({bytes_out}\d+)""",
    """\sdstBytes=({bytes_in}\d+)""",
    """EventDescription=({additional_info}[^=]+?)\s\w+=""",
    """EventDescription=[^=]+?Reason:\s*({failure_reason}[^=]+?)\s\w+=""",
    """\sInboundInterface=({src_interface}[^=]+?)\s\w+=""",
    """\sOutboundInterface=({dest_interface}[^=]+?)\s\w+=""",
    """\sApplication=(not-applicable|({network_app}[^=]+?))\s\w+="""
  ]
  DupFields = ["result->action"
}
```