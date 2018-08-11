# Voip24h API
## 1. getUser
### Description:
Get data using user.

**Request sample:**
```json
{
	"requestType": "getUser",
	"partnerSecret": "rdn7mllWMqND7S5DnVz8",
	"data": {
		"user": "137"
	}
}
```

**Response sample:**
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": [
        [
            {
                "callId": "1532857052.131132",
                "user": "137",
                "phoneNumber": "0982056720",
                "callType": "EXTERNAL",
                "callStatus": "NO ANSWER",
                "callDate": "2018-07-29 16:37:32"
            },
            {
                "callId": "1532834934.130789",
                "user": "137",
                "phoneNumber": "0971828252",
                "callType": "EXTERNAL",
                "callStatus": "NO ANSWER",
                "callDate": "2018-07-29 10:28:54"
            }
        ]
    ]
}
```
---
## 2. getDate
### Description:
Get data using date.

**Request sample:**
```json
{
	"requestType": "getDate",
	"partnerSecret": "rdn7mllWMqND7S5DnVz8",
	"data": {
		"user": "137",
		"fromDate": "01/01/2018",
		"toDate": "30/07/2018"
	}
}
```

**Response sample:**
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": [
        [
            {
                "callId": "1532857052.131132",
                "user": "137",
                "phoneNumber": "0982056720",
                "callType": "EXTERNAL",
                "callStatus": "NO ANSWER",
                "callDate": "2018-07-29 16:37:32"
            },
            {
                "callId": "1532834934.130789",
                "user": "137",
                "phoneNumber": "0971828252",
                "callType": "EXTERNAL",
                "callStatus": "NO ANSWER",
                "callDate": "2018-07-29 10:28:54"
            }
        ]
    ]
}
```
---
## 3. getUserDate
### Description:
Get data using user and date.

**Request sample:**
```json
{
	"requestType": "getUserDate",
	"partnerSecret": "rdn7mllWMqND7S5DnVz8",
	"data": {
		"user": "137",
		"fromDate": "01/01/2018",
		"toDate": "30/07/2018"
	}
}
```

**Response sample:**
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": [
        [
            {
                "callId": "1532857052.131132",
                "user": "137",
                "phoneNumber": "0982056720",
                "callType": "EXTERNAL",
                "callStatus": "NO ANSWER",
                "callDate": "2018-07-29 16:37:32"
            },
            {
                "callId": "1532834934.130789",
                "user": "137",
                "phoneNumber": "0971828252",
                "callType": "EXTERNAL",
                "callStatus": "NO ANSWER",
                "callDate": "2018-07-29 10:28:54"
            }
        ]
    ]
}
```
---
