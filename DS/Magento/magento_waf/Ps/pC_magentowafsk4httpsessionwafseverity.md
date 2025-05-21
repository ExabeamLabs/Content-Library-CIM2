#### Parser Content
```Java
{
Name = magento-waf-sk4-http-session-wafseverity
  Vendor = Magento
  Product = Magento WAF
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ssz"
  Conditions = [ """requestClientApplication=magentoprod""", """"waf_severity":"""" ]
  Fields = [
    """"time_start":"({time}[^"]+)"""",
    """"status":"({http_response_code}\d+)"""",
    """"url":"({url}[^"]+)"""",
    """"protocol":"({protocol}[^"]+)"""",
    """"client_ip":"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?"""",
    """"request":"({request}[^"]+)"""",
# request_referer is removed
# content_type is removed
# cache_status is removed
# geo_city is removed
# geo_region is removed
    """"service_id":"({service_id}[^"]+)"""",
    """"request_id":"({request_id}[^"]+)"""",
# ip_map is removed
# request_x_forwarded_for is removed
# geo_datacenter is removed
# service_version is removed
# geo_country_code is removed
    """"resp_header_size":"({response_size}\d+)"""",
    """"project_id":"({project_id}[^"]+)"""",
    """"messageId":"({message_id}[^"]+)"""",
# req_header_size is removed
# request_user_agent is removed
    """"accountId":"({account_id}[^"]+)"""",
# waf_severity is removed
# geo_datacenter is removed
# origin_host is removed
  ]


}
```