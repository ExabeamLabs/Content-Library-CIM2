#### Parser Content
```Java
{
Name = juniper-jn-str-configuration-modify-success-mgd
Vendor = "Juniper Networks"
Product = "Junos OS"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """ mgd """
  """ UI_COMMIT """
  """ requested """
]
Fields = [
  """<\d+>\d+\s+({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\d(\+|\-)\d\d:\d\d)"""
  """({host}\S+)\s+mgd\s"""
  """\sUser '({user}[\w\.\-\!\#\^\~]{1,40}\$?)' requested '({operation}[^']+)' """
  """({dest_host}\S+)\s+mgd\s"""
]
ParserVersion = "v1.0.0"


}
```