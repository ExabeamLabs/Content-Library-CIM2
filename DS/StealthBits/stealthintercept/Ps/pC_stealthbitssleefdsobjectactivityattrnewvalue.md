#### Parser Content
```Java
{
Name = "stealthbits-s-leef-ds-object-activity-attrnewvalue"
Vendor = "StealthBits"
Product = "StealthIntercept"
TimeFormat = "yyyy-MM-dd HH:mm:ss"
Conditions = [
  """LEEF:1.0|STEALTHbits|"""
  """AttrNewValue="""
  """Success="""
]
Fields = [
  """\d\d:\d\d:\d\d ({host}[\w\-.]+) LEEF"""
  """devTime=({time}\d\d\d\d\-\d\d\-\d\d \d\d:\d\d:\d\d)"""
  """src=({src_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
  """dst=({dest_ip}((([0-9a-fA-F.]{1,4}):{1,2}){7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""
  """cat=({operation_type}.+?)\s+(\w+=|$)"""
  """usrName =(({domain}[^\\]+)\\)?({user}.+?)\s+(\w+=|$)"""
  """AffectedObject=(?:\t|([^\\]+\\)?({object}.+?))\s*(\w+=|$)"""
  """AttrName =(?:\t|({attribute}.+?))\s+(\w+=|$)"""
  """AttrOldValue=(?:\t|({old_attribute}.+?))\s+(\w+=|$)"""
  """AttrNewValue=(?:\t|({new_attribute}.+?))\s+(\w+=|$)"""
  """Success=({result}.+?)\s+(\w+=|$)"""
  """Success=False.+?Reason=({failure_reason}.+?)\s+(\w+=|$)"""
  """DistinguishedName =(.+?({object_dn}(CN|cn)=.+?,({object_ou}(OU|ou).+?(DC|dc)=[\w-]+))|(?:.+?))\s+(\w+=|$)"""
  """DistinguishedName =({object_dn}.+?)\s+(\w+=|$)"""
  """ClassName =({object_class}.+?)\s+OrigServer="""
  """OrigServer=([^\\]+\\)?({dest_host}.+?)\s+(\w+=|$)"""
]
ParserVersion = "v1.0.0"


}
```