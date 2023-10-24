#### Parser Content
```Java
{
Name = "varonis-dsp-leef-file-success-datadvantage"
Vendor = "Varonis"
Product = "Varonis Data Security Platform"
TimeFormat = "MM/dd/yyyy hh:mm:ss a"
Conditions = [
  """LEEF:"""
  """|Varonis|DatAdvantage|"""
]
Fields = [
  """devTime=({time}\d+/\d+/\d+ \d+:\d+:\d+ (am|AM|pm|PM))"""
  """accountName =({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
  """domain=(|({domain}.+?))\s+(\w+=|$)"""
  """src=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?\s+(\w+=|$)"""
  """Event_Type=({access}.+?)\s+(\w+=|$)"""
  """Event_Status=({result}.+?)\s+(\w+=|$)"""
  """Affected_Object=(|({file_path}(({file_dir}[^=]+?)\\+)?({file_name}[^\\]+?(\.({file_ext}[^\.\s]+))?)))\s+(\w+=|$)"""
  """Affected_Object_Path=(|({file_path}.+?))\s+(\w+=|$)"""
  """Affected_Object_Path=({file_dir}.+?)\\[^\\]+?\s+(\w+=|$)"""
  """cat=({category}[^=]+?)\s+(\w+=|$)"""
  """DatAdvantage\|[^\\]+?\|({alert_name}[^\\]+?)\|"""
  """Device_Name =({src_host}[\w\-.]+?)\s+(\w+=|$)"""
  """accountName =({user}[\w\.\-]{1,40}\$?)\s+(\w+=|$)"""
  """usrName =(({domain}[^\\]+)\\)?(({user}[\w\.\-]{1,40}\$?)|({full_name}[^"=]+?))\s+(\w+=|$)"""
]
DupFields = [
  "access->event_code",
  "alert_name->additional_info"
]
ParserVersion = "v1.0.0"


}
```