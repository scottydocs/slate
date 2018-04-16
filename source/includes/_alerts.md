# Alerts

## addAlertCustomInfo

A POST request to add and merge custom information for a specified alert.

```shell
curl -X POST -u graze:graze -k -v "https://<server>/v1/addAlertCustomInfo" -H "Content-Type: application/json; charset=UTF-8" -d '{"alert_id" : 9, "custom_info" : { "field1" : "value2" , "field2" : "value2" , "field3" : ["item1","item2","item3"] , "field4" : {"field4-1" : "value4-1","field4-2" : "value4-2"} }}'
```
**Test it out:**

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/a5bd1ed9834c3ed28cdb)

This endpoint returns an HTTP status code. See [HTTP Status Codes](#HTTP)

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
auth_code | String | Valid auth_token returned from the authenticate request.
alert_id | Number | Valid alert ID, an internal identifier generated by AIOps.
custom_info | JSON | A JSON Object containing the custom information.

## addAlertToSituation

A POST request that adds a specified alert to a specified Situation.

```shell
curl -X POST -u graze:graze -k -v "https://<server>/graze/v1/addAlertToSituation" -H "Content-Type: application/json; charset=UTF-8" -d '{"alert_id" : 16, "sitn_id" : 7 }'
```
**Test it out:**

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/a5bd1ed9834c3ed28cdb)

This endpoint returns an HTTP status code. See [HTTP Status Codes](#HTTP)

### Query Parameters

Parameter | Type | Description
--------- | ------- | -----------
auth_code | String | Valid auth_token returned from the authenticate request.
alert_id | Number | Valid alert ID, an internal identifier generated by AIOps.
sitn_id | Number | Valid Situation ID, an internal identifier generated by AIOps.

## assignAndAcknowledgeAlert

A POST request that assigns and acknowledges the moderator tot he Alert for a specified alert ID and user ID.

```shell
curl -X POST -u graze:graze -k -v "https://<server>/graze/v1/assignAndAcknowledgeAlert" -H "Content-Type: application/json; charset=UTF-8" -d '{"alert_id" : 7, "username" : "network1" }'
```
**Test it out:**

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/a5bd1ed9834c3ed28cdb)

This endpoint returns an HTTP status code. See [HTTP Status Codes](#HTTP)

### URL Parameters

Parameter | Description
--------- | -----------
auth_code | String | Valid auth_token returned from the authenticate request.
alert_id | Number | Valid alert ID, an internal identifier generated by AIOps.
user_id | Number | Valid user ID, an internal identifier generated by AIOps.
username | String | Valid username of a user account in AIOps.