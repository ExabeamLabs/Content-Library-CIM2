#### Parser Content
```Java
{
Name = "microsoft-o365-json-app-login-success-loginsuccess-2"
Conditions = [
""""event-name":"""
""""src-endpoint":"mcas-activities""""
""""activityResult":"""
"""event-name":"login-success"""
]
ParserVersion = "v1.0.0"

o365-file-app-activity.Fields} [
      """exa_json_path=$.PolicyMatchInfo.PolicyName,exa_field_name=policy_name"""
      """exa_json_path=$.FileExtension,exa_field_name=file_ext"""
      """exa_json_path=$.Application,exa_field_name=app"""
      """exa_json_path=$.ObjectId,exa_regex=({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))$"""
      """exa_json_path=$.DeviceName,exa_field_name=src_host"""
      """exa_json_path=$.RemovableMediaDeviceAttributes.Manufacturer,exa_field_name=removable_media_vendor"""
      """exa_json_path=$.RemovableMediaDeviceAttributes.SerialNumber,exa_field_name=removable_media_serial_number"""
      """"PolicyName":\s*"({policy_name}[^"]+)""""
      """"FileExtension":\s*"({file_ext}[^"]+)""""
      """"Application":\s*"({app}[^"]+)""""
      """"ObjectId":\s*"({file_path}({file_dir}[^"]+[\\\/])({file_name}[^"]+?(\.(?!(_|-|\{))({file_ext}[^\\\.\s)"]+))?))""""
      """"DeviceName":\s*"({src_host}[^"]+)""""
      """"Manufacturer":\s*"({removable_media_vendor}[^"]+)""""
      """"SerialNumber":\s*"({removable_media_serial_number}[^"]+)""""
    
}
```