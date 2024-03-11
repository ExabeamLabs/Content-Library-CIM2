#### Parser Content
```Java
{
Name = salesforce-sf-sk4-app-activity-success-changedprofileforuserstdtostd
Vendor = Salesforce
Product = Salesforce
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
Conditions = [
  """flexString1=changedprofileforuserstdtostd"""
  """destinationServiceName =Sales Cloud"""
]
Fields = [
  """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d+Z)\s+"""
  """\Wsuser=({email_address}.+?)(\s+\w+=|\s*$)"""
  """\WflexString1=({operation}.+?)(\s+\w+=|\s*$)"""
  """\WflexString2=({additional_info}.+?)(\s+\w+=|\s*$)"""
  """({app}Sales Cloud)"""
  """\Wduser=({object}.+?)(\s+\w+=|\s*$)"""
]
ParserVersion = "v1.0.0"


}
```