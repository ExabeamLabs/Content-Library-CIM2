#### Parser Content
```Java
{
Name = vmware-airwatch-kv-alert-trigger-success-airwatch
  ParserVersion = v1.0.0
  Product = Vmware AirWatch
  Conditions = [ """AirWatch""", """Event Category:"""", """Event:"""" ]

airwatch-auth-activity = {
    Vendor = VMware
    TimeFormat = "MMMM dd, yyyy HH:mm:ss"
    Fields = [
      """Event Timestamp:\s*({time}\w+\s*\d\d,\s*\d\d\d\d\s*\d\d:\d\d:\d\d)""",
      """\s({host}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3})\s*\[mdmAirwatch""",
      """Event Category:"+({event_name}[^"]+)"""",
      """EnrollmentUser:"+(N\/A|({user}[^"]+))"""",
      """Event:"+({result}[^"]+)"""",
      """Event Data:"+({additional_info}[^"]+)"""",
      """DeviceFriendlyName:"+((N\/A)|(DELETE IN PROGRESS...)|({device_name}[^"]+))"""",
      """Reason=({failure_reason}[^"]+)"""",
    ]
     DupFields = ["device_name->src_host"
}
```