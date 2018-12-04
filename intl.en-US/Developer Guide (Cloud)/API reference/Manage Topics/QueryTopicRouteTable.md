# QueryTopicRouteTable {#reference_n4w_fjd_xdb .reference}

Call this operation to query the target topics that subscribe to a specified source topic. This process is known as querying the route table for the specified source topic. The operation is only used to query user topics.

## Request Parameters {#section_atq_ln5_xdb .section}

|Parameter|Type|Required|Description|
|:--------|:---|:-------|:----------|
|Action|String|Yes|The operation that you want to perform. Set the value to QueryTopicRouteTable.|
|Topic|String|Yes|The source topic, which publishes messages.|
|Common Request Parameters|-|Yes|See [Common parameters](intl.en-US/Developer Guide (Cloud)/API reference/Common parameters.md#).|

## Response parameters {#section_rsm_sn5_xdb .section}

|Parameter|Type|Description|
|:--------|:---|:----------|
|RequestId|String|The globally unique ID generated by Alibaba Cloud for the request.|
|Success|Boolean|Indicates whether the call is successful. A value of true indicates that the call is successful. A value of false indicates that the call has failed.|
|ErrorMessage|String|The error message returned when the call fails.|
|Code|String|The error code returned when the call fails. For more information about error codes, see [Error codes](intl.en-US/Developer Guide (Cloud)/API reference/Error codes.md#).|
|DstTopics|List|The list of target topics returned when the call is successful.|

## Examples {#section_y2t_yn5_xdb .section}

**Request example**

```
https://iot.cn-shanghai.aliyuncs.com/?Action=QueryTopicRouteTable
&Topic=%2Fx7aWKW94bb8%2FtestDataToDataHub%2Fupdate
&Public Request Parameters
```

**Response example**

```
{
    "RequestId":"FCC27691-9151-4B93-9622-9C90F30542EC",
    "Success":true,
    "DstTopics":["/CXi4***/device2/get","/CXi4***/device3/get"]
}
```
