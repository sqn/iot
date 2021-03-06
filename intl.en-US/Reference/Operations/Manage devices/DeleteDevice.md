# DeleteDevice {#reference_jn4_3qz_wdb .reference}

You can call this operation to delete a specified device.

## Descriptions {#section_psk_rdm_xdb .section}

If a device is no longer needed, you can delete the device. After the device is deleted, the device ID  \(IotId\) will be invalid, and any information associated with the device will be deleted. You will no longer be able to perform any action on the device.

## Request parameters {#section_ac2_xdm_xdb .section}

|Name|Type|Required|Description|
|:---|:---|:-------|:----------|
|Action|String|Yes|The operation that you want to perform. Set the value to DeleteDevice.|
|IotId|String|No| The device ID that you want to delete.

 **Note:** If you set this parameter, you do not need to set ProductKey and DeviceName parameters. IotId, as the unique identifier of the device, corresponds to the combination of ProductKey & DeviceName. If you set both the IotId and the ProductKey&DeviceName, the IotId takes priority.

 |
|ProductKey|String|No| The identifier of the product that the devices belongs to.

 **Note:** If you set this parameter, you must also set the parameter DeviceName.

 |
|DeviceName|String|No| The name of the device that you want to delete.

 **Note:** If you set this parameter, you must also set the parameter ProductKey.

 |

## Response parameters {#section_cqf_l2m_xdb .section}

|Name|Type|Description|
|:---|:---|:----------|
|RequestId|String|The GUID generated by Alibaba Cloud for the request.|
|Success|Boolean|Indicate whether the call is successful. A value of true indicates that the call is successful. A value of false indicates that the call has failed.|
|ErrorMessage|String|The error messages returned when the call fails.|

## Examples {#section_add_t2m_xdb .section}

**Request example**

```
https://iot.cn-shanghai.aliyuncs.com/?Action=DeleteDevice
 &IotId=MpEKNuEUJzIORNANAWJX0010929900*****
 & <common request parameters>
```

**Response example**

-   JSON format

    ```
    {
      "RequestId":"57b144cf-09fc-4916-a272-a62902d5b207",
      "Success": true
    }
    ```

-   XML format

    ```
    <? xml version="1.0" encoding="UTF-8"? >
     <DeleteDeviceResponse>
          <RequestId>57b144cf-09fc-4916-a272-a62902d5b207</RequestId>
          <Success>true</Success>
      </DeleteDeviceResponse>
    ```


