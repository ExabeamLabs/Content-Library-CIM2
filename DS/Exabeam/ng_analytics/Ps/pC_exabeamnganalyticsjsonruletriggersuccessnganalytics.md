#### Parser Content
```Java
{
Name = exabeam-nganalytics-json-rule-trigger-success-nganalytics
  Product = NG Analytics
  Conditions = [ """"product":"NG Analytics"""" , """subscription_code""" , """"vendor":"Exabeam"""" ]

exa-events-ns = {
    Vendor = Exabeam
    ParserVersion = v1.0.0
    TimeFormat = "epoch"
    event_from_time_millisFormat = "epoch"
    event_to_time_millisFormat = "epoch"
    ExtractionType = json
    Fields = [
      """exa_json_path=$.approx_log_time,exa_field_name=time"""
       """exa_json_path=$.dest_ip,exa_field_name=dest_ip"""
       """exa_json_path=$.src_host,exa_field_name=src_host"""
       """exa_json_path=$.src_ip,exa_field_name=src_ip"""
       """exa_json_path=$.risk_score,exa_field_name=risk_score"""
       """exa_json_path=$.event_url,exa_field_name=event_url""",
       """exa_json_path=$.rules,exa_field_name=rules""",
       """exa_json_path=$.entities,exa_field_name=entities"""
       """exa_json_path=$.subscription_code,exa_field_name=subscription_code"""
       """exa_json_path=$.event_filter,exa_field_name=event_filter"""
       """exa_json_path=$.event_from_time_millis,exa_field_name=event_from_time_millis"""
       """exa_json_path=$.event_to_time_millis,exa_field_name=event_to_time_millis"""
       """exa_json_path=$.observed_activity,exa_field_name=observed_activity"""
       """exa_json_path=$.previous_id,exa_field_name=previous_id"""
       """exa_json_path=$.rarity_percentile,exa_field_name=rarity_percentile"""
       """exa_json_path=$.rarity_raw_score,exa_field_name=rarity_raw_score"""
       """exa_json_path=$.rarity_score,exa_field_name=rarity_score"""
       """exa_json_path=$.recoverability,exa_field_name=recoverability"""
       """exa_json_path=$.src_product,exa_field_name=src_product"""
       """exa_json_path=$.src_vendor,exa_field_name=src_vendor"""
       """exa_json_path=$.business_criticality,exa_regex=({business_criticality}\d+)"""
       """exa_json_path=$.dest_host,exa_field_name=dest_host"""
       """exa_json_path=$.create_case,exa_field_name=create_case"""
       """exa_json_path=$.id,exa_field_name=id"""
    
}
```