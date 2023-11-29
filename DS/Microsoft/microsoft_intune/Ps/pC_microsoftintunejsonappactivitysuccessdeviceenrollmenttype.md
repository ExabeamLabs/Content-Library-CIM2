#### Parser Content
```Java
{
Name = microsoft-intune-json-app-activity-success-deviceenrollmenttype
  Vendor = Microsoft
  Product = Microsoft Intune
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssZ"
  Conditions = [ """"enrolledDateTime":""", """"deviceName":""", """"azureADDeviceId":""", """"azureADRegistered":""", """"deviceEnrollmentType":""" ]
  Fields = [
    """"id":\s*"({device_id}[^"]+)"""",
    """"deviceEnrollmentType":\s*"({operation}[^"]+)"""",
    """"deviceName":\s*"({device_name}[^"]+)"""",
    """"lastSyncDateTime":\s*"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\dZ)""",
    """"emailAddress":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"userPrincipalName":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""",
    """"userDisplayName":\s*"({full_name}[^"]+)"""",
    """"userId":\s*"({user_sid}[^"]+)""""
  ]
  ParserVersion = v1.0.0


}
```