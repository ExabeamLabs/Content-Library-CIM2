#### Parser Content
```Java
{
Name = "code42-incydr-sk4-printer-activity-success-printed"
  Vendor = "Code42"
  Product = "Code42 Incydr"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = [
    """"fileCategoryByExtension""""
    """"eventType":"PRINTED""""
    """"osHostName"""
  ]
  Fields = [
    """\"eventTimestamp\"+:\s*\"+({time}\d+-\d+-\d+T\d+:\d+:\d+)"""
    """\"eventType\"+:\s*\"+({event_code}[^\"]+)"""
    """\"source\":\"+({log_source}[^\"]+)\""""
    """\"userUid\"+:\s*\"+({user_uid}[^\"]+)\""""
    """\"deviceUid\"+:\s*\"+({device_id}[^\"]+)\""""
    """\"processOwner\"+:\s*\"+({user}[\w\.\-\!\#\^\~]{1,40}\$?)\""""
    """\"deviceUserName\"+:\s*\"+({email_address}[^@\"]+@[^\"]+)\""""
    """\"osHostName\"+:\s*\"+({dest_host}[^\"]+)\""""
    """\"actor\"+:\"+(({email_address}[^\"@]+@[^\"@]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """\"publicIpAddress\":\"+({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?\""""
    """\"privateIpAddresses\":\[*"+({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
    """\"printerName\":\"+({printer_name}[^\"]+)\""""
    """\"printJobName\":\"+\s*({object}[^\"]+)\""""
  ]
  DupFields = [
    "dest_host->device_name"
    "event_code->operation"
  ]
  ParserVersion = "v1.0.0"


}
```