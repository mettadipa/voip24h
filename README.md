# Voip24h API Document
### `v1.1`

## Change log:
- `1.0`
 Release date: 14/08/2018
- `1.1`
 Release date: 20/10/2018
    Add getCallData API

## I. Introduce
- Restfull API.
- Method: `POST`
- API Endpoint:
    ```sh
    /api/v1/partner/voip24h
    ```
## II. Voip24h API
### Summary
__Request:__
- `requestType`: Type of request for each API.
- `partnerSecret`: Partner secret Voip24h provide to partner.

__Response:__
- `respCode`: Response code for each request 
    ```sh
     0:  Success
    -1:  Failure
    ```
- `respMsg`: Error description.
- `data`: API data response.
### 1. getUser
**Description:**
> Get data using user.

**Request sample:**
- `user`: User extension.
```json
{
	"requestType": "getUser",
	"partnerSecret": "rdn7mllWMqND7S5DnVdB",
	"data": {
		"user": "137"
	}
}
```

**Response sample:**
- `callId`: ID of call.
- `user`: User extension.
- `phoneNumber`: Phone number.
- `callType`: Type of call (INBOUND/OUTBOUND/EXTERNAL).
- `duration`: Call duration in second.
- `callDate`: Date when the call is executed.
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": [
        {
            "callId": "1532857052.131132",
            "user": "137",
            "phoneNumber": "0982056720",
            "callType": "EXTERNAL",
            "callStatus": "NO ANSWER",
            "duration": 69,
            "callDate": "2018-07-29 16:37:32"
        },
        {
            "callId": "1532834934.130789",
            "user": "137",
            "phoneNumber": "0971828252",
            "callType": "EXTERNAL",
            "callStatus": "NO ANSWER",
            "duration": 0,
            "callDate": "2018-07-29 10:28:54"
        }
    ]
}
```
---
### 2. getDate
**Description:**
> Get data using date.

**Request sample:**
- `fromDate`: From date.
- `toDate`: To date.
```json
{
	"requestType": "getDate",
	"partnerSecret": "rdn7mllWMqND7S5DnVdB",
	"data": {
		"fromDate": "01/01/2018",
		"toDate": "30/07/2018"
	}
}
```

**Response sample:**
- `callId`: ID of call.
- `user`: User extension.
- `phoneNumber`: Phone number.
- `callType`: Type of call (INBOUND/OUTBOUND/EXTERNAL).
- `duration`: Call duration in second.
- `callDate`: Date when the call is executed.
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": [
        {
            "callId": "1532857052.131132",
            "user": "137",
            "phoneNumber": "0982056720",
            "callType": "EXTERNAL",
            "callStatus": "NO ANSWER",
            "duration": 69,
            "callDate": "2018-07-29 16:37:32"
        },
        {
            "callId": "1532834934.130789",
            "user": "137",
            "phoneNumber": "0971828252",
            "callType": "EXTERNAL",
            "callStatus": "NO ANSWER",
            "duration": 0,
            "callDate": "2018-07-29 10:28:54"
        }
    ]
}
```
---
### 3. getUserDate
**Description:**
> Get data using user and date.

**Request sample:**
- `user`: User extension.
- `fromDate`: From date.
- `toDate`: To date.
```json
{
	"requestType": "getUserDate",
	"partnerSecret": "rdn7mllWMqND7S5DnVdB",
	"data": {
		"user": "137",
		"fromDate": "01/01/2018",
		"toDate": "30/07/2018"
	}
}
```

**Response sample:**
- `callId`: ID of call.
- `user`: User extension.
- `phoneNumber`: Phone number.
- `callType`: Type of call (INBOUND/OUTBOUND/EXTERNAL).
- `duration`: Call duration in second.
- `callDate`: Date when the call is executed.
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": [
        {
            "callId": "1532857052.131132",
            "user": "137",
            "phoneNumber": "0982056720",
            "callType": "EXTERNAL",
            "callStatus": "NO ANSWER",
            "duration": 69,
            "callDate": "2018-07-29 16:37:32"
        },
        {
            "callId": "1532834934.130789",
            "user": "137",
            "phoneNumber": "0971828252",
            "callType": "EXTERNAL",
            "callStatus": "NO ANSWER",
            "duration": 0,
            "callDate": "2018-07-29 10:28:54"
        }
    ]
}
```
---
### 4. getCallData
**Description:**
> Get data of specific call.

**Request sample:**
- `uniqueId`: Id of call.
```json
{
	"requestType": "getCallData",
	"partnerSecret": "rdn7mllWMqND7S5DnVdB",
	"data": {
		"uniqueId": "1535642103.21687"
	}
}
```

**Response sample:**
- `callId`: ID of call.
- `user`: User extension.
- `phoneNumber`: Phone number.
- `callType`: Type of call (INBOUND/OUTBOUND/EXTERNAL).
- `duration`: Call duration in second.
- `callDate`: Date when the call is executed.
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": {
        "callId": "1535642103.21687",
        "user": "516",
        "phoneNumber": "0908598361",
        "callType": "OUTBOUND",
        "callStatus": "ANSWERED",
        "duration": 12,
        "callDate": "2018-08-30 22:15:03"
    }
}
```
---
### 5. recordingDownload
**Description:**
> Get recording download link.

**Request sample:**
- `callId`: ID of call.
```json
{
	"requestType": "recordingDownload",
	"partnerSecret": "rdn7mllWMqND7S5DnVdB",
	"data": {
		"callId": "1531709393.4472"
	}
}
```

**Response sample:**
- `link`: Download link.
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": {
        "link": "http://localhost:8000/api/recording/download?host=eyJpdiI6IldickN0R2pjTVwvNDVuU0hqTUhzVkRBPT0iLCJ2YWx1ZSI6IjJPY1JhaVJXdWJHSlFYSlg3ZjQreE5NNFFBcUtrU0lSZTB0XC9HYWJOV0FJPSIsIm1hYyI6IjFiNjFkYjVkNjMxNjI0ZWJkMTA1MDUxYWQ5ZTIzYzM2NGEyNzIyNDVlNTE4YTZjZGQ0YzNiMzJmMTVlODg2OGMifQ==&recordingFile=in-0899199799-0948873483-20180716-094953-1531709393.4472.gsm"
    }
}
```
---
### 6. recordingListen
**Description:**
> Get link to listen recording on the web

**Request sample:**
- `callId`: ID of call.
```json
{
	"requestType": "recordingListen",
	"partnerSecret": "rdn7mllWMqND7S5DnVdB",
	"data": {
		"callId": "1531709393.4472"
	}
}
```

**Response sample:**
- `link`: Listening link.
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": {
        "link": "http://localhost:8000/recording/listen?host=eyJpdiI6IkVLbTdPd3NGU256VXJmdVhkZHlPT3c9PSIsInZhbHVlIjoibzlNUnlJTm1iNWZEK2VOQ2ViRTBVTVRrcWZpZHp3aFA3SVk2MStDM1FOOD0iLCJtYWMiOiIxOGNmZTdhODBlNWQ2ZTRiNzE0MDFhOTE5OTViYzExZDMwOTA5ODA4NDMzMWRjODgxYTYyYjA3MTQ0YTg0ZTRiIn0=&recordingFile=in-0899199799-0948873483-20180716-094953-1531709393.4472.gsm"
    }
}
```
---
### 7. makeDial
**Description:**
> Make call using extension & phone.

**Request sample:**
- `extension`: Extension of Asterisk.
- `phone`: Mobile phone number.
```json
{
	"requestType": "makeDial",
	"partnerSecret": "rdn7mllWMqND7S5DnVdB",
	"data": {
		"extension": "101",
		"phone": "01687506228"
	}
}
```

**Response sample:**
- `extension`: Extension of Asterisk.
- `phone`: Mobile phone number.
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": {
        "extension": "101",
        "phone": "01687506228"
    }
}
```
---
