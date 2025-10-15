#### Parser Content
```Java
{
Name = "darktrace-darktrace-json-alert-trigger-success-suspiciousproperties"
  Product = "Darktrace"
  Vendor = "Darktrace"
  TimeFormat = "epoch"
  Conditions = [ """"title":""", """"summary":""", """"Suspicious properties"""", """"key":""" ]
  Fields = [
    """"title":\s*"({alert_name}[^"]+)"""
    """"createdAt":\s*({time}\d{13})"""  
    """"id":\s*"({alert_id}[^"]+)"""
    """"incidentEventUrl":\s*"({url}[^"]+)"""
    """"summary":\s*"({additional_info}[^"]+)"""
    """"key":\s*"Actor"[^\}]+?"values":\s*\[?"(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@[^\]\s"\\,\|]+\.[^'\]\s"\\,\|]+)|({user}[\w\.\-\!\#\^\~]{1,40}\$?))""""
    """"key":\s*"City"[^\}]+?"values":\s*\[?"({location_city}[^"]+)"""
    """"key":\s*"Country"[^\}]+?"values":\s*\[?"({location_country}[^"]+)"""
    """"key":\s*"Suspicious properties"[^\}]+?"values":\s*\[?({alert_reason}[^\]]+)"""
    """"key":\s*"Source IP"[^\}]+?"ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"key":\s*"Event"[^\}]+?"values":\s*\[?"({alert_type}[^"]+)"""
    """"category":\s*"({alert_severity}[^"]+)"""
  ]
  ParserVersion = "v1.0.0"


}
```