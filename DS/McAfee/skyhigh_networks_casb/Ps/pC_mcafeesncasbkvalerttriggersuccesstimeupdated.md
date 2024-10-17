#### Parser Content
```Java
{
Name = "mcafee-sncasb-kv-alert-trigger-success-timeupdated"
 Vendor = "McAfee"
 Product = "Skyhigh Networks CASB"
 TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
 Conditions = [
   """anomaly.timeupdated="""
   """,activityName ="""
   """,MimeType="""
 ]
 Fields = [
   """\d+:\d+:\d+\s({host}[^\s]+)\s\w+="""
   """,timestamp=({time}\d\d\d\d\-\d\d\-\d\dT\d+:\d+:\d+)"""
   """\sriskLevel=({alert_severity}[^,]+)"""
   """,userAction=({alert_name}[^,]+)"""
   """,destinationHost=({dest_host}[^,]+)"""
   """,userDisplayName =({user}[\w\.\-\!\#\^\~]{1,40}\$?)"""
   """,ByteCount=({bytes}\d+)"""
   """,MimeType=({additional_info}[^,]+)"""
   """,response=({action}[^,]+)"""
 ]
 DupFields = [
   "alert_name->alert_type"
 ]
 ParserVersion = "v1.0.0"


}
```