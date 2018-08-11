# Voip24h

## I. Introduce
- Restfull API.
- Method: `POST`
- API Endpoint:
    ```sh
    /api/v1/partner/voip24h
    ```
## II. API
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
}
```
---
### 2. getDate
**Description:**
> Get data using date.

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
}
```
---
### 3. getUserDate
**Description:**
> Get data using user and date.

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
}
```
---
### 4. recordingDownload
**Description:**
> Get recording download link.

**Request sample:**
```json
{
	"requestType": "recordingDownload",
	"partnerSecret": "rdn7mllWMqND7S5DnVz8",
	"data": {
		"recordingFile": "in-84871076868-01256930269-20170712-161807-1499851087.50918.wav"
	}
}
```

**Response sample:**
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": "http://localhost:8000/api/recording/download?host=eyJpdiI6InR4Z2ZidTVkU3V6dGE2WUFhbFJxTmc9PSIsInZhbHVlIjoiZTBadnprRmU5VlVWUys4RGlvVDAycUdmRnZWMWZoaVNnWnZCbzRxUTZ6cz0iLCJtYWMiOiJlNTg2YjBmMmUwYzliNzZjYjVlMjc0M2UyOGIzZDUyNGRhYTIzNTNmZWRkZDMxNmI1NmFjZjg1MWJjZjRiMjMzIn0=&recordingFile=in-84871076868-01256930269-20170712-161807-1499851087.50918.wav"
}
```
---
### 5. recordingListen
**Description:**
> Get recording listen link.

**Request sample:**
```json
{
	"requestType": "recordingListen",
	"partnerSecret": "rdn7mllWMqND7S5DnVz8",
	"data": {
		"recordingFile": "in-84871076868-01256930269-20170712-161807-1499851087.50918.wav"
	}
}
```

**Response sample:**
```json
{
    "respCode": 0,
    "respMsg": "Success",
    "data": "http://localhost:8000/recording/listen?host=eyJpdiI6InFCdVwvNVlRM21hb2NtQnF6UkJmNnZnPT0iLCJ2YWx1ZSI6ImlEdktueHhKXC9OallYTEIrUDl6SUlveUhRR3RDa2ZTbVBQTU1tQUI3VnJZPSIsIm1hYyI6IjQ2Y2RjODgwODM0YzRhYzg0ODQxODVkYWY5NTFhNzllMWI5MmU2NWY5YWU5MGVmOWU5Y2ViYWIzMjZhZWFjZjAifQ==&recordingFile=in-84871076868-01256930269-20170712-161807-1499851087.50918.wav"
}
```
---
