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

  xml-epic-siem = {
    Vendor = Epic
    Product = Epic SIEM
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSZ"
    Fields = [
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s+({host}[\w\-\.]+)\s"""
    """<E1Mid>({operation}[^<]+)<\/E1Mid>"""
    """<EMPid>({user}[\w\.\-\!\#\^\~]{1,40}\$?)\^({full_name}[^\^]+)\^({user_id}[^<]+)?<\/EMPid>"""
    """"IP">\s*<Value>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"SOURCE">\s*<Value>({log_source}[^<\[]+)"""
    """"USERJOB">\s*<Value>[^\^]*\^({resource}[^<]+)<\/Value>"""
    """"ROLE">\s*<Value>({role}[^<]+)<\/Value>"""
    """"DEP">\s*<Value>[^\^]*\^({department}[^<]+)<\/Value>"""
    """"HKUDVCID">\s*<Value>({device_id}[^<]+)<\/Value>"""
    """"HKUOSNAM">\s*<Value>({os}[^<]+)<\/Value>"""
    """"HKUOSVER">\s*<Value>({os_version}[^<]+)<\/Value>"""
    """"LOGIN_LDAP_ID">\s*<Value>({user_id}[^<]+)<\/Value>"""
    """"LOGIN_CLIENT_ID">\s*<Value>({client_id}[^<]+)<\/Value>"""
    """"CLIENT_TYPE">\s*<Value>({client_type}[^<\[]+)"""
    
}
```