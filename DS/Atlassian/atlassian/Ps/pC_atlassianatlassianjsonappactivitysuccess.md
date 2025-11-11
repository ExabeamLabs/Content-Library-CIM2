#### Parser Content
```Java
{
Name = "atlassian-atlassian-json-app-activity-success"
  Vendor = "Atlassian"
  Product = "Atlassian"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss.SSSZ"
  ExtractionType = json
  ParserVersion = "v1.0.0"
  Conditions = [ """"type":""", """"events"""", """api.atlassian""", """"action":""" ]
  Fields = [
    """exa_json_path=$..attributes.time,exa_field_name=time"""
    """exa_json_path=$..attributes.action,exa_field_name=action"""
    """exa_json_path=$..attributes.actor.name,exa_field_name=full_name"""
    """exa_json_path=$..attributes.actor.email,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))"""
    """exa_json_path=$..attributes.location.ip,exa_field_name=src_ip"""
    """exa_json_path=$..attributes.location.countryName,exa_field_name=country"""
    """exa_json_path=$..attributes.location.regionName,exa_field_name=region"""
    """exa_json_path=$..attributes.location.city,exa_field_name=city"""
    """exa_json_path=$..message.content,exa_field_name=additional_info"""
    """exa_json_path=$..attributes.context..type,exa_field_name=object_type"""
  ]


}
```