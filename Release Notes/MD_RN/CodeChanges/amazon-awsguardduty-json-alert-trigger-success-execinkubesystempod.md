# Code Changes for amazon-awsguardduty-json-alert-trigger-success-execinkubesystempod (Parser)

| Code Change | Field Name | Before | After |
|-------------|------------|--------|-------|
| edit_regex_field | tags | ['"tags":\[({tags}.+"\})\]\}'] | ['"tags":\s*({tags}[^$]+?)\]', 'exa_regex="tags":\s*({tags}[^$]+?)\]'] |