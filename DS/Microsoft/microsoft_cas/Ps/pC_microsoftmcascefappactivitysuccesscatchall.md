#### Parser Content
```Java
{
Name = microsoft-mcas-cef-app-activity-success-catchall
  Product = Microsoft CAS
  Conditions = [ """CEF:""", """|MCAS|SIEM_Agent|""", """|EVENT_CATEGORY_"""]
  ParserVersion = "v1.0.0"

Microsoft-CAS-Event-Category= {
  Vendor = Microsoft
  Product = Microsoft CAS
  TimeFormat = "epoch"
  Fields = [
      """\|SIEM_Agent\|[^\|]*\|[^\|]*\|({operation}[^\|]+)\|"""
      """\|SIEM_Agent\|[^\|]*\|({access}[^\|]+)\|"""
      """\Wrt=({time}\d{13})"""
      """\WdestinationServiceName =({app}.+?)\s+(\w+=)"""
      """\Wsuser=({user}[\w\.\-\!\#\^\~]{1,40}\$?)\s+(\w+=)"""
      """\Wsuser=({email_address}[^@\s]+@({email_domain}[^@\s]+))\s+(\w+=)"""
      """\Wmsg=({additional_info}.*?)\s+(\w+=|$)"""
      """\Wfile ({file_url}https?:\/\/[^\/]+({file_dir}\/.*?\/)({file_name}[^\/]+?)\.({file_ext}[^\s\;][\w]+))"""
      """\Wcs3=({object}[^\,]+),"""
      """\WParameters: DLP Policy .*?:\s*({policy_name}[^\,]+)\s*,"""
      """\WSecurity event:\s*({action}[^\s]+)\s"""
      """\Wproperty Action\s({rule_action}\w+)\s(\w+=)"""
      """\WReason:\s*({additional_info}[^;\)]+)"""
      """\Wdvc=(|({host}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}))"""
      """\WrequestClientApplication=(|({user_agent}.*?))\s+(\w+=)"""
      """\Wmsg=\s*({action}[^\s]+)\sa company ({file_type}[^:]+):"""
      """\Wmsg=\s*({action}[^\s]+)\sowner to group: user.+?\sto group\s({group_name}.+?)\ssuser="""
      """\Wmsg=\s*({action}Trash)\s({file_type}[^:]+):"""
    
}
```