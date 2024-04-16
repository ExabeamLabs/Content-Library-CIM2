#### Parser Content
```Java
{
Name = pan-prismaaccess-leef-network-traffic-success-end
  Vendor = Palo Alto Networks
  Product = Prisma Access
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSS"
  Conditions = [ """cat=TRAFFIC""", """Palo Alto Networks""", """srcPort""", """dstPort""", """dst=""", """src=""", """proto=""", """Subtype=end""", """_globalprotect""" ]
  Fields = [
    """devTime=({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d)""",
    """({result}deny)""",
    """cat=({category}[^\s]+)""",
    """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """RuleName =({rule}\S+)""",
    """proto=({protocol}[^s]+)\sBytes""",
    """\sBytes=({bytes}\d+)""",
    """usrName =.+(?:\\\\)({user}[\w\.\-]{1,40}\$?)""",
    """\susrName =(|((({domain}[^\s\\]+)\\)?({user}[\w\.\-]{1,40}\$?)))\s""",
    """Application=({app}\S+)""",
    """dstPort=({dest_port}\d+)""",
    """({result}allow)""",
    """SourceDeviceMac=({src_mac}\S+)""",
    """ DestinationDeviceMac=({dest_mac}\S+)""",
    """\sDeviceName =({host}[\w\-\.]+)(?=(?:\s|\||,|;)[\w.-]+=)"""
    """((?:1969-[^,]+?)|({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+[\+-]\d+:\d+))"""
  ]
  ParserVersion = "v1.0.0"


}
```