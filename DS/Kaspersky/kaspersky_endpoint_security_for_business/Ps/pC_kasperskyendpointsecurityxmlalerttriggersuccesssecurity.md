#### Parser Content
```Java
{
Name = kaspersky-endpointsecurity-xml-alert-trigger-success-security
  Vendor = Kaspersky
  Product = Kaspersky Endpoint Security for Business
  ParserVersion = "v1.0.0"
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Conditions = [ """Kaspersky Endpoint Security 10 for Windows""" ]
  Fields = [
    """Result:\s+({result}[^:]+)""",
    """<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){5}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(({file_dir}[^\<]+?)\\+)?({file_name}[^\<\\]+?(\.({file_ext}[^\<\.\s]+)))<\/Data><\/Cell>""",
    """<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){8}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(({domain}[^\<]+)\\+)?({user}[\w\.\-\!\#\^\~]{1,40}\$?)<\/Data><\/Cell>""",
    """<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){1}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>({group_name}[^\<]+?)<\/Data><\/Cell>""",
    """<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){2}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>({src_host}[^\<]+?)<\/Data><\/Cell>""",
    """<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){3}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>({alert_name}[^\<]+?)<\/Data><\/Cell>""",
    """<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){4}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>({time}[^\<]+?)<\/Data><\/Cell>""",
    """<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){5}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>({file_path}[^\<]+?)<\/Data><\/Cell>""",
    """<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){6}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>({threat_category}[^\<]+?)<\/Data><\/Cell>""",
    """<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){13}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4}))(:({src_port}\d+))?<\/Data><\/Cell>""",
    """<Row>(<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>(<\/Cell>|[^\<]+?<\/Data><\/Cell>)){15}<Cell ss:StyleID="TableData"><Data ss:Type=[^\<]+?>({domain}[^\<]+?)<\/Data><\/Cell>""",
  ]
  DupFields=[ "alert_name->alert_type" ]


}
```