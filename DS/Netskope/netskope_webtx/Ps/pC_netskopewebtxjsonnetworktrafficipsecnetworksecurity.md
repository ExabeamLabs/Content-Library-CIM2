#### Parser Content
```Java
{
Name = netskope-webtx-json-network-traffic-ipsecnetworksecurity
    Vendor = Netskope
    Product = Netskope Webtx
    ParserVersion = "v1.0.0"
    ExtractionType = json
    TimeFormat = "epoch_sec"
    Conditions = [ """x-cs-access-method""" , """x-cs-traffic-type""" , """x-category""" ]
    Fields = [
        """exa_json_path=$.cs-method,exa_field_name=method""",
        """exa_json_path=$.cs-uri-scheme,exa_field_name=protocol""",
        """exa_json_path=$.sc-status,exa_field_name=http_response_code"""
        """exa_json_path=$.cs-bytes,exa_field_name=bytes_in"""
        """exa_json_path=$.sc-bytes,exa_field_name=bytes_out"""
        """exa_json_path=$.bytes,exa_field_name=bytes"""
        """exa_json_path=$.c-ip,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?"""
        """exa_json_path=$.s-ip,exa_regex=({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""",
        """exa_json_path=$.cs-username,exa_regex=({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))"""
        """exa_json_path=$.cs-user-agent,exa_field_name=user_agent""",
        """exa_json_path=$.sc-content-type,exa_field_name=mime""",
        """exa_json_path=$.cs-host,exa_regex=(-|({web_domain}[a-zA-z0-9.\-_]+(\.[a-zA-Z]{2,})?))\s*("|\||$|\t|\s+[\w\-\(\)]+=)""",
        """exa_json_path=$.cs-uri,exa_field_name=uri""",
        """exa_json_path=$.x-cs-session-id,exa_field_name=session_id"""
        """exa_json_path=$.x-c-country,exa_field_name=location_country"""
        """exa_json_path=$.x-c-location,exa_field_name=location_city"""
        """exa_json_path=$.x-c-region,exa_field_name=location_state"""
        """exa_json_path=$.x-cs-app,exa_field_name=app"""
        """exa_json_path=$.x-c-browser,exa_field_name=browser"""
        """exa_json_path=$.x-c-os,exa_field_name=os"""
        """exa_json_path=$.x-category,exa_field_name=category"""
        """exa_json_path=$.x-cs-timestamp,exa_field_name=time"""
        """exa_json_path=$.bytes,exa_field_name=bytes"""
        """exa_json_path=$.cs-uri-query,exa_field_name=uri_query"""
        """exa_json_path=$.x-type,exa_field_name=connection_type"""
        """exa_json_path=$.x-cs-traffic-type,exa_field_name=traffic_type"""
        """exa_json_path=$.cs-referer,exa_field_name=referrer"""
    ]


}
```