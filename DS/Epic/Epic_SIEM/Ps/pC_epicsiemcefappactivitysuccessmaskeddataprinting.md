#### Parser Content
```Java
{
Name = epic-siem-cef-app-activity-success-maskeddataprinting
  ParserVersion = "v1.0.0"
  Product = Epic SIEM
  Conditions = [ """CEF:""", """|Epic|Security-SIEM|""", """|MASKED_DATA_PRINTING|""" ]

cef-epic-app-activity = {
  Vendor = Epic
  Product = Epic SIEM
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
    """({host}[\w\-.]+)\s+CEF:"""
  """CEF:([^\|]*\|){5}({operation}[^\|]+)"""
  """workstationID=({dest_host}[\w\-.]+)"""
  """shost=({src_host}[\w\-.]+)"""
  """flag=({additional_info}.+?)\s+(\w+=|$)"""
  """MASKMODE=({result}.+?)\s+(\w+=|$)"""
  """PREVUSER=({user}[^\s,]+)"""
  """NEWUSER=({account}[^\s,]+)"""
  
}
```