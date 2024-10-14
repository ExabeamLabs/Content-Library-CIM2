#### Parser Content
```Java
{
Name = "skudonet-skudonetwaf-kv-app-activity-success-modsecuritycontenttype"
ParserVersion = "v1.0.0"
Conditions = [
"""Skudonet ModSecurity"""
"""severity"""
"""OWASP_CRS"""
]

Skudonet-app-activity = {
      Vendor = "Skudonet"
      Product = "Skudonet WAF"
      TimeFormat = "EEE MMM dd HH:mm:ss yyyy"
      event_timeFormat = ["MMM dd HH:mm:ss"]
      Fields = [
        """\[uri\s*"({uri_path}[^"]+)"\]"""
        """\[hostname\s*"({host}[\w.-]+)"\]"""
        """\[severity\s*"({alert_severity}[^"]+)"\]"""
        """client:({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))"""
        """\[file\s*"({file_url}[^"]+)"\]"""
        """\[msg\s*"({additional_info}[^"]+)"\]""""
        """REQUEST_METHOD'\s*\(Value:\s*`?({method}[^"'\)]+)"""
        """\[unique_id\s*"({alert_id}[^"]+)"\]"""
        """\[ver\s*"({user_agent}[^"]+)"\]"""
        """TX:content_type'\s*\(Value:\s*`\|({mime}[^"]+)\|'\s*\)"""
        """({event_time}\w+\s\d+\s\d+:\d+:\d+)\s({server}[^"\s]+)\s"""
        """pound:\s*({policy_id}[^",]+),\s*"""
  
}
```