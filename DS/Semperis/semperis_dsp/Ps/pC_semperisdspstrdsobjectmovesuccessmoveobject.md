#### Parser Content
```Java
{
Name = semperis-dsp-str-ds-object-move-success-moveobject
  ParserVersion = v1.0.0
  Vendor = Semperis
  Product = Semperis DSP
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """MoveObject""", """Semperis.DSP""", """[ChangeId]""" ]
  Fields = [
  """OriginatingTime\]\s({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{1,2}\.\d{1,3}Z)"""
  """OriginatingServer\]\s({host}[\w\-.]+)"""
  """ObjectModificationType\]\s({event_name}[^\[]+?)\s+\["""
  """AttributeModificationType\]\s({operation_type}[^\[]+?)\s+\["""
  """ClassName\]\s({ds_object_class}[^\s]+)"""
  """DistinguishedName\]\s({ds_object_dn}[^\[]+?)\s+\["""
  """AttributeName\]\s({attribute}[^\s]+)"""
  """StringValueFrom\]\s({old_attribute}[^\s]+)"""
  """StringValueTo\]\s({new_attribute}[^"]+?)\s*("|$)"""
  """({app}Semperis.DSP)"""
  ]


}
```