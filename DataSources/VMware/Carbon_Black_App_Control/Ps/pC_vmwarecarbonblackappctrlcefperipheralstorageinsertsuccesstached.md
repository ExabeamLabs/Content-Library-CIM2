#### Parser Content
```Java
{
Name = vmware-carbonblackappctrl-cef-peripheral-storage-insert-success-tached
  Vendor = VMware
  Product = Carbon Black App Control
  TimeFormat = "MM dd yyyy HH:mm:ss"
  Conditions = [ """|Bit9|Security Platform|""","""tached|""" ]
  Fields = [
    """({time}\d\d \d\d \d\d\d\d \d\d:\d\d:\d\d)""",
    """\|Bit9\|Security Platform\|(.*?\|){2}({operation}[^\|]+)\|""",
    """(\||\s)dst=(|({dest_ip}.+?))(\s+[\w-]+=|\s*$)""",
    """(\||\s)dhost=(|(\S+\\+)?({dest_host}.+?))\s+(\w+=|$)""",
    """(\||\s)dvchost=(|({host}.+?))(\s\w+=|\s*$)""",
    """(\||\s)msg=({activity_details}.+?)\.\s""",
    """(\||\s)msg=Device\s+'({device_id}.+?)'""",
    """(\||\s)msg=Device\s+'({device_id}[^']+?)\s*\([^']+'""",
  ]
  ParserVersion = "v1.0.0"


}
```