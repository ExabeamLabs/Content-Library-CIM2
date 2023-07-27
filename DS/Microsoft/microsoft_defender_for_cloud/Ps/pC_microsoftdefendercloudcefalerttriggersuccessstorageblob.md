#### Parser Content
```Java
{
Name = microsoft-defendercloud-cef-alert-trigger-success-storageblob
  ParserVersion = v1.0.0
  Conditions = [ """CEF:""", """"category":""", """"Storage.Blob_OpenContainersScanning.FailedAttempt"""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":""", """"ASC"""" ]

cef-azure-alert = {
    Vendor = Microsoft
    Product = Microsoft Defender for Cloud
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSSSSSZ"
    Fields = [
    """"eventDateTime":"({time}\d{4}-\d{1,2}-\d{1,2}T\d{1,2}:\d{1,2}:\d{2}(\.\d{1,7})?Z)"""
    """"title":"({alert_name}[^"]+)""""
    """"userPrincipalName":\s*"([-|\\|<]|({email_address}[^@"]+@[^".]+\.[^"]+)|(({user}[^\s"@]+)(@[^"]+)?))>?""""
    """"severity":"({alert_severity}[^"]+)""""
    """"domainName":"({domain}[^"]+)""""
    """"id":"({alert_id}[^"]+)""""
    """msg=({additional_info}[^=]+?)\s\w+="""
    """"category":"({alert_type}[^"]+)""""
    """"accountName":"({user}[\w\.\-]{1,40}\$?)""""
    
}
```