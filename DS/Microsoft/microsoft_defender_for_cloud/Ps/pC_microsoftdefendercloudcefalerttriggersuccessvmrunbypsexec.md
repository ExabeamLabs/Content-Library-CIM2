#### Parser Content
```Java
{
Name = microsoft-defendercloud-cef-alert-trigger-success-vmrunbypsexec
  ParserVersion = v1.0.0
  Conditions = [ """"category":""", """"VM_RunByPsExec"""", """"title":""", """"vendor":""", """"Microsoft"""", """"provider":""", """"ASC"""" ]

cef-azure-alert = {
    Vendor = Microsoft
    Product = Microsoft Defender for Cloud
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
    
}
```