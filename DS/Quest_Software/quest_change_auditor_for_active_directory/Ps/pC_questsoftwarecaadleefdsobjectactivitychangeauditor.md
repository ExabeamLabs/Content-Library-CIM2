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
    """ipAddress=({host_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))""",
    """computer=({host}[\w\-.]+)""",
    """dst=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
    """dstPort=({dest_port}\d+)""",
    """event=({event_name}[^\^=]+?)\^""",
    """action=({operation_type}[^\^=]+?)\^""",
    """result=({result}[^\^=]+?)\^""",
    """user=(({domain}[^\\\s\^=]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)\^""",
    """domainFqdn=({domain}[^\s\^]+)""",
    """origin=(({src_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|({src_host}[\w\-.]+))""",
    """originIPv4=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """objectClass=({object_type}[^\^]+)""",
    """objectName =({object_name}[^\^]+)""",
    """objectDn=({ds_object_dn}[^\^]+)""",
    """objectDn=CN=[^\^]+?({ds_object_ou}OU=[^\^]+)""",
    """attributeName =({attribute}[^\^]+)""",
    """adUsnChangedPre=({old_attribute}[^\^]+)""",
    """adUsnChangedPost=({new_attribute}[^\^]+)""",
  ]
  ParserVersion = "v1.0.0"


}
```