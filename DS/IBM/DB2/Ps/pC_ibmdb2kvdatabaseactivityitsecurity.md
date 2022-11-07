#### Parser Content
```Java
{
Name = ibm-db2-kv-database-activity-itsecurity
  Vendor = IBM
  Product = DB2
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [ """CEF:""", """|Enterprise-IT-Security""", """PCI_DB2 """ ]
  Fields = [
    """\s({time}\d+-\d+-\d+T\d+:\d+:\d+)\S*\s+({host}[\w\-.]+)\s+PCI_DB2""",
    """deviceProcessName =({host}[\w\-.]+)""",
    """act=({operation}.+?)\s+(\w+=|$)""",
    """cat=({category}.+?)\s+(\w+=|$)""",
    """cs2=({result}.+?)\s+(\w+=|$)""",
    """shost=({src_host}[\w\-.]+)\s+(\w+=|$)""",
    """deviceProcessName =({process_name}.+?)\s+(\w+=|$)""",
    """cs1=({additional_info}.+?)\s+(\w+=|$)""",
    """filePath=({file_name}.+?)\s+(\w+=|$)""",
    """duser=({user}.+?)\s*\w+=""",
    """({event_code}DB2_AU06)""",
    """({event_name}DB2Aud006_Privileged_User_Activity)""",
  ]
  ParserVersion = "v1.0.0"


}
```