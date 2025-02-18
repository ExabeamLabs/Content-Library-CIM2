#### Parser Content
```Java
{
Name = microsoft-defendercloud-cef-alert-trigger-success-mcasalert
  ParserVersion = v1.0.0
  Conditions = [ """"category":""", """"MCAS_ALERT_UEBA_INVESTIGATION_PRIORITY_INCREASE"""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":""" ]

cef-azure-alert = {
    Vendor = Microsoft
    Product = Microsoft Defender
    TimeFormat = ["yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ", "yyyy-MM-dd'T'HH:mm:ss.SSSZ"]
    Fields = [
    """"eventDateTime":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{2}(\.\d{1,7})?Z)"""
    """"title":"({alert_name}[^"]+)""""
    """"userPrincipalName":\s*"([-|\\|<]|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)(@[^"]+)?))>?""""
    """"severity":"({alert_severity}[^"]+)""""
    """"domainName":"({domain}[^"]+)""""
    """"id":"({alert_id}[^"]+)""""
    """msg=({additional_info}[^=]+?)\s\w+="""
    """"category":"({alert_type}[^"]+)""""
    """"accountName":"({user}[\w\.\-\!\#\^\~]{1,40}\$?)""""
    """"status":"({incident_status}[^"]+)"""
    
}
```