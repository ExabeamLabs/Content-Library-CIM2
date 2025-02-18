#### Parser Content
```Java
{
Name = netskope-webtx-json-network-traffic-ipsecnetworksecurity
    Vendor = Netskope
    Product = Netskope Webtx
    ParserVersion = "v1.0.0"
    ExtractionType = json
    TimeFormat = "epoch_sec"
    Conditions = [ """"x-type": "http_transaction"""" , """"cs-bytes":""" , """"cs-host":""", """"x-request-id":""", """"x-cs-access-method":""" ]
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
        """exa_json_path=$.cs-uri-query,exa_field_name=uri_query"""
        """exa_json_path=$.x-type,exa_field_name=connection_type"""
        """exa_json_path=$.x-cs-traffic-type,exa_field_name=traffic_type"""
        """exa_json_path=$.cs-referer,exa_field_name=referrer"""
        """"cs-method":\s*"({method}[^"]+)""""
        """"cs-uri-scheme":\s*"({protocol}[^"]+)""""
        """"sc-status":\s*"({http_response_code}\d+)""""
        """"cs-bytes":\s*"({bytes_in}\d+)""""
        """"sc-bytes":\s*"({bytes_out}\d+)""""
        """"bytes":\s*"({bytes}\d+)""""
        """"c-ip":\s*"({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""""
        """"s-ip":\s*"({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){1,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({dest_port}\d+))?""""
        """"cs-username":\s*"({email_address}([A-Za-z0-9]+[!#$%&'+\/=?^_`~.\-])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,;\|]+\.[^\]\s"\\,;\|]+))""""
        """"cs-user-agent":\s*"({user_agent}[^"]+)""""
        """"sc-content-type":\s*"({mime}[^"]+)""""
        """"cs-host":\s*"(-|({web_domain}[a-zA-z0-9.\-_]+(\.[a-zA-Z]{2,})?))\s*("|\||$|\t|\s+[\w\-\(\)]+=)""""
        """"cs-uri":\s*"({uri}[^"]+)""""
        """"x-cs-session-id":\s*"({session_id}[^"]+)""""
        """"x-c-country":\s*"({location_country}[^"]+)""""
        """"x-c-location":\s*"({location_city}[^"]+)""""
        """"x-c-region":\s*"({location_state}[^"]+)""""
        """"x-cs-app":\s*"({app}[^"]+)""""
        """"x-c-browser":\s*"({browser}[^"]+)""""
        """"x-c-os":\s*"({os}[^"]+)""""
        """"x-category":\s*"({category}[^"]+)""""
        """"x-cs-timestamp":\s*"({time}\d{10})""""
        """"cs-uri-query":\s*"({uri_query}[^"]+)""""
        """"x-type":\s*"({connection_type}[^"]+)""""
        """"x-cs-traffic-type":\s*"({traffic_type}[^"]+)""""
        """"cs-referer":\s*"({referrer}[^"]+)""""
    ]


}
```