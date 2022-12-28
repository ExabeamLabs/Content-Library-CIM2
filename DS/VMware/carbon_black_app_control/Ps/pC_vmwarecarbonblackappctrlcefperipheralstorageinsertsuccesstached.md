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
    """(\||\s)dst=(|({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?)(\s+[\w-]+=|\s*$)""",
    """(\||\s)dhost=(|(\S+\\+)?({dest_host}.+?))\s+(\w+=|$)""",
    """(\||\s)dvchost=(|({host}.+?))(\s\w+=|\s*$)""",
    """(\||\s)msg=({operation_details}.+?)\.\s""",
    """(\||\s)msg=Device\s+'({device_id}.+?)'""",
    """(\||\s)msg=Device\s+'({device_id}[^']+?)\s*\([^']+'""",
  ]
  ParserVersion = "v1.0.0"


}
```