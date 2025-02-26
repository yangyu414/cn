# editFirewallPackage


## 描述
更改异常检测类型WAF规则包的灵敏度和操作

## 请求方式
PATCH

## 请求地址
https://starshield.jdcloud-api.com/v1/zones/{zone_identifier}/firewall$$waf$$packages/{identifier}

|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**zone_identifier**|String|True| | |
|**identifier**|String|True| | |

## 请求参数
|名称|类型|是否必需|默认值|描述|
|---|---|---|---|---|
|**sensitivity**|String|False|high|防火墙包的敏感度。|
|**action_mode**|String|False|challenge|将对防火墙包下的规则执行的默认操作。|


## 返回参数
|名称|类型|描述|
|---|---|---|
|**result**|[Result](editFirewallPackage#result)| |
|**requestId**|String| |

### <div id="result">Result</div>
|名称|类型|描述|
|---|---|---|
|**data**|[WAFRulePackage](editFirewallPackage#wafrulepackage)| |
### <div id="wafrulepackage">WAFRulePackage</div>
|名称|类型|描述|
|---|---|---|
|**id**|String|WAF包标识符标签|
|**name**|String|防火墙包的名称|
|**description**|String|防火墙包的目的/功能摘要|
|**detection_mode**|String| |
|**zone_id**|String|区标识符标签|
|**status**|String|指示对域应用防火墙包。|
|**sensitivity**|String|防火墙包的敏感度。|
|**action_mode**|String|将对防火墙包下的规则执行的默认操作。|

## 返回码
|返回码|描述|
|---|---|
|**200**|request successful|
