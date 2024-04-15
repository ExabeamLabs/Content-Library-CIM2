#### Parser Content
```Java
{
Name = "zoom-z-sk4-app-activity-success-operator"
  Vendor = "Zoom"
  Product = "Zoom"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [
    """destinationServiceName =Zoom"""
    """"operation_detail":""""
    """"operator":""""
  ]
  Fields = [
    """\WdestinationServiceName =({app}.+?)(\s+\w+=|\s*$)"""
    """time\":\"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)"""
    """\"operator\":\"({email_address}[^\s@\"]+@[^\s@\"]+)\""""
    """\"operation_detail\"\s*:\s*\"({additional_info}[^\"]+)"""
    """\"action\"\s*:\s*\"({operation}[^\"]+)\""""
    """\"category_type\"\s*:\s*\"({object_type}[^\"]+)\""""
    """\"operation_detail\"\s*:\s*\".*?\s+({object}[^\s@\"]+@[^\s@\"]+)\s+"""
  ]
  ParserVersion = "v1.0.0"


}
```