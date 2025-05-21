#### Parser Content
```Java
{
Name = cloudfare-waf-sk4-http-request-cloudflareaws
  ParserVersion = v1.0.0
  Vendor = Cloudflare
  Product = Cloudflare WAF
  TimeFormat = "yyyy-MM-dd HH:mm:ss"
  Conditions = [ """requestClientApplication=cloudflareAWS""" ]
  Fields = [
    """"ClientDeviceType":"({device_type}[^"]+)"""
    """"ClientCountry":"({src_country}[^"]+)"""
    """"ClientIP":"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
    """"ClientRequestUserAgent":"({user_agent}[^"]+)"""
    """"ClientRequestURI":"({uri_path}[^"]+)"""
# request_referer is removed
# firewall_matches_action is removed
    """ClientRequestBytes"+:({bytes}\d+)""",
# firewall_matches_rule_id is removed
# firewall_matches_sources is removed
    """"ClientRequestMethod":"({method}[^"]+)""",
    """WAFAction"+:"+({action}[^"]+)""",
# waf_flag is removed
# waf_profile is removed
# waf_rule_id is removed
# waf_rule_msg is removed
    """ClientRequestProtocol"+:"+({protocol}[^"]+)""",
# request_path is removed
# request_host is removed
  ]


}
```