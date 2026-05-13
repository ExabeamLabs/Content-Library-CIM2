#### Parser Content
```Java
{
Name = epic-siem-cef-app-login-success-roverlogin
  ParserVersion = "v1.0.0"
  Product = Epic SIEM
  Conditions = [ """CEF:""", """|Epic|Security-SIEM|""", """|ROVER_LOGIN|""" ]
  Fields = ${EpicParsersTemplates.cef-epic-app-activity.Fields} [
    """suser=([^\^]+)?\^({full_name}[^\^]+)\^({user}[\w\.\-\!\#\^\~]{1,40}\$?)?"""
  ]

cef-epic-app-activity = {
  Vendor = Epic
  Product = Epic SIEM
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Fields = [
  """({host}[\w\-.]+)\s+CEF:"""
  """CEF:([^\|]*\|){5}({operation}[^\|]+)"""
  """workstationID=({dest_host}[\w\-.]+)"""
  """shost=({src_host}[\w\-.]+)"""
  """MASKMODE=({result}.+?)\s+(\w+=|$)"""
  """PREVUSER=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """NEWUSER=({account}[^\s,]+)"""
  """LOGINLDAPID=({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
  """IP=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """USERJOB=(|([^\^]+)?\^({resource}.+?))\s+(\w+=|$)"""
  """ROLE=({role}.+?)(\s+\w+=|\s*$)"""
  ]
 
}
```