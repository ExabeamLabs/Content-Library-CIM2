#### Parser Content
```Java
{
Name = netskope-sc-json-configuration-modify-success-configuration-1
  ParserVersion = v1.0.0
  Product = Netskope Security Cloud
  Conditions = [ """"audit_log_event":"Exception Configuration"""" , """"type":"""" ,""""sAMAccountName":""""]

json-netskope-activity = {
  Vendor = Netskope
  Product = Netskope Security Cloud
  TimeFormat = "epoch_sec"
  ExtractionType = json
  Fields = [
    """exa_json_path=$.timestamp,exa_field_name=time"""
    """exa_json_path=$.user,exa_regex=(({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))"""
    """exa_json_path=$.supporting_data.data_values,exa_field_name=additional_info"""
  
}
```