#### Parser Content
```Java
{
Name = workday-wd-kv-app-activity-success-activityaction
  Vendor = Workday
  Product = Workday
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  Conditions = [ """"taskDisplayName":"""", """"systemAccount":""" , """"activityAction":""""]
  Fields = [
    """"userAgent":"({user_agent}[^"]+)"""
    """"requestTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d\.\d\d\dZ)"""
    """"deviceType":"({device_type}[^"]+)"""
    """"systemAccount":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
    """({app}(W|w)orkday)"""
    """"activityAction":"({additional_info}[^"]+)"""
    """"taskDisplayName":"({operation}[^"]+)"""
    """"ipAddress":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """"sessionId":"({session_id}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```