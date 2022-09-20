#### Parser Content
```Java
{
Name = questsoftware-caad-leef-ds-object-activity-changeauditor
  Vendor = Quest Software
  Product = Quest Change Auditor for Active Directory
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """LEEF:""", """|Quest Software""" , """|Change Auditor|""" , """action=""" ]
  Fields = [
    """devTime=({time}\w+\s+\d+\s+\d\d\d\d\s+\d\d:\d\d:\d\d)""",
    """ipAddress=({host_ip}[A-Fa-f:\d.]+)""",
    """computer=({host}[\w\-.]+)""",
    """dst=({dest_ip}[A-Fa-f:\d.]+)""",
    """dstPort=({dest_port}\d+)""",
    """event=({event_name}[^\^=]+?)\^""",
    """action=({operation_type}[^\^=]+?)\^""",
    """result=({result}[^\^=]+?)\^""",
    """user=(({domain}[^\\\s\^=]+)\\+)?({user}[^\\\s\^=]+)""",
    """domainFqdn=({domain}[^\s\^]+)""",
    """origin=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-.]+))""",
    """originIPv4=({src_ip}[A-Fa-f:\d.]+)""",
    """objectClass=({object_class}[^\^]+)""",
    """objectName =({object}[^\^]+)""",
    """objectDn=({object_dn}[^\^]+)""",
    """objectDn=CN=[^\^]+?({object_ou}OU=[^\^]+)""",
    """attributeName =({attribute}[^\^]+)""",
    """adUsnChangedPre=({old_attribute}[^\^]+)""",
    """adUsnChangedPost=({new_attribute}[^\^]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```