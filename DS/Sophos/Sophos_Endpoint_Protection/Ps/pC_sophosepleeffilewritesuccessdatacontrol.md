#### Parser Content
```Java
{
Name = sophos-ep-leef-file-write-success-datacontrol
  Vendor = Sophos
  Product = Sophos Endpoint Protection
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """LEEF:1.0|Sophos|Enterprise Console|""","""|Data control - Alert only|""", """DestinationValue=removableStorage""" ]
  Fields = [
    """({host}[^\s]+)\s+LEEF:1.0"""
    """devTime=({time}\d{4}-\d{2}-\d{2} \d{2}:\d{2}:\d{2})""",
    """ComputerName =({dest_host}.+?)\s+(\w+=|$)""",
    """LEEF:[^|]*\|Sophos\|Enterprise Console\|[^|]*\|({operation}[^|]*)\|""",
    """usrName =[^\\]*\\({user}.+?)\s+(\w+=|$)""",
    """src=({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})""",
    """domain=({domain}.+?)\s+(\w+=|$)""",
    """FileName =({file_name}.+?)\s+(\w+=|$)""",
    """FileSize=({bytes}\d+)"""
  ]
  ParserVersion = "v1.0.0"


}
```