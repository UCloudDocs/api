# 创建外网防火墙 - CreateUEcFirewall

## 简介

创建外网防火墙









## 定义

### 公共参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **Action**     | string  | 对应的 API 指令名称，当前 API 为 `CreateUEcFirewall`                        | **Yes** |
| **PublicKey**  | string  | 用户公钥，可从 [控制台](https://console.ucloud.cn/uapi/apikey) 获取                                             | **Yes** |
| **Signature**  | string  | 根据公钥及 API 指令生成的用户签名，参见 [签名算法](api/summary/signature.md)  | **Yes** |

### 请求参数

| 参数名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **ProjectId** | string | 项目ID。不填写为默认项目，子帐号必须填写。 请参考[GetProjectList接口](https://docs.ucloud.cn/api/summary/get_project_list) |No|
| **Name** | string | 防火墙名称 |**Yes**|
| **Rule.N.ProtocolType** | string | 协议，可选值：TCP，UDP，ICMP |**Yes**|
| **Rule.N.Port** | string | 端口，范围用"-"符号分隔，如：1-65535 |**Yes**|
| **Rule.N.SrcIp** | string | 源ip |**Yes**|
| **Rule.N.Action** | string | ACCEPT（接受）和DROP（拒绝） |**Yes**|
| **Rule.N.Priority** | string | 优先级：HIGH（高），MEDIUM（中），LOW（低） |**Yes**|
| **Rule.N.Remark** | string | 备注 |No|
| **Remark** | string | 描述 |No|

### 响应字段

| 字段名 | 类型 | 描述信息 | 必填 |
|:---|:---|:---|:---|
| **RetCode** | int | 返回状态码，为 0 则为成功返回，非 0 为失败 |**Yes**|
| **Action** | string | 操作指令名称 |**Yes**|
| **Message** | string | 返回错误消息，当 `RetCode` 非 0 时提供详细的描述信息 |No|
| **FirewallId** | string | 防火墙Id |**Yes**|




## 示例

### 请求示例
    
```
https://api.ucloud.cn/?Action=CreateUEcFirewall
&ProjectId=IDsbnwJt
&Name=EOshSZsY
&Rule.n.ProtocolType=wGvGHDSl
&Rule.n.Port=fOgszAIP
&Rule.n.SrcIp=HXinRhGr
&Rule.n.Action=YkMZOXpD
&Rule.n.Priority=rXaNQRQR
&Rule.n.Remark=PbSGEwdW
&Remark=bpWwkzZb
```

### 响应示例
    
```json
{
  "Action": "CreateUEcFirewallResponse",
  "FirewallId": "OApnKLSk",
  "RetCode": 0
}
```





