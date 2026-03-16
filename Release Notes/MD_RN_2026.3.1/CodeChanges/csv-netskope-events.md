# Code Changes for csv-netskope-events (ParserTemplate)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | app |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){22}(-|({app}[^,]+))'] |
| edit_regex_field | browser |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){7}(-|({browser}[^,]+))'] |
| edit_regex_field | bytes |  | ['^(-,|"([^"]*)",|([^,]*),){0}(-|({bytes}\d+))'] |
| edit_regex_field | category |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){18}(-|({category}[^,]+))'] |
| edit_regex_field | country |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){9}(-|({country}[^,]+))'] |
| edit_regex_field | dest_ip |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){41}(-|({dest_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))'] |
| edit_regex_field | dest_port |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){42}(-|({dest_port}\d+))'] |
| edit_regex_field | device_name |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){10}(-|({device_name}[^,]+))'] |
| edit_regex_field | domain |  | ['^(-,|"([^"]*)",|([^,]*),){4}(-|({domain}[^,]+))'] |
| edit_regex_field | email_address |  | [',(-|(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),(\d\d\d\d-\d\d-\d\d),'] |
| edit_regex_field | email_domain |  | [',(-|(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),(\d\d\d\d-\d\d-\d\d),'] |
| edit_regex_field | host |  | ['^(-,|"([^"]*)",|([^,]*),){5}(-|({host}[^,]+))'] |
| edit_regex_field | http_response_code |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){4}(-|({http_response_code}\d+))'] |
| edit_regex_field | method |  | ['^(-,|"([^"]*)",|([^,]*),){6}(-|({method}[^,]+))'] |
| edit_regex_field | mime |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){3}(-|({mime}[^,]+))'] |
| edit_regex_field | os |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){15}(-|({os}[^,]+))'] |
| edit_regex_field | protocol |  | ['^(-,|"([^"]*)",|([^,]*),){11}(-|({protocol}[^,]+))'] |
| edit_regex_field | referrer |  | ['^(-,|"([^"]*)",|([^,]*),){7}(-|({referrer}[^,]+))'] |
| edit_regex_field | src_ip |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){50}(-|({src_ip}((([0-9a-fA-F.]{0,4}):{1,2}){1,7}([0-9a-fA-F]){0,4})|(((25[0-5]|(2[0-4]|1\d|[0-9]|)\d)\.?\b){4})))'] |
| edit_regex_field | src_port |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){52}(-|({src_port}\d+))'] |
| edit_regex_field | time |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){60}(-|({time}\d{10}))'] |
| edit_regex_field | traffic_type |  | [',(\d\d\d\d-\d\d-\d\d),(-,|"+(.+?)"+,|([^,]*),){61}(-|({traffic_type}[^,]+))'] |
| edit_regex_field | uri |  | ['^(-,|"([^"]*)",|([^,]*),){8}(-|"({uri}[^"]+)",|({=uri}[^,]+),)'] |
| edit_regex_field | user |  | [',(-|(({email_address}([A-Za-z0-9]+[!#$%&\'+-\/=?^_`~])*[A-Za-z0-9]+@({email_domain}[^\]\s"\\,\|]+\.[^\]\s"\\,\|]+))|({user}[\w\.\-\!\#\^\~]{1,40}\$?))),(\d\d\d\d-\d\d-\d\d),'] |
| edit_regex_field | user_agent |  | ['^(-,|"([^"]*)",|([^,]*),){12}(-|"?({user_agent}.+?)"?),([^,]+),(\d\d\d\d-\d\d-\d\d),'] |
| edit_regex_field | web_content_type |  | ['^(-,|"([^"]*)",|([^,]*),){3}(-|"({web_content_type}[^"]+)",|({=web_content_type}[^,]+),)'] |