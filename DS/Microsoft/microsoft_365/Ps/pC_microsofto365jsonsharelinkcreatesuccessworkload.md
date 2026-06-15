#### Parser Content
```Java
{
Name = "microsoft-o365-json-share-link-create-success-workload"
TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
ExtractionType = json
Conditions = [ """"Operation":"""", """LinkCreated"""", """Workload""" ]
ParserVersion = "v1.0.0"

o365-file-share-link = {
    Vendor = Microsoft
    Product = Microsoft 365
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    ExtractionType = json
    Fields = [
    """"(browser|BrowserName)":"({browser}[^"]+)""""
    """"site":"({site_at}[^",]+)"""",
    """"Platform":"({os}[^"]+)""""
    """"ItemType":"({file_type}[^"]+)""""
    """"Operation":"({operation}[^"]+)""""
    """"OrganizationId":"({tenant_id}[^"]+)","""
    """"RecordType":\s*"*({object_type}[^,]+?)"*,""",
    """useragent":"({user_agent}[^"]+)"""
    """"correlationId":"({correlation_id}[^"]+)"""",
    """"AuthenticationType":"({auth_type}[^"]+)"""",
    """"SourceFileName":"({src_file_name}[^,]+)""",
    """"objectId":"({object_id}[^"]+)"""",
    """"SiteUrl":"({site_name}({url}[^"]+))""""
    """"ClientIP":\s*"(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?"""",
    """"SourceFileExtension":"({file_ext}[^"]+)""""
    """"Workload":\s*"({app}[^"]+)"""",
    """"SourceRelativeUrl":\s*"({src_file_path}[^"]+)"""",
    """"UserId":"(({email_address}[^@"]+@[^\.]+\.[^"]+)(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))|({user_sid}[^"]+))"""",
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"TargetUserOrGroupType":"({object_type}[^"]+)""""
    """<Type>({permissions}[^<\s]+?)<"""
    """"Operation":"({share_type}[^"]+?)LinkCreated""""
    """"UserType":"({user_type}[^,}"]+)"*""",
    """"TargetUserOrGroupName":"({target}[^"]+)"""",
    """"TargetUserOrGroupName":"([^@]+)@({target_domain}[^"]*?)"""",
    """"ObjectId\\*"{1,20}:"?[\s\\]*"+(Unknown|Not Available|({object}({mailbox_name}[^"]+)))"""
    """exa_json_path=$.BrowserName,exa_field_name=browser""",
    """exa_json_path=$..Site,exa_field_name=site_at"""
    """exa_json_path=$.Platform,exa_field_name=os"""
    """exa_json_path=$.ItemType,exa_field_name=file_type"""
    """exa_json_path=$.Operation,exa_field_name=operation"""
    """exa_json_path=$.OrganizationId,exa_field_name=tenant_id"""
    """exa_json_path=$.RecordType,exa_field_name=object_type"""
    """exa_json_path=$.UserAgent,exa_field_name=user_agent""",
    """exa_json_path=$.CorrelationId,exa_field_name=correlation_id"""
    """exa_json_path=$.AuthenticationType,exa_field_name=auth_type"""
    """exa_json_path=$.SourceFileName,exa_field_name=src_file_name"""
    """exa_json_path=$..ObjectId,exa_field_name=object_id""",
    """exa_json_path=$.SiteUrl,exa_field_name=site_name"""
    """exa_json_path=$.SiteUrl,exa_regex=({url}\w+:\/+({web_domain}[^"\\\/\s]+)[^"\s]*)"""
    """exa_json_path=$.ClientIP,exa_regex=({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?""",
    """exa_json_path=$.SourceFileExtension,exa_field_name=file_ext"""
    """exa_json_path=$.Workload,exa_field_name=app"""
    """exa_json_path=$.SourceRelativeUrl,exa_field_name=src_file_path"""
    """exa_regex="UserId":"(({email_address}[^@"]+@[^\.]+\.[^"]+)(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))|({user_sid}[^"]+))"""",
    """exa_json_path=$.CreationTime,exa_field_name=time""",
    """exa_json_path=$.TargetUserOrGroupType,exa_field_name=object_type"""
    """exa_regex=<Type>({permissions}[^<\s]+?)<"""
    """exa_regex="Operation":"({share_type}[^"]+?)LinkCreated""""
    """exa_json_path=$.UserType,exa_field_name=user_type""",
    """exa_json_path=$.TargetUserOrGroupName,exa_field_name=target""",
    """exa_json_path=$.TargetUserOrGroupName,exa_regex=([^@]+)@({target_domain}[^"]*?)""",
    """exa_regex="ObjectId\\*"{1,20}:"?[\s\\]*"+(Unknown|Not Available|({object}({mailbox_name}[^"]+)))"""
o365-file-share-link = {
    Vendor = Microsoft
    Product = Microsoft 365
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    ExtractionType = json
    Fields = [
    """"(browser|BrowserName)":"({browser}[^"]+)""""
    """"site":"({site_at}[^",]+)"""",
    """"Platform":"({os}[^"]+)""""
    """"ItemType":"({file_type}[^"]+)""""
    """"Operation":"({operation}[^"]+)""""
    """"OrganizationId":"({tenant_id}[^"]+)","""
    """"RecordType":\s*"*({object_type}[^,]+?)"*,""",
    """useragent":"({user_agent}[^"]+)"""
    """"correlationId":"({correlation_id}[^"]+)"""",
    """"AuthenticationType":"({auth_type}[^"]+)"""",
    """"SourceFileName":"({src_file_name}[^,]+)""",
    """"objectId":"({object_id}[^"]+)"""",
    """"SiteUrl":"({site_name}({url}[^"]+))""""
    """"ClientIP":\s*"(::ffff:)?({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(\%\d+)?(:({src_port}\d+))?"""",
    """"SourceFileExtension":"({file_ext}[^"]+)""""
    """"Workload":\s*"({app}[^"]+)"""",
    """"SourceRelativeUrl":\s*"({src_file_path}[^"]+)"""",
    """"UserId":"(({email_address}[^@"]+@[^\.]+\.[^"]+)(?<!local)|(({user}[\w\.\-\!\#\^\~]{1,40}\$?)@({domain}[^"]+))|({user_sid}[^"]+))"""",
    """"CreationTime":"({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)""",
    """"TargetUserOrGroupType":"({object_type}[^"]+)""""
    """<Type>({permissions}[^<\s]+?)<"""
    """"Operation":"({share_type}[^"]+?)LinkCreated""""
    """"UserType":"({user_type}[^,}
}
```