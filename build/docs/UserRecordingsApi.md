---
title: UserRecordingsApi
---
# platformClient.UserRecordingsApi

All URIs are relative to *https://api.mypurecloud.com*

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
[**deleteUserrecording**](UserRecordingsApi.html#deleteUserrecording) | **DELETE** /api/v2/userrecordings/{recordingId} | Delete a user recording.
[**getUserrecording**](UserRecordingsApi.html#getUserrecording) | **GET** /api/v2/userrecordings/{recordingId} | Get a user recording.
[**getUserrecordingMedia**](UserRecordingsApi.html#getUserrecordingMedia) | **GET** /api/v2/userrecordings/{recordingId}/media | Download a user recording.
[**getUserrecordings**](UserRecordingsApi.html#getUserrecordings) | **GET** /api/v2/userrecordings | Get a list of user recordings.
[**getUserrecordingsSummary**](UserRecordingsApi.html#getUserrecordingsSummary) | **GET** /api/v2/userrecordings/summary | Get user recording summary
[**putUserrecording**](UserRecordingsApi.html#putUserrecording) | **PUT** /api/v2/userrecordings/{recordingId} | Update a user recording.
{: class="table table-striped"}

<a name="deleteUserrecording"></a>

# void deleteUserrecording(recordingId)



DELETE /api/v2/userrecordings/{recordingId}

Delete a user recording.



Requires NO permissions: 




### Example Usage

~~~ javascript
// Browser
const platformClient = require('platformClient');
// Node
const platformClient = require('purecloud-platform-client-v2');

// Configure OAuth2 access token for authorization: PureCloud Auth
platformClient.ApiClient.instance.authentications['PureCloud Auth'].accessToken = 'YOUR ACCESS TOKEN';

var apiInstance = new platformClient.UserRecordingsApi();

var recordingId = "recordingId_example"; // String | User Recording ID

apiInstance.deleteUserrecording(recordingId)
  .then(function() {
    console.log('deleteUserrecording returned successfully.');
  })
  .catch(function(err) {
  	console.log('There was a failure calling deleteUserrecording');
    console.error(err);
  });

~~~

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
 **recordingId** | **String** | User Recording ID |  |
{: class="table table-striped"}

### Return type

void (no response body)

<a name="getUserrecording"></a>

# UserRecording getUserrecording(recordingId, opts)



GET /api/v2/userrecordings/{recordingId}

Get a user recording.



Requires NO permissions: 




### Example Usage

~~~ javascript
// Browser
const platformClient = require('platformClient');
// Node
const platformClient = require('purecloud-platform-client-v2');

// Configure OAuth2 access token for authorization: PureCloud Auth
platformClient.ApiClient.instance.authentications['PureCloud Auth'].accessToken = 'YOUR ACCESS TOKEN';

var apiInstance = new platformClient.UserRecordingsApi();

var recordingId = "recordingId_example"; // String | User Recording ID

var opts = { 
  'expand': ["expand_example"] // [String] | Which fields, if any, to expand.
};
apiInstance.getUserrecording(recordingId, opts)
  .then(function(data) {
    console.log(`getUserrecording success! data: ${JSON.stringify(data, null, 2)}`);
  })
  .catch(function(err) {
  	console.log('There was a failure calling getUserrecording');
    console.error(err);
  });

~~~

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
 **recordingId** | **String** | User Recording ID |  |
 **expand** | **[String]** | Which fields, if any, to expand. | [optional] <br />**Values**: conversation |
{: class="table table-striped"}

### Return type

**UserRecording**

<a name="getUserrecordingMedia"></a>

# DownloadResponse getUserrecordingMedia(recordingId, opts)



GET /api/v2/userrecordings/{recordingId}/media

Download a user recording.



Requires NO permissions: 




### Example Usage

~~~ javascript
// Browser
const platformClient = require('platformClient');
// Node
const platformClient = require('purecloud-platform-client-v2');

// Configure OAuth2 access token for authorization: PureCloud Auth
platformClient.ApiClient.instance.authentications['PureCloud Auth'].accessToken = 'YOUR ACCESS TOKEN';

var apiInstance = new platformClient.UserRecordingsApi();

var recordingId = "recordingId_example"; // String | User Recording ID

var opts = { 
  'formatId': "WEBM" // String | The desired media format.
};
apiInstance.getUserrecordingMedia(recordingId, opts)
  .then(function(data) {
    console.log(`getUserrecordingMedia success! data: ${JSON.stringify(data, null, 2)}`);
  })
  .catch(function(err) {
  	console.log('There was a failure calling getUserrecordingMedia');
    console.error(err);
  });

~~~

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
 **recordingId** | **String** | User Recording ID |  |
 **formatId** | **String** | The desired media format. | [optional] [default to WEBM]<br />**Values**: WAV, WEBM, WAV_ULAW, OGG_VORBIS, OGG_OPUS, MP3, NONE |
{: class="table table-striped"}

### Return type

**DownloadResponse**

<a name="getUserrecordings"></a>

# UserRecordingEntityListing getUserrecordings(opts)



GET /api/v2/userrecordings

Get a list of user recordings.



Requires NO permissions: 




### Example Usage

~~~ javascript
// Browser
const platformClient = require('platformClient');
// Node
const platformClient = require('purecloud-platform-client-v2');

// Configure OAuth2 access token for authorization: PureCloud Auth
platformClient.ApiClient.instance.authentications['PureCloud Auth'].accessToken = 'YOUR ACCESS TOKEN';

var apiInstance = new platformClient.UserRecordingsApi();

var opts = { 
  'pageSize': 25, // Number | Page size
  'pageNumber': 1, // Number | Page number
  'expand': ["expand_example"] // [String] | Which fields, if any, to expand.
};
apiInstance.getUserrecordings(opts)
  .then(function(data) {
    console.log(`getUserrecordings success! data: ${JSON.stringify(data, null, 2)}`);
  })
  .catch(function(err) {
  	console.log('There was a failure calling getUserrecordings');
    console.error(err);
  });

~~~

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
 **pageSize** | **Number** | Page size | [optional] [default to 25] |
 **pageNumber** | **Number** | Page number | [optional] [default to 1] |
 **expand** | **[String]** | Which fields, if any, to expand. | [optional] <br />**Values**: conversation |
{: class="table table-striped"}

### Return type

**UserRecordingEntityListing**

<a name="getUserrecordingsSummary"></a>

# FaxSummary getUserrecordingsSummary()



GET /api/v2/userrecordings/summary

Get user recording summary



Requires NO permissions: 




### Example Usage

~~~ javascript
// Browser
const platformClient = require('platformClient');
// Node
const platformClient = require('purecloud-platform-client-v2');

// Configure OAuth2 access token for authorization: PureCloud Auth
platformClient.ApiClient.instance.authentications['PureCloud Auth'].accessToken = 'YOUR ACCESS TOKEN';

var apiInstance = new platformClient.UserRecordingsApi();
apiInstance.getUserrecordingsSummary()
  .then(function(data) {
    console.log(`getUserrecordingsSummary success! data: ${JSON.stringify(data, null, 2)}`);
  })
  .catch(function(err) {
  	console.log('There was a failure calling getUserrecordingsSummary');
    console.error(err);
  });

~~~

### Parameters

This endpoint does not need any parameter.
{: class="table table-striped"}

### Return type

**FaxSummary**

<a name="putUserrecording"></a>

# UserRecording putUserrecording(recordingId, body, opts)



PUT /api/v2/userrecordings/{recordingId}

Update a user recording.



Requires NO permissions: 



### Request Body Schema

{::options parse_block_html="true" /}

<script type="text/javascript">
	function copyUserRecordingExample() {
		var $temp = $("<textarea>");
		$("body").append($temp);
		$temp.val($('#UserRecordingExample').text()).select();
		document.execCommand("copy");
		$temp.remove();
	}
</script>

UserRecording <a style="cursor: pointer" onclick="copyUserRecordingExample()">Copy</a>

<div id="UserRecordingExample" style="max-height: 250px; overflow-y: scroll;">
~~~ json
{ 
  "id": String, 
  "name": String, 
  "dateCreated": Date, 
  "dateModified": Date, 
  "contentUri": String, 
  "workspace": { 
    "id": String, 
    "name": String, 
    "selfUri": String, 
  },  
  "createdBy": { 
    "id": String, 
    "name": String, 
    "selfUri": String, 
  },  
  "conversation": { 
    "id": String, 
    "name": String, 
    "startTime": Date, 
    "endTime": Date, 
    "address": String, 
    "participants": { 
      "id": String, 
      "startTime": Date, 
      "endTime": Date, 
      "connectedTime": Date, 
      "name": String, 
      "userUri": String, 
      "userId": String, 
      "externalContactId": String, 
      "externalOrganizationId": String, 
      "queueId": String, 
      "groupId": String, 
      "queueName": String, 
      "purpose": String, 
      "participantType": String, 
      "consultParticipantId": String, 
      "address": String, 
      "ani": String, 
      "aniName": String, 
      "dnis": String, 
      "locale": String, 
      "wrapupRequired": Boolean, 
      "wrapupPrompt": String, 
      "wrapupTimeoutMs": Number, 
      "wrapupSkipped": Boolean, 
      "wrapup": { 
        "code": String, 
        "name": String, 
        "notes": String, 
        "tags": [String], 
        "durationSeconds": Number, 
        "endTime": Date, 
        "provisional": Boolean, 
      },  
      "monitoredParticipantId": String, 
      "attributes": {String: String}, 
      "calls": { 
        "state": String, 
        "id": String, 
        "direction": String, 
        "recording": Boolean, 
        "recordingState": String, 
        "muted": Boolean, 
        "confined": Boolean, 
        "held": Boolean, 
        "recordingId": String, 
        "segments": { 
          "startTime": Date, 
          "endTime": Date, 
          "type": String, 
          "howEnded": String, 
          "disconnectType": String, 
        },  
        "errorInfo": { 
          "status": Number, 
          "code": String, 
          "entityId": String, 
          "entityName": String, 
          "message": String, 
          "messageWithParams": String, 
          "messageParams": {String: String}, 
          "contextId": String, 
          "details": { 
            "errorCode": String, 
            "fieldName": String, 
            "entityId": String, 
            "entityName": String, 
          },  
          "errors": { 
            "status": Number, 
            "code": String, 
            "entityId": String, 
            "entityName": String, 
            "message": String, 
            "messageWithParams": String, 
            "messageParams": {String: String}, 
            "contextId": String, 
            "details": { 
              "errorCode": String, 
              "fieldName": String, 
              "entityId": String, 
              "entityName": String, 
            },  
            "errors": { 
              "status": Number, 
              "code": String, 
              "entityId": String, 
              "entityName": String, 
              "message": String, 
              "messageWithParams": String, 
              "messageParams": {String: String}, 
              "contextId": String, 
              "details": { 
                "errorCode": String, 
                "fieldName": String, 
                "entityId": String, 
                "entityName": String, 
              },  
              "errors": { 
                "status": Number, 
                "code": String, 
                "entityId": String, 
                "entityName": String, 
                "message": String, 
                "messageWithParams": String, 
                "messageParams": {String: String}, 
                "contextId": String, 
                "details": [Detail], 
                "errors": [ErrorBody], 
              },  
            },  
          },  
        },  
        "disconnectType": String, 
        "startHoldTime": Date, 
        "documentId": String, 
        "connectedTime": Date, 
        "disconnectedTime": Date, 
        "disconnectReasons": { 
          "type": String, 
          "code": Number, 
          "phrase": String, 
        },  
        "faxStatus": { 
          "direction": String, 
          "expectedPages": Number, 
          "activePage": Number, 
          "linesTransmitted": Number, 
          "bytesTransmitted": Number, 
          "baudRate": Number, 
          "pageErrors": Number, 
          "lineErrors": Number, 
        },  
        "provider": String, 
        "scriptId": String, 
        "peerId": String, 
        "uuiData": String, 
        "self": { 
          "name": String, 
          "nameRaw": String, 
          "addressNormalized": String, 
          "addressRaw": String, 
          "addressDisplayable": String, 
        },  
        "other": { 
          "name": String, 
          "nameRaw": String, 
          "addressNormalized": String, 
          "addressRaw": String, 
          "addressDisplayable": String, 
        },  
      },  
      "callbacks": { 
        "state": String, 
        "id": String, 
        "segments": { 
          "startTime": Date, 
          "endTime": Date, 
          "type": String, 
          "howEnded": String, 
          "disconnectType": String, 
        },  
        "direction": String, 
        "held": Boolean, 
        "disconnectType": String, 
        "startHoldTime": Date, 
        "dialerPreview": { 
          "id": String, 
          "contactId": String, 
          "contactListId": String, 
          "campaignId": String, 
          "phoneNumberColumns": { 
            "columnName": String, 
            "type": String, 
          },  
        },  
        "voicemail": { 
          "id": String, 
          "uploadStatus": String, 
        },  
        "callbackNumbers": [String], 
        "callbackUserName": String, 
        "scriptId": String, 
        "skipEnabled": Boolean, 
        "timeoutSeconds": Number, 
        "connectedTime": Date, 
        "disconnectedTime": Date, 
        "callbackScheduledTime": Date, 
        "automatedCallbackConfigId": String, 
        "provider": String, 
        "peerId": String, 
      },  
      "chats": { 
        "state": String, 
        "id": String, 
        "roomId": String, 
        "recordingId": String, 
        "segments": { 
          "startTime": Date, 
          "endTime": Date, 
          "type": String, 
          "howEnded": String, 
          "disconnectType": String, 
        },  
        "held": Boolean, 
        "direction": String, 
        "disconnectType": String, 
        "startHoldTime": Date, 
        "connectedTime": Date, 
        "disconnectedTime": Date, 
        "provider": String, 
        "scriptId": String, 
        "peerId": String, 
      },  
      "cobrowsesessions": { 
        "state": String, 
        "id": String, 
        "disconnectType": String, 
        "self": { 
          "name": String, 
          "nameRaw": String, 
          "addressNormalized": String, 
          "addressRaw": String, 
          "addressDisplayable": String, 
        },  
        "cobrowseSessionId": String, 
        "cobrowseRole": String, 
        "controlling": [String], 
        "viewerUrl": String, 
        "providerEventTime": Date, 
        "connectedTime": Date, 
        "disconnectedTime": Date, 
        "provider": String, 
        "peerId": String, 
        "segments": { 
          "startTime": Date, 
          "endTime": Date, 
          "type": String, 
          "howEnded": String, 
          "disconnectType": String, 
        },  
      },  
      "emails": { 
        "state": String, 
        "id": String, 
        "held": Boolean, 
        "subject": String, 
        "messagesSent": Number, 
        "segments": { 
          "startTime": Date, 
          "endTime": Date, 
          "type": String, 
          "howEnded": String, 
          "disconnectType": String, 
        },  
        "direction": String, 
        "recordingId": String, 
        "errorInfo": { 
          "status": Number, 
          "code": String, 
          "entityId": String, 
          "entityName": String, 
          "message": String, 
          "messageWithParams": String, 
          "messageParams": {String: String}, 
          "contextId": String, 
          "details": { 
            "errorCode": String, 
            "fieldName": String, 
            "entityId": String, 
            "entityName": String, 
          },  
          "errors": { 
            "status": Number, 
            "code": String, 
            "entityId": String, 
            "entityName": String, 
            "message": String, 
            "messageWithParams": String, 
            "messageParams": {String: String}, 
            "contextId": String, 
            "details": { 
              "errorCode": String, 
              "fieldName": String, 
              "entityId": String, 
              "entityName": String, 
            },  
            "errors": { 
              "status": Number, 
              "code": String, 
              "entityId": String, 
              "entityName": String, 
              "message": String, 
              "messageWithParams": String, 
              "messageParams": {String: String}, 
              "contextId": String, 
              "details": { 
                "errorCode": String, 
                "fieldName": String, 
                "entityId": String, 
                "entityName": String, 
              },  
              "errors": { 
                "status": Number, 
                "code": String, 
                "entityId": String, 
                "entityName": String, 
                "message": String, 
                "messageWithParams": String, 
                "messageParams": {String: String}, 
                "contextId": String, 
                "details": [Detail], 
                "errors": [ErrorBody], 
              },  
            },  
          },  
        },  
        "disconnectType": String, 
        "startHoldTime": Date, 
        "connectedTime": Date, 
        "disconnectedTime": Date, 
        "autoGenerated": Boolean, 
        "provider": String, 
        "scriptId": String, 
        "peerId": String, 
        "messageId": String, 
        "draftAttachments": { 
          "attachmentId": String, 
          "name": String, 
          "contentUri": String, 
          "contentType": String, 
          "contentLength": Number, 
        },  
      },  
      "messages": { 
        "state": String, 
        "id": String, 
        "held": Boolean, 
        "segments": { 
          "startTime": Date, 
          "endTime": Date, 
          "type": String, 
          "howEnded": String, 
          "disconnectType": String, 
        },  
        "direction": String, 
        "recordingId": String, 
        "errorInfo": { 
          "status": Number, 
          "code": String, 
          "entityId": String, 
          "entityName": String, 
          "message": String, 
          "messageWithParams": String, 
          "messageParams": {String: String}, 
          "contextId": String, 
          "details": { 
            "errorCode": String, 
            "fieldName": String, 
            "entityId": String, 
            "entityName": String, 
          },  
          "errors": { 
            "status": Number, 
            "code": String, 
            "entityId": String, 
            "entityName": String, 
            "message": String, 
            "messageWithParams": String, 
            "messageParams": {String: String}, 
            "contextId": String, 
            "details": { 
              "errorCode": String, 
              "fieldName": String, 
              "entityId": String, 
              "entityName": String, 
            },  
            "errors": { 
              "status": Number, 
              "code": String, 
              "entityId": String, 
              "entityName": String, 
              "message": String, 
              "messageWithParams": String, 
              "messageParams": {String: String}, 
              "contextId": String, 
              "details": { 
                "errorCode": String, 
                "fieldName": String, 
                "entityId": String, 
                "entityName": String, 
              },  
              "errors": { 
                "status": Number, 
                "code": String, 
                "entityId": String, 
                "entityName": String, 
                "message": String, 
                "messageWithParams": String, 
                "messageParams": {String: String}, 
                "contextId": String, 
                "details": [Detail], 
                "errors": [ErrorBody], 
              },  
            },  
          },  
        },  
        "disconnectType": String, 
        "startHoldTime": Date, 
        "connectedTime": Date, 
        "disconnectedTime": Date, 
        "provider": String, 
        "type": String, 
        "recipientCountry": String, 
        "recipientType": String, 
        "scriptId": String, 
        "peerId": String, 
        "toAddress": { 
          "name": String, 
          "nameRaw": String, 
          "addressNormalized": String, 
          "addressRaw": String, 
          "addressDisplayable": String, 
        },  
        "fromAddress": { 
          "name": String, 
          "nameRaw": String, 
          "addressNormalized": String, 
          "addressRaw": String, 
          "addressDisplayable": String, 
        },  
        "messages": { 
          "messageId": String, 
          "messageURI": String, 
          "messageStatus": String, 
          "messageSegmentCount": Number, 
          "messageTime": Date, 
          "media": { 
            "url": String, 
            "mediaType": String, 
            "contentLengthBytes": Number, 
            "name": String, 
            "id": String, 
          },  
          "stickers": { 
            "url": String, 
            "id": String, 
          },  
        },  
      },  
      "screenshares": { 
        "state": String, 
        "id": String, 
        "context": String, 
        "sharing": Boolean, 
        "peerCount": Number, 
        "disconnectType": String, 
        "connectedTime": Date, 
        "disconnectedTime": Date, 
        "provider": String, 
        "peerId": String, 
        "segments": { 
          "startTime": Date, 
          "endTime": Date, 
          "type": String, 
          "howEnded": String, 
          "disconnectType": String, 
        },  
      },  
      "socialExpressions": { 
        "state": String, 
        "id": String, 
        "socialMediaId": String, 
        "socialMediaHub": String, 
        "socialUserName": String, 
        "previewText": String, 
        "recordingId": String, 
        "segments": { 
          "startTime": Date, 
          "endTime": Date, 
          "type": String, 
          "howEnded": String, 
          "disconnectType": String, 
        },  
        "held": Boolean, 
        "disconnectType": String, 
        "startHoldTime": Date, 
        "connectedTime": Date, 
        "disconnectedTime": Date, 
        "provider": String, 
        "scriptId": String, 
        "peerId": String, 
      },  
      "videos": { 
        "state": String, 
        "id": String, 
        "context": String, 
        "audioMuted": Boolean, 
        "videoMuted": Boolean, 
        "sharingScreen": Boolean, 
        "peerCount": Number, 
        "disconnectType": String, 
        "connectedTime": Date, 
        "disconnectedTime": Date, 
        "provider": String, 
        "peerId": String, 
        "msids": [String], 
      },  
      "evaluations": { 
        "id": String, 
        "name": String, 
        "conversation": { 
          "id": String, 
          "name": String, 
          "startTime": Date, 
          "endTime": Date, 
          "address": String, 
          "participants": { 
            "id": String, 
            "startTime": Date, 
            "endTime": Date, 
            "connectedTime": Date, 
            "name": String, 
            "userUri": String, 
            "userId": String, 
            "externalContactId": String, 
            "externalOrganizationId": String, 
            "queueId": String, 
            "groupId": String, 
            "queueName": String, 
            "purpose": String, 
            "participantType": String, 
            "consultParticipantId": String, 
            "address": String, 
            "ani": String, 
            "aniName": String, 
            "dnis": String, 
            "locale": String, 
            "wrapupRequired": Boolean, 
            "wrapupPrompt": String, 
            "wrapupTimeoutMs": Number, 
            "wrapupSkipped": Boolean, 
            "wrapup": { 
              "code": String, 
              "name": String, 
              "notes": String, 
              "tags": [String], 
              "durationSeconds": Number, 
              "endTime": Date, 
              "provisional": Boolean, 
            },  
            "monitoredParticipantId": String, 
            "attributes": {String: String}, 
            "calls": { 
              "state": String, 
              "id": String, 
              "direction": String, 
              "recording": Boolean, 
              "recordingState": String, 
              "muted": Boolean, 
              "confined": Boolean, 
              "held": Boolean, 
              "recordingId": String, 
              "segments": { 
                "startTime": Date, 
                "endTime": Date, 
                "type": String, 
                "howEnded": String, 
                "disconnectType": String, 
              },  
              "errorInfo": { 
                "status": Number, 
                "code": String, 
                "entityId": String, 
                "entityName": String, 
                "message": String, 
                "messageWithParams": String, 
                "messageParams": {String: String}, 
                "contextId": String, 
                "details": [Detail], 
                "errors": [ErrorBody], 
              },  
              "disconnectType": String, 
              "startHoldTime": Date, 
              "documentId": String, 
              "connectedTime": Date, 
              "disconnectedTime": Date, 
              "disconnectReasons": { 
                "type": String, 
                "code": Number, 
                "phrase": String, 
              },  
              "faxStatus": { 
                "direction": String, 
                "expectedPages": Number, 
                "activePage": Number, 
                "linesTransmitted": Number, 
                "bytesTransmitted": Number, 
                "baudRate": Number, 
                "pageErrors": Number, 
                "lineErrors": Number, 
              },  
              "provider": String, 
              "scriptId": String, 
              "peerId": String, 
              "uuiData": String, 
              "self": { 
                "name": String, 
                "nameRaw": String, 
                "addressNormalized": String, 
                "addressRaw": String, 
                "addressDisplayable": String, 
              },  
              "other": { 
                "name": String, 
                "nameRaw": String, 
                "addressNormalized": String, 
                "addressRaw": String, 
                "addressDisplayable": String, 
              },  
            },  
            "callbacks": { 
              "state": String, 
              "id": String, 
              "segments": { 
                "startTime": Date, 
                "endTime": Date, 
                "type": String, 
                "howEnded": String, 
                "disconnectType": String, 
              },  
              "direction": String, 
              "held": Boolean, 
              "disconnectType": String, 
              "startHoldTime": Date, 
              "dialerPreview": { 
                "id": String, 
                "contactId": String, 
                "contactListId": String, 
                "campaignId": String, 
                "phoneNumberColumns": [PhoneNumberColumn], 
              },  
              "voicemail": { 
                "id": String, 
                "uploadStatus": String, 
              },  
              "callbackNumbers": [String], 
              "callbackUserName": String, 
              "scriptId": String, 
              "skipEnabled": Boolean, 
              "timeoutSeconds": Number, 
              "connectedTime": Date, 
              "disconnectedTime": Date, 
              "callbackScheduledTime": Date, 
              "automatedCallbackConfigId": String, 
              "provider": String, 
              "peerId": String, 
            },  
            "chats": { 
              "state": String, 
              "id": String, 
              "roomId": String, 
              "recordingId": String, 
              "segments": { 
                "startTime": Date, 
                "endTime": Date, 
                "type": String, 
                "howEnded": String, 
                "disconnectType": String, 
              },  
              "held": Boolean, 
              "direction": String, 
              "disconnectType": String, 
              "startHoldTime": Date, 
              "connectedTime": Date, 
              "disconnectedTime": Date, 
              "provider": String, 
              "scriptId": String, 
              "peerId": String, 
            },  
            "cobrowsesessions": { 
              "state": String, 
              "id": String, 
              "disconnectType": String, 
              "self": { 
                "name": String, 
                "nameRaw": String, 
                "addressNormalized": String, 
                "addressRaw": String, 
                "addressDisplayable": String, 
              },  
              "cobrowseSessionId": String, 
              "cobrowseRole": String, 
              "controlling": [String], 
              "viewerUrl": String, 
              "providerEventTime": Date, 
              "connectedTime": Date, 
              "disconnectedTime": Date, 
              "provider": String, 
              "peerId": String, 
              "segments": { 
                "startTime": Date, 
                "endTime": Date, 
                "type": String, 
                "howEnded": String, 
                "disconnectType": String, 
              },  
            },  
            "emails": { 
              "state": String, 
              "id": String, 
              "held": Boolean, 
              "subject": String, 
              "messagesSent": Number, 
              "segments": { 
                "startTime": Date, 
                "endTime": Date, 
                "type": String, 
                "howEnded": String, 
                "disconnectType": String, 
              },  
              "direction": String, 
              "recordingId": String, 
              "errorInfo": { 
                "status": Number, 
                "code": String, 
                "entityId": String, 
                "entityName": String, 
                "message": String, 
                "messageWithParams": String, 
                "messageParams": {String: String}, 
                "contextId": String, 
                "details": [Detail], 
                "errors": [ErrorBody], 
              },  
              "disconnectType": String, 
              "startHoldTime": Date, 
              "connectedTime": Date, 
              "disconnectedTime": Date, 
              "autoGenerated": Boolean, 
              "provider": String, 
              "scriptId": String, 
              "peerId": String, 
              "messageId": String, 
              "draftAttachments": { 
                "attachmentId": String, 
                "name": String, 
                "contentUri": String, 
                "contentType": String, 
                "contentLength": Number, 
              },  
            },  
            "messages": { 
              "state": String, 
              "id": String, 
              "held": Boolean, 
              "segments": { 
                "startTime": Date, 
                "endTime": Date, 
                "type": String, 
                "howEnded": String, 
                "disconnectType": String, 
              },  
              "direction": String, 
              "recordingId": String, 
              "errorInfo": { 
                "status": Number, 
                "code": String, 
                "entityId": String, 
                "entityName": String, 
                "message": String, 
                "messageWithParams": String, 
                "messageParams": {String: String}, 
                "contextId": String, 
                "details": [Detail], 
                "errors": [ErrorBody], 
              },  
              "disconnectType": String, 
              "startHoldTime": Date, 
              "connectedTime": Date, 
              "disconnectedTime": Date, 
              "provider": String, 
              "type": String, 
              "recipientCountry": String, 
              "recipientType": String, 
              "scriptId": String, 
              "peerId": String, 
              "toAddress": { 
                "name": String, 
                "nameRaw": String, 
                "addressNormalized": String, 
                "addressRaw": String, 
                "addressDisplayable": String, 
              },  
              "fromAddress": { 
                "name": String, 
                "nameRaw": String, 
                "addressNormalized": String, 
                "addressRaw": String, 
                "addressDisplayable": String, 
              },  
              "messages": { 
                "messageId": String, 
                "messageURI": String, 
                "messageStatus": String, 
                "messageSegmentCount": Number, 
                "messageTime": Date, 
                "media": [MessageMedia], 
                "stickers": [MessageSticker], 
              },  
            },  
            "screenshares": { 
              "state": String, 
              "id": String, 
              "context": String, 
              "sharing": Boolean, 
              "peerCount": Number, 
              "disconnectType": String, 
              "connectedTime": Date, 
              "disconnectedTime": Date, 
              "provider": String, 
              "peerId": String, 
              "segments": { 
                "startTime": Date, 
                "endTime": Date, 
                "type": String, 
                "howEnded": String, 
                "disconnectType": String, 
              },  
            },  
            "socialExpressions": { 
              "state": String, 
              "id": String, 
              "socialMediaId": String, 
              "socialMediaHub": String, 
              "socialUserName": String, 
              "previewText": String, 
              "recordingId": String, 
              "segments": { 
                "startTime": Date, 
                "endTime": Date, 
                "type": String, 
                "howEnded": String, 
                "disconnectType": String, 
              },  
              "held": Boolean, 
              "disconnectType": String, 
              "startHoldTime": Date, 
              "connectedTime": Date, 
              "disconnectedTime": Date, 
              "provider": String, 
              "scriptId": String, 
              "peerId": String, 
            },  
            "videos": { 
              "state": String, 
              "id": String, 
              "context": String, 
              "audioMuted": Boolean, 
              "videoMuted": Boolean, 
              "sharingScreen": Boolean, 
              "peerCount": Number, 
              "disconnectType": String, 
              "connectedTime": Date, 
              "disconnectedTime": Date, 
              "provider": String, 
              "peerId": String, 
              "msids": [String], 
            },  
            "evaluations": { 
              "id": String, 
              "name": String, 
              "conversation": { 
                "id": String, 
                "name": String, 
                "startTime": Date, 
                "endTime": Date, 
                "address": String, 
                "participants": [Participant], 
                "conversationIds": [String], 
                "maxParticipants": Number, 
                "recordingState": String, 
                "state": String, 
                "selfUri": String, 
              },  
              "evaluationForm": { 
                "id": String, 
                "name": String, 
                "modifiedDate": Date, 
                "published": Boolean, 
                "contextId": String, 
                "questionGroups": [QuestionGroup], 
                "publishedVersions": DomainEntityListingEvaluationForm, 
                "selfUri": String, 
              },  
              "evaluator": { 
                "id": String, 
                "name": String, 
                "chat": Chat, 
                "department": String, 
                "email": String, 
                "primaryContactInfo": [Contact], 
                "addresses": [Contact], 
                "state": String, 
                "title": String, 
                "username": String, 
                "manager": User, 
                "images": [UserImage], 
                "version": Number, 
                "routingStatus": RoutingStatus, 
                "presence": UserPresence, 
                "conversationSummary": UserConversationSummary, 
                "outOfOffice": OutOfOffice, 
                "geolocation": Geolocation, 
                "station": UserStations, 
                "authorization": UserAuthorization, 
                "profileSkills": [String], 
                "locations": [Location], 
                "groups": [Group], 
                "acdAutoAnswer": Boolean, 
                "selfUri": String, 
              },  
              "agent": { 
                "id": String, 
                "name": String, 
                "chat": Chat, 
                "department": String, 
                "email": String, 
                "primaryContactInfo": [Contact], 
                "addresses": [Contact], 
                "state": String, 
                "title": String, 
                "username": String, 
                "manager": User, 
                "images": [UserImage], 
                "version": Number, 
                "routingStatus": RoutingStatus, 
                "presence": UserPresence, 
                "conversationSummary": UserConversationSummary, 
                "outOfOffice": OutOfOffice, 
                "geolocation": Geolocation, 
                "station": UserStations, 
                "authorization": UserAuthorization, 
                "profileSkills": [String], 
                "locations": [Location], 
                "groups": [Group], 
                "acdAutoAnswer": Boolean, 
                "selfUri": String, 
              },  
              "calibration": { 
                "id": String, 
                "name": String, 
                "calibrator": User, 
                "agent": User, 
                "conversation": Conversation, 
                "evaluationForm": EvaluationForm, 
                "contextId": String, 
                "averageScore": Number, 
                "highScore": Number, 
                "lowScore": Number, 
                "createdDate": Date, 
                "evaluations": [Evaluation], 
                "evaluators": [User], 
                "scoringIndex": Evaluation, 
                "expertEvaluator": User, 
                "selfUri": String, 
              },  
              "status": String, 
              "answers": { 
                "totalScore": Number, 
                "totalCriticalScore": Number, 
                "questionGroupScores": [QuestionGroupScore], 
                "anyFailedKillQuestions": Boolean, 
                "comments": String, 
                "agentComments": String, 
              },  
              "agentHasRead": Boolean, 
              "releaseDate": Date, 
              "assignedDate": Date, 
              "changedDate": Date, 
              "queue": { 
                "id": String, 
                "name": String, 
                "division": Division, 
                "description": String, 
                "version": Number, 
                "dateCreated": Date, 
                "dateModified": Date, 
                "modifiedBy": String, 
                "createdBy": String, 
                "state": String, 
                "modifiedByApp": String, 
                "createdByApp": String, 
                "mediaSettings": {String: MediaSetting}, 
                "bullseye": Bullseye, 
                "acwSettings": AcwSettings, 
                "skillEvaluationMethod": String, 
                "queueFlow": UriReference, 
                "whisperPrompt": UriReference, 
                "autoAnswerOnly": Boolean, 
                "callingPartyName": String, 
                "callingPartyNumber": String, 
                "defaultScripts": {String: Script}, 
                "outboundEmailAddress": QueueEmailAddress, 
                "memberCount": Number, 
                "selfUri": String, 
              },  
              "neverRelease": Boolean, 
              "resourceId": String, 
              "resourceType": String, 
              "redacted": Boolean, 
              "isScoringIndex": Boolean, 
              "selfUri": String, 
            },  
            "screenRecordingState": String, 
            "flaggedReason": String, 
          },  
          "conversationIds": [String], 
          "maxParticipants": Number, 
          "recordingState": String, 
          "state": String, 
          "selfUri": String, 
        },  
        "evaluationForm": { 
          "id": String, 
          "name": String, 
          "modifiedDate": Date, 
          "published": Boolean, 
          "contextId": String, 
          "questionGroups": { 
            "id": String, 
            "name": String, 
            "type": String, 
            "defaultAnswersToHighest": Boolean, 
            "defaultAnswersToNA": Boolean, 
            "naEnabled": Boolean, 
            "weight": Number, 
            "manualWeight": Boolean, 
            "questions": { 
              "id": String, 
              "text": String, 
              "helpText": String, 
              "type": String, 
              "naEnabled": Boolean, 
              "commentsRequired": Boolean, 
              "visibilityCondition": { 
                "combiningOperation": String, 
                "predicates": [Object], 
              },  
              "answerOptions": { 
                "id": String, 
                "text": String, 
                "value": Number, 
              },  
              "maxResponseCharacters": Number, 
              "explanationPrompt": String, 
              "isKill": Boolean, 
              "isCritical": Boolean, 
            },  
            "visibilityCondition": { 
              "combiningOperation": String, 
              "predicates": [Object], 
            },  
          },  
          "publishedVersions": { 
            "entities": { 
              "id": String, 
              "name": String, 
              "modifiedDate": Date, 
              "published": Boolean, 
              "contextId": String, 
              "questionGroups": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "defaultAnswersToHighest": Boolean, 
                "defaultAnswersToNA": Boolean, 
                "naEnabled": Boolean, 
                "weight": Number, 
                "manualWeight": Boolean, 
                "questions": [Question], 
                "visibilityCondition": VisibilityCondition, 
              },  
              "publishedVersions": { 
                "entities": [EvaluationForm], 
                "pageSize": Number, 
                "pageNumber": Number, 
                "total": Number, 
                "selfUri": String, 
                "firstUri": String, 
                "previousUri": String, 
                "nextUri": String, 
                "lastUri": String, 
                "pageCount": Number, 
              },  
              "selfUri": String, 
            },  
            "pageSize": Number, 
            "pageNumber": Number, 
            "total": Number, 
            "selfUri": String, 
            "firstUri": String, 
            "previousUri": String, 
            "nextUri": String, 
            "lastUri": String, 
            "pageCount": Number, 
          },  
          "selfUri": String, 
        },  
        "evaluator": { 
          "id": String, 
          "name": String, 
          "chat": { 
            "jabberId": String, 
          },  
          "department": String, 
          "email": String, 
          "primaryContactInfo": { 
            "address": String, 
            "display": String, 
            "mediaType": String, 
            "type": String, 
            "extension": String, 
          },  
          "addresses": { 
            "address": String, 
            "display": String, 
            "mediaType": String, 
            "type": String, 
            "extension": String, 
          },  
          "state": String, 
          "title": String, 
          "username": String, 
          "manager": User, 
          "images": { 
            "resolution": String, 
            "imageUri": String, 
          },  
          "version": Number, 
          "routingStatus": { 
            "userId": String, 
            "status": String, 
            "startTime": Date, 
          },  
          "presence": { 
            "id": String, 
            "name": String, 
            "source": String, 
            "primary": Boolean, 
            "presenceDefinition": { 
              "id": String, 
              "systemPresence": String, 
              "selfUri": String, 
            },  
            "message": String, 
            "modifiedDate": Date, 
            "selfUri": String, 
          },  
          "conversationSummary": { 
            "userId": String, 
            "call": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "callback": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "email": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "message": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "chat": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "socialExpression": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "video": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
          },  
          "outOfOffice": { 
            "id": String, 
            "name": String, 
            "user": User, 
            "startDate": Date, 
            "endDate": Date, 
            "active": Boolean, 
            "indefinite": Boolean, 
            "selfUri": String, 
          },  
          "geolocation": { 
            "id": String, 
            "name": String, 
            "type": String, 
            "primary": Boolean, 
            "latitude": Number, 
            "longitude": Number, 
            "country": String, 
            "region": String, 
            "city": String, 
            "locations": { 
              "id": String, 
              "name": String, 
              "address": { 
                "city": String, 
                "country": String, 
                "countryName": String, 
                "state": String, 
                "street1": String, 
                "street2": String, 
                "zipcode": String, 
              },  
              "addressVerified": Boolean, 
              "emergencyNumber": { 
                "e164": String, 
                "number": String, 
                "type": String, 
              },  
              "state": String, 
              "version": Number, 
              "path": [String], 
              "selfUri": String, 
            },  
            "selfUri": String, 
          },  
          "station": { 
            "associatedStation": { 
              "id": String, 
              "name": String, 
              "type": String, 
              "associatedUser": User, 
              "associatedDate": Date, 
              "defaultUser": User, 
              "providerInfo": {String: String}, 
            },  
            "effectiveStation": { 
              "id": String, 
              "name": String, 
              "type": String, 
              "associatedUser": User, 
              "associatedDate": Date, 
              "defaultUser": User, 
              "providerInfo": {String: String}, 
            },  
            "defaultStation": { 
              "id": String, 
              "name": String, 
              "type": String, 
              "associatedUser": User, 
              "associatedDate": Date, 
              "defaultUser": User, 
              "providerInfo": {String: String}, 
            },  
            "lastAssociatedStation": { 
              "id": String, 
              "name": String, 
              "type": String, 
              "associatedUser": User, 
              "associatedDate": Date, 
              "defaultUser": User, 
              "providerInfo": {String: String}, 
            },  
          },  
          "authorization": { 
            "roles": { 
              "id": String, 
              "name": String, 
            },  
            "permissions": [String], 
            "permissionPolicies": { 
              "id": String, 
              "domain": String, 
              "entityName": String, 
              "policyName": String, 
              "policyDescription": String, 
              "actionSetKey": String, 
              "allowConditions": Boolean, 
              "resourceConditionNode": { 
                "variableName": String, 
                "conjunction": String, 
                "operator": String, 
                "operands": [ResourceConditionValue], 
                "terms": [ResourceConditionNode], 
              },  
              "namedResources": [String], 
              "resourceCondition": String, 
              "actionSet": [String], 
            },  
          },  
          "profileSkills": [String], 
          "locations": { 
            "id": String, 
            "floorplanId": String, 
            "coordinates": {String: Number}, 
            "notes": String, 
            "locationDefinition": { 
              "id": String, 
              "name": String, 
              "address": { 
                "city": String, 
                "country": String, 
                "countryName": String, 
                "state": String, 
                "street1": String, 
                "street2": String, 
                "zipcode": String, 
              },  
              "addressVerified": Boolean, 
              "emergencyNumber": { 
                "e164": String, 
                "number": String, 
                "type": String, 
              },  
              "state": String, 
              "version": Number, 
              "path": [String], 
              "selfUri": String, 
            },  
          },  
          "groups": { 
            "id": String, 
            "name": String, 
            "description": String, 
            "dateModified": Date, 
            "memberCount": Number, 
            "state": String, 
            "version": Number, 
            "type": String, 
            "images": { 
              "resolution": String, 
              "imageUri": String, 
            },  
            "addresses": { 
              "address": String, 
              "display": String, 
              "type": String, 
              "mediaType": String, 
            },  
            "rulesVisible": Boolean, 
            "visibility": String, 
            "owners": User, 
            "selfUri": String, 
          },  
          "acdAutoAnswer": Boolean, 
          "selfUri": String, 
        },  
        "agent": { 
          "id": String, 
          "name": String, 
          "chat": { 
            "jabberId": String, 
          },  
          "department": String, 
          "email": String, 
          "primaryContactInfo": { 
            "address": String, 
            "display": String, 
            "mediaType": String, 
            "type": String, 
            "extension": String, 
          },  
          "addresses": { 
            "address": String, 
            "display": String, 
            "mediaType": String, 
            "type": String, 
            "extension": String, 
          },  
          "state": String, 
          "title": String, 
          "username": String, 
          "manager": User, 
          "images": { 
            "resolution": String, 
            "imageUri": String, 
          },  
          "version": Number, 
          "routingStatus": { 
            "userId": String, 
            "status": String, 
            "startTime": Date, 
          },  
          "presence": { 
            "id": String, 
            "name": String, 
            "source": String, 
            "primary": Boolean, 
            "presenceDefinition": { 
              "id": String, 
              "systemPresence": String, 
              "selfUri": String, 
            },  
            "message": String, 
            "modifiedDate": Date, 
            "selfUri": String, 
          },  
          "conversationSummary": { 
            "userId": String, 
            "call": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "callback": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "email": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "message": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "chat": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "socialExpression": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
            "video": { 
              "contactCenter": { 
                "active": Number, 
                "acw": Number, 
              },  
              "enterprise": { 
                "active": Number, 
                "acw": Number, 
              },  
            },  
          },  
          "outOfOffice": { 
            "id": String, 
            "name": String, 
            "user": User, 
            "startDate": Date, 
            "endDate": Date, 
            "active": Boolean, 
            "indefinite": Boolean, 
            "selfUri": String, 
          },  
          "geolocation": { 
            "id": String, 
            "name": String, 
            "type": String, 
            "primary": Boolean, 
            "latitude": Number, 
            "longitude": Number, 
            "country": String, 
            "region": String, 
            "city": String, 
            "locations": { 
              "id": String, 
              "name": String, 
              "address": { 
                "city": String, 
                "country": String, 
                "countryName": String, 
                "state": String, 
                "street1": String, 
                "street2": String, 
                "zipcode": String, 
              },  
              "addressVerified": Boolean, 
              "emergencyNumber": { 
                "e164": String, 
                "number": String, 
                "type": String, 
              },  
              "state": String, 
              "version": Number, 
              "path": [String], 
              "selfUri": String, 
            },  
            "selfUri": String, 
          },  
          "station": { 
            "associatedStation": { 
              "id": String, 
              "name": String, 
              "type": String, 
              "associatedUser": User, 
              "associatedDate": Date, 
              "defaultUser": User, 
              "providerInfo": {String: String}, 
            },  
            "effectiveStation": { 
              "id": String, 
              "name": String, 
              "type": String, 
              "associatedUser": User, 
              "associatedDate": Date, 
              "defaultUser": User, 
              "providerInfo": {String: String}, 
            },  
            "defaultStation": { 
              "id": String, 
              "name": String, 
              "type": String, 
              "associatedUser": User, 
              "associatedDate": Date, 
              "defaultUser": User, 
              "providerInfo": {String: String}, 
            },  
            "lastAssociatedStation": { 
              "id": String, 
              "name": String, 
              "type": String, 
              "associatedUser": User, 
              "associatedDate": Date, 
              "defaultUser": User, 
              "providerInfo": {String: String}, 
            },  
          },  
          "authorization": { 
            "roles": { 
              "id": String, 
              "name": String, 
            },  
            "permissions": [String], 
            "permissionPolicies": { 
              "id": String, 
              "domain": String, 
              "entityName": String, 
              "policyName": String, 
              "policyDescription": String, 
              "actionSetKey": String, 
              "allowConditions": Boolean, 
              "resourceConditionNode": { 
                "variableName": String, 
                "conjunction": String, 
                "operator": String, 
                "operands": [ResourceConditionValue], 
                "terms": [ResourceConditionNode], 
              },  
              "namedResources": [String], 
              "resourceCondition": String, 
              "actionSet": [String], 
            },  
          },  
          "profileSkills": [String], 
          "locations": { 
            "id": String, 
            "floorplanId": String, 
            "coordinates": {String: Number}, 
            "notes": String, 
            "locationDefinition": { 
              "id": String, 
              "name": String, 
              "address": { 
                "city": String, 
                "country": String, 
                "countryName": String, 
                "state": String, 
                "street1": String, 
                "street2": String, 
                "zipcode": String, 
              },  
              "addressVerified": Boolean, 
              "emergencyNumber": { 
                "e164": String, 
                "number": String, 
                "type": String, 
              },  
              "state": String, 
              "version": Number, 
              "path": [String], 
              "selfUri": String, 
            },  
          },  
          "groups": { 
            "id": String, 
            "name": String, 
            "description": String, 
            "dateModified": Date, 
            "memberCount": Number, 
            "state": String, 
            "version": Number, 
            "type": String, 
            "images": { 
              "resolution": String, 
              "imageUri": String, 
            },  
            "addresses": { 
              "address": String, 
              "display": String, 
              "type": String, 
              "mediaType": String, 
            },  
            "rulesVisible": Boolean, 
            "visibility": String, 
            "owners": User, 
            "selfUri": String, 
          },  
          "acdAutoAnswer": Boolean, 
          "selfUri": String, 
        },  
        "calibration": { 
          "id": String, 
          "name": String, 
          "calibrator": { 
            "id": String, 
            "name": String, 
            "chat": { 
              "jabberId": String, 
            },  
            "department": String, 
            "email": String, 
            "primaryContactInfo": { 
              "address": String, 
              "display": String, 
              "mediaType": String, 
              "type": String, 
              "extension": String, 
            },  
            "addresses": { 
              "address": String, 
              "display": String, 
              "mediaType": String, 
              "type": String, 
              "extension": String, 
            },  
            "state": String, 
            "title": String, 
            "username": String, 
            "manager": User, 
            "images": { 
              "resolution": String, 
              "imageUri": String, 
            },  
            "version": Number, 
            "routingStatus": { 
              "userId": String, 
              "status": String, 
              "startTime": Date, 
            },  
            "presence": { 
              "id": String, 
              "name": String, 
              "source": String, 
              "primary": Boolean, 
              "presenceDefinition": { 
                "id": String, 
                "systemPresence": String, 
                "selfUri": String, 
              },  
              "message": String, 
              "modifiedDate": Date, 
              "selfUri": String, 
            },  
            "conversationSummary": { 
              "userId": String, 
              "call": { 
                "contactCenter": MediaSummaryDetail, 
                "enterprise": MediaSummaryDetail, 
              },  
              "callback": { 
                "contactCenter": MediaSummaryDetail, 
                "enterprise": MediaSummaryDetail, 
              },  
              "email": { 
                "contactCenter": MediaSummaryDetail, 
                "enterprise": MediaSummaryDetail, 
              },  
              "message": { 
                "contactCenter": MediaSummaryDetail, 
                "enterprise": MediaSummaryDetail, 
              },  
              "chat": { 
                "contactCenter": MediaSummaryDetail, 
                "enterprise": MediaSummaryDetail, 
              },  
              "socialExpression": { 
                "contactCenter": MediaSummaryDetail, 
                "enterprise": MediaSummaryDetail, 
              },  
              "video": { 
                "contactCenter": MediaSummaryDetail, 
                "enterprise": MediaSummaryDetail, 
              },  
            },  
            "outOfOffice": { 
              "id": String, 
              "name": String, 
              "user": User, 
              "startDate": Date, 
              "endDate": Date, 
              "active": Boolean, 
              "indefinite": Boolean, 
              "selfUri": String, 
            },  
            "geolocation": { 
              "id": String, 
              "name": String, 
              "type": String, 
              "primary": Boolean, 
              "latitude": Number, 
              "longitude": Number, 
              "country": String, 
              "region": String, 
              "city": String, 
              "locations": { 
                "id": String, 
                "name": String, 
                "address": LocationAddress, 
                "addressVerified": Boolean, 
                "emergencyNumber": LocationEmergencyNumber, 
                "state": String, 
                "version": Number, 
                "path": [String], 
                "selfUri": String, 
              },  
              "selfUri": String, 
            },  
            "station": { 
              "associatedStation": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "associatedUser": User, 
                "associatedDate": Date, 
                "defaultUser": User, 
                "providerInfo": {String: String}, 
              },  
              "effectiveStation": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "associatedUser": User, 
                "associatedDate": Date, 
                "defaultUser": User, 
                "providerInfo": {String: String}, 
              },  
              "defaultStation": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "associatedUser": User, 
                "associatedDate": Date, 
                "defaultUser": User, 
                "providerInfo": {String: String}, 
              },  
              "lastAssociatedStation": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "associatedUser": User, 
                "associatedDate": Date, 
                "defaultUser": User, 
                "providerInfo": {String: String}, 
              },  
            },  
            "authorization": { 
              "roles": { 
                "id": String, 
                "name": String, 
              },  
              "permissions": [String], 
              "permissionPolicies": { 
                "id": String, 
                "domain": String, 
                "entityName": String, 
                "policyName": String, 
                "policyDescription": String, 
                "actionSetKey": String, 
                "allowConditions": Boolean, 
                "resourceConditionNode": ResourceConditionNode, 
                "namedResources": [String], 
                "resourceCondition": String, 
                "actionSet": [String], 
              },  
            },  
            "profileSkills": [String], 
            "locations": { 
              "id": String, 
              "floorplanId": String, 
              "coordinates": {String: Number}, 
              "notes": String, 
              "locationDefinition": { 
                "id": String, 
                "name": String, 
                "address": LocationAddress, 
                "addressVerified": Boolean, 
                "emergencyNumber": LocationEmergencyNumber, 
                "state": String, 
                "version": Number, 
                "path": [String], 
                "selfUri": String, 
              },  
            },  
            "groups": { 
              "id": String, 
              "name": String, 
              "description": String, 
              "dateModified": Date, 
              "memberCount": Number, 
              "state": String, 
              "version": Number, 
              "type": String, 
              "images": { 
                "resolution": String, 
                "imageUri": String, 
              },  
              "addresses": { 
                "address": String, 
                "display": String, 
                "type": String, 
                "mediaType": String, 
              },  
              "rulesVisible": Boolean, 
              "visibility": String, 
              "owners": User, 
              "selfUri": String, 
            },  
            "acdAutoAnswer": Boolean, 
            "selfUri": String, 
          },  
          "agent": User, 
          "conversation": { 
            "id": String, 
            "name": String, 
            "startTime": Date, 
            "endTime": Date, 
            "address": String, 
            "participants": { 
              "id": String, 
              "startTime": Date, 
              "endTime": Date, 
              "connectedTime": Date, 
              "name": String, 
              "userUri": String, 
              "userId": String, 
              "externalContactId": String, 
              "externalOrganizationId": String, 
              "queueId": String, 
              "groupId": String, 
              "queueName": String, 
              "purpose": String, 
              "participantType": String, 
              "consultParticipantId": String, 
              "address": String, 
              "ani": String, 
              "aniName": String, 
              "dnis": String, 
              "locale": String, 
              "wrapupRequired": Boolean, 
              "wrapupPrompt": String, 
              "wrapupTimeoutMs": Number, 
              "wrapupSkipped": Boolean, 
              "wrapup": { 
                "code": String, 
                "name": String, 
                "notes": String, 
                "tags": [String], 
                "durationSeconds": Number, 
                "endTime": Date, 
                "provisional": Boolean, 
              },  
              "monitoredParticipantId": String, 
              "attributes": {String: String}, 
              "calls": { 
                "state": String, 
                "id": String, 
                "direction": String, 
                "recording": Boolean, 
                "recordingState": String, 
                "muted": Boolean, 
                "confined": Boolean, 
                "held": Boolean, 
                "recordingId": String, 
                "segments": [Segment], 
                "errorInfo": ErrorBody, 
                "disconnectType": String, 
                "startHoldTime": Date, 
                "documentId": String, 
                "connectedTime": Date, 
                "disconnectedTime": Date, 
                "disconnectReasons": [DisconnectReason], 
                "faxStatus": FaxStatus, 
                "provider": String, 
                "scriptId": String, 
                "peerId": String, 
                "uuiData": String, 
                "self": Address, 
                "other": Address, 
              },  
              "callbacks": { 
                "state": String, 
                "id": String, 
                "segments": [Segment], 
                "direction": String, 
                "held": Boolean, 
                "disconnectType": String, 
                "startHoldTime": Date, 
                "dialerPreview": DialerPreview, 
                "voicemail": Voicemail, 
                "callbackNumbers": [String], 
                "callbackUserName": String, 
                "scriptId": String, 
                "skipEnabled": Boolean, 
                "timeoutSeconds": Number, 
                "connectedTime": Date, 
                "disconnectedTime": Date, 
                "callbackScheduledTime": Date, 
                "automatedCallbackConfigId": String, 
                "provider": String, 
                "peerId": String, 
              },  
              "chats": { 
                "state": String, 
                "id": String, 
                "roomId": String, 
                "recordingId": String, 
                "segments": [Segment], 
                "held": Boolean, 
                "direction": String, 
                "disconnectType": String, 
                "startHoldTime": Date, 
                "connectedTime": Date, 
                "disconnectedTime": Date, 
                "provider": String, 
                "scriptId": String, 
                "peerId": String, 
              },  
              "cobrowsesessions": { 
                "state": String, 
                "id": String, 
                "disconnectType": String, 
                "self": Address, 
                "cobrowseSessionId": String, 
                "cobrowseRole": String, 
                "controlling": [String], 
                "viewerUrl": String, 
                "providerEventTime": Date, 
                "connectedTime": Date, 
                "disconnectedTime": Date, 
                "provider": String, 
                "peerId": String, 
                "segments": [Segment], 
              },  
              "emails": { 
                "state": String, 
                "id": String, 
                "held": Boolean, 
                "subject": String, 
                "messagesSent": Number, 
                "segments": [Segment], 
                "direction": String, 
                "recordingId": String, 
                "errorInfo": ErrorBody, 
                "disconnectType": String, 
                "startHoldTime": Date, 
                "connectedTime": Date, 
                "disconnectedTime": Date, 
                "autoGenerated": Boolean, 
                "provider": String, 
                "scriptId": String, 
                "peerId": String, 
                "messageId": String, 
                "draftAttachments": [Attachment], 
              },  
              "messages": { 
                "state": String, 
                "id": String, 
                "held": Boolean, 
                "segments": [Segment], 
                "direction": String, 
                "recordingId": String, 
                "errorInfo": ErrorBody, 
                "disconnectType": String, 
                "startHoldTime": Date, 
                "connectedTime": Date, 
                "disconnectedTime": Date, 
                "provider": String, 
                "type": String, 
                "recipientCountry": String, 
                "recipientType": String, 
                "scriptId": String, 
                "peerId": String, 
                "toAddress": Address, 
                "fromAddress": Address, 
                "messages": [MessageDetails], 
              },  
              "screenshares": { 
                "state": String, 
                "id": String, 
                "context": String, 
                "sharing": Boolean, 
                "peerCount": Number, 
                "disconnectType": String, 
                "connectedTime": Date, 
                "disconnectedTime": Date, 
                "provider": String, 
                "peerId": String, 
                "segments": [Segment], 
              },  
              "socialExpressions": { 
                "state": String, 
                "id": String, 
                "socialMediaId": String, 
                "socialMediaHub": String, 
                "socialUserName": String, 
                "previewText": String, 
                "recordingId": String, 
                "segments": [Segment], 
                "held": Boolean, 
                "disconnectType": String, 
                "startHoldTime": Date, 
                "connectedTime": Date, 
                "disconnectedTime": Date, 
                "provider": String, 
                "scriptId": String, 
                "peerId": String, 
              },  
              "videos": { 
                "state": String, 
                "id": String, 
                "context": String, 
                "audioMuted": Boolean, 
                "videoMuted": Boolean, 
                "sharingScreen": Boolean, 
                "peerCount": Number, 
                "disconnectType": String, 
                "connectedTime": Date, 
                "disconnectedTime": Date, 
                "provider": String, 
                "peerId": String, 
                "msids": [String], 
              },  
              "evaluations": { 
                "id": String, 
                "name": String, 
                "conversation": Conversation, 
                "evaluationForm": EvaluationForm, 
                "evaluator": User, 
                "agent": User, 
                "calibration": Calibration, 
                "status": String, 
                "answers": EvaluationScoringSet, 
                "agentHasRead": Boolean, 
                "releaseDate": Date, 
                "assignedDate": Date, 
                "changedDate": Date, 
                "queue": Queue, 
                "neverRelease": Boolean, 
                "resourceId": String, 
                "resourceType": String, 
                "redacted": Boolean, 
                "isScoringIndex": Boolean, 
                "selfUri": String, 
              },  
              "screenRecordingState": String, 
              "flaggedReason": String, 
            },  
            "conversationIds": [String], 
            "maxParticipants": Number, 
            "recordingState": String, 
            "state": String, 
            "selfUri": String, 
          },  
          "evaluationForm": { 
            "id": String, 
            "name": String, 
            "modifiedDate": Date, 
            "published": Boolean, 
            "contextId": String, 
            "questionGroups": { 
              "id": String, 
              "name": String, 
              "type": String, 
              "defaultAnswersToHighest": Boolean, 
              "defaultAnswersToNA": Boolean, 
              "naEnabled": Boolean, 
              "weight": Number, 
              "manualWeight": Boolean, 
              "questions": { 
                "id": String, 
                "text": String, 
                "helpText": String, 
                "type": String, 
                "naEnabled": Boolean, 
                "commentsRequired": Boolean, 
                "visibilityCondition": VisibilityCondition, 
                "answerOptions": [AnswerOption], 
                "maxResponseCharacters": Number, 
                "explanationPrompt": String, 
                "isKill": Boolean, 
                "isCritical": Boolean, 
              },  
              "visibilityCondition": { 
                "combiningOperation": String, 
                "predicates": [Object], 
              },  
            },  
            "publishedVersions": { 
              "entities": { 
                "id": String, 
                "name": String, 
                "modifiedDate": Date, 
                "published": Boolean, 
                "contextId": String, 
                "questionGroups": [QuestionGroup], 
                "publishedVersions": DomainEntityListingEvaluationForm, 
                "selfUri": String, 
              },  
              "pageSize": Number, 
              "pageNumber": Number, 
              "total": Number, 
              "selfUri": String, 
              "firstUri": String, 
              "previousUri": String, 
              "nextUri": String, 
              "lastUri": String, 
              "pageCount": Number, 
            },  
            "selfUri": String, 
          },  
          "contextId": String, 
          "averageScore": Number, 
          "highScore": Number, 
          "lowScore": Number, 
          "createdDate": Date, 
          "evaluations": { 
            "id": String, 
            "name": String, 
            "conversation": { 
              "id": String, 
              "name": String, 
              "startTime": Date, 
              "endTime": Date, 
              "address": String, 
              "participants": { 
                "id": String, 
                "startTime": Date, 
                "endTime": Date, 
                "connectedTime": Date, 
                "name": String, 
                "userUri": String, 
                "userId": String, 
                "externalContactId": String, 
                "externalOrganizationId": String, 
                "queueId": String, 
                "groupId": String, 
                "queueName": String, 
                "purpose": String, 
                "participantType": String, 
                "consultParticipantId": String, 
                "address": String, 
                "ani": String, 
                "aniName": String, 
                "dnis": String, 
                "locale": String, 
                "wrapupRequired": Boolean, 
                "wrapupPrompt": String, 
                "wrapupTimeoutMs": Number, 
                "wrapupSkipped": Boolean, 
                "wrapup": Wrapup, 
                "monitoredParticipantId": String, 
                "attributes": {String: String}, 
                "calls": [Call], 
                "callbacks": [Callback], 
                "chats": [ConversationChat], 
                "cobrowsesessions": [Cobrowsesession], 
                "emails": [Email], 
                "messages": [Message], 
                "screenshares": [Screenshare], 
                "socialExpressions": [SocialExpression], 
                "videos": [Video], 
                "evaluations": [Evaluation], 
                "screenRecordingState": String, 
                "flaggedReason": String, 
              },  
              "conversationIds": [String], 
              "maxParticipants": Number, 
              "recordingState": String, 
              "state": String, 
              "selfUri": String, 
            },  
            "evaluationForm": { 
              "id": String, 
              "name": String, 
              "modifiedDate": Date, 
              "published": Boolean, 
              "contextId": String, 
              "questionGroups": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "defaultAnswersToHighest": Boolean, 
                "defaultAnswersToNA": Boolean, 
                "naEnabled": Boolean, 
                "weight": Number, 
                "manualWeight": Boolean, 
                "questions": [Question], 
                "visibilityCondition": VisibilityCondition, 
              },  
              "publishedVersions": { 
                "entities": [EvaluationForm], 
                "pageSize": Number, 
                "pageNumber": Number, 
                "total": Number, 
                "selfUri": String, 
                "firstUri": String, 
                "previousUri": String, 
                "nextUri": String, 
                "lastUri": String, 
                "pageCount": Number, 
              },  
              "selfUri": String, 
            },  
            "evaluator": { 
              "id": String, 
              "name": String, 
              "chat": { 
                "jabberId": String, 
              },  
              "department": String, 
              "email": String, 
              "primaryContactInfo": { 
                "address": String, 
                "display": String, 
                "mediaType": String, 
                "type": String, 
                "extension": String, 
              },  
              "addresses": { 
                "address": String, 
                "display": String, 
                "mediaType": String, 
                "type": String, 
                "extension": String, 
              },  
              "state": String, 
              "title": String, 
              "username": String, 
              "manager": User, 
              "images": { 
                "resolution": String, 
                "imageUri": String, 
              },  
              "version": Number, 
              "routingStatus": { 
                "userId": String, 
                "status": String, 
                "startTime": Date, 
              },  
              "presence": { 
                "id": String, 
                "name": String, 
                "source": String, 
                "primary": Boolean, 
                "presenceDefinition": PresenceDefinition, 
                "message": String, 
                "modifiedDate": Date, 
                "selfUri": String, 
              },  
              "conversationSummary": { 
                "userId": String, 
                "call": MediaSummary, 
                "callback": MediaSummary, 
                "email": MediaSummary, 
                "message": MediaSummary, 
                "chat": MediaSummary, 
                "socialExpression": MediaSummary, 
                "video": MediaSummary, 
              },  
              "outOfOffice": { 
                "id": String, 
                "name": String, 
                "user": User, 
                "startDate": Date, 
                "endDate": Date, 
                "active": Boolean, 
                "indefinite": Boolean, 
                "selfUri": String, 
              },  
              "geolocation": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "primary": Boolean, 
                "latitude": Number, 
                "longitude": Number, 
                "country": String, 
                "region": String, 
                "city": String, 
                "locations": [LocationDefinition], 
                "selfUri": String, 
              },  
              "station": { 
                "associatedStation": UserStation, 
                "effectiveStation": UserStation, 
                "defaultStation": UserStation, 
                "lastAssociatedStation": UserStation, 
              },  
              "authorization": { 
                "roles": [DomainRole], 
                "permissions": [String], 
                "permissionPolicies": [ResourcePermissionPolicy], 
              },  
              "profileSkills": [String], 
              "locations": { 
                "id": String, 
                "floorplanId": String, 
                "coordinates": {String: Number}, 
                "notes": String, 
                "locationDefinition": LocationDefinition, 
              },  
              "groups": { 
                "id": String, 
                "name": String, 
                "description": String, 
                "dateModified": Date, 
                "memberCount": Number, 
                "state": String, 
                "version": Number, 
                "type": String, 
                "images": [UserImage], 
                "addresses": [GroupContact], 
                "rulesVisible": Boolean, 
                "visibility": String, 
                "owners": [User], 
                "selfUri": String, 
              },  
              "acdAutoAnswer": Boolean, 
              "selfUri": String, 
            },  
            "agent": { 
              "id": String, 
              "name": String, 
              "chat": { 
                "jabberId": String, 
              },  
              "department": String, 
              "email": String, 
              "primaryContactInfo": { 
                "address": String, 
                "display": String, 
                "mediaType": String, 
                "type": String, 
                "extension": String, 
              },  
              "addresses": { 
                "address": String, 
                "display": String, 
                "mediaType": String, 
                "type": String, 
                "extension": String, 
              },  
              "state": String, 
              "title": String, 
              "username": String, 
              "manager": User, 
              "images": { 
                "resolution": String, 
                "imageUri": String, 
              },  
              "version": Number, 
              "routingStatus": { 
                "userId": String, 
                "status": String, 
                "startTime": Date, 
              },  
              "presence": { 
                "id": String, 
                "name": String, 
                "source": String, 
                "primary": Boolean, 
                "presenceDefinition": PresenceDefinition, 
                "message": String, 
                "modifiedDate": Date, 
                "selfUri": String, 
              },  
              "conversationSummary": { 
                "userId": String, 
                "call": MediaSummary, 
                "callback": MediaSummary, 
                "email": MediaSummary, 
                "message": MediaSummary, 
                "chat": MediaSummary, 
                "socialExpression": MediaSummary, 
                "video": MediaSummary, 
              },  
              "outOfOffice": { 
                "id": String, 
                "name": String, 
                "user": User, 
                "startDate": Date, 
                "endDate": Date, 
                "active": Boolean, 
                "indefinite": Boolean, 
                "selfUri": String, 
              },  
              "geolocation": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "primary": Boolean, 
                "latitude": Number, 
                "longitude": Number, 
                "country": String, 
                "region": String, 
                "city": String, 
                "locations": [LocationDefinition], 
                "selfUri": String, 
              },  
              "station": { 
                "associatedStation": UserStation, 
                "effectiveStation": UserStation, 
                "defaultStation": UserStation, 
                "lastAssociatedStation": UserStation, 
              },  
              "authorization": { 
                "roles": [DomainRole], 
                "permissions": [String], 
                "permissionPolicies": [ResourcePermissionPolicy], 
              },  
              "profileSkills": [String], 
              "locations": { 
                "id": String, 
                "floorplanId": String, 
                "coordinates": {String: Number}, 
                "notes": String, 
                "locationDefinition": LocationDefinition, 
              },  
              "groups": { 
                "id": String, 
                "name": String, 
                "description": String, 
                "dateModified": Date, 
                "memberCount": Number, 
                "state": String, 
                "version": Number, 
                "type": String, 
                "images": [UserImage], 
                "addresses": [GroupContact], 
                "rulesVisible": Boolean, 
                "visibility": String, 
                "owners": [User], 
                "selfUri": String, 
              },  
              "acdAutoAnswer": Boolean, 
              "selfUri": String, 
            },  
            "calibration": { 
              "id": String, 
              "name": String, 
              "calibrator": { 
                "id": String, 
                "name": String, 
                "chat": Chat, 
                "department": String, 
                "email": String, 
                "primaryContactInfo": [Contact], 
                "addresses": [Contact], 
                "state": String, 
                "title": String, 
                "username": String, 
                "manager": User, 
                "images": [UserImage], 
                "version": Number, 
                "routingStatus": RoutingStatus, 
                "presence": UserPresence, 
                "conversationSummary": UserConversationSummary, 
                "outOfOffice": OutOfOffice, 
                "geolocation": Geolocation, 
                "station": UserStations, 
                "authorization": UserAuthorization, 
                "profileSkills": [String], 
                "locations": [Location], 
                "groups": [Group], 
                "acdAutoAnswer": Boolean, 
                "selfUri": String, 
              },  
              "agent": User, 
              "conversation": { 
                "id": String, 
                "name": String, 
                "startTime": Date, 
                "endTime": Date, 
                "address": String, 
                "participants": [Participant], 
                "conversationIds": [String], 
                "maxParticipants": Number, 
                "recordingState": String, 
                "state": String, 
                "selfUri": String, 
              },  
              "evaluationForm": { 
                "id": String, 
                "name": String, 
                "modifiedDate": Date, 
                "published": Boolean, 
                "contextId": String, 
                "questionGroups": [QuestionGroup], 
                "publishedVersions": DomainEntityListingEvaluationForm, 
                "selfUri": String, 
              },  
              "contextId": String, 
              "averageScore": Number, 
              "highScore": Number, 
              "lowScore": Number, 
              "createdDate": Date, 
              "evaluations": { 
                "id": String, 
                "name": String, 
                "conversation": Conversation, 
                "evaluationForm": EvaluationForm, 
                "evaluator": User, 
                "agent": User, 
                "calibration": Calibration, 
                "status": String, 
                "answers": EvaluationScoringSet, 
                "agentHasRead": Boolean, 
                "releaseDate": Date, 
                "assignedDate": Date, 
                "changedDate": Date, 
                "queue": Queue, 
                "neverRelease": Boolean, 
                "resourceId": String, 
                "resourceType": String, 
                "redacted": Boolean, 
                "isScoringIndex": Boolean, 
                "selfUri": String, 
              },  
              "evaluators": User, 
              "scoringIndex": { 
                "id": String, 
                "name": String, 
                "conversation": Conversation, 
                "evaluationForm": EvaluationForm, 
                "evaluator": User, 
                "agent": User, 
                "calibration": Calibration, 
                "status": String, 
                "answers": EvaluationScoringSet, 
                "agentHasRead": Boolean, 
                "releaseDate": Date, 
                "assignedDate": Date, 
                "changedDate": Date, 
                "queue": Queue, 
                "neverRelease": Boolean, 
                "resourceId": String, 
                "resourceType": String, 
                "redacted": Boolean, 
                "isScoringIndex": Boolean, 
                "selfUri": String, 
              },  
              "expertEvaluator": User, 
              "selfUri": String, 
            },  
            "status": String, 
            "answers": { 
              "totalScore": Number, 
              "totalCriticalScore": Number, 
              "questionGroupScores": { 
                "questionGroupId": String, 
                "totalScore": Number, 
                "maxTotalScore": Number, 
                "totalCriticalScore": Number, 
                "maxTotalCriticalScore": Number, 
                "totalScoreUnweighted": Number, 
                "maxTotalScoreUnweighted": Number, 
                "totalCriticalScoreUnweighted": Number, 
                "maxTotalCriticalScoreUnweighted": Number, 
                "markedNA": Boolean, 
                "questionScores": [QuestionScore], 
              },  
              "anyFailedKillQuestions": Boolean, 
              "comments": String, 
              "agentComments": String, 
            },  
            "agentHasRead": Boolean, 
            "releaseDate": Date, 
            "assignedDate": Date, 
            "changedDate": Date, 
            "queue": { 
              "id": String, 
              "name": String, 
              "division": { 
                "id": String, 
                "name": String, 
                "selfUri": String, 
              },  
              "description": String, 
              "version": Number, 
              "dateCreated": Date, 
              "dateModified": Date, 
              "modifiedBy": String, 
              "createdBy": String, 
              "state": String, 
              "modifiedByApp": String, 
              "createdByApp": String, 
              "mediaSettings": { 
                "alertingTimeoutSeconds": Number, 
                "serviceLevel": ServiceLevel, 
              },  
              "bullseye": { 
                "rings": [Ring], 
              },  
              "acwSettings": { 
                "wrapupPrompt": String, 
                "timeoutMs": Number, 
              },  
              "skillEvaluationMethod": String, 
              "queueFlow": { 
                "id": String, 
                "name": String, 
                "selfUri": String, 
              },  
              "whisperPrompt": { 
                "id": String, 
                "name": String, 
                "selfUri": String, 
              },  
              "autoAnswerOnly": Boolean, 
              "callingPartyName": String, 
              "callingPartyNumber": String, 
              "defaultScripts": { 
                "id": String, 
                "name": String, 
                "versionId": String, 
                "createdDate": Date, 
                "modifiedDate": Date, 
                "publishedDate": Date, 
                "versionDate": Date, 
                "startPageId": String, 
                "startPageName": String, 
                "features": Object, 
                "variables": Object, 
                "customActions": Object, 
                "pages": [Page], 
                "selfUri": String, 
              },  
              "outboundEmailAddress": { 
                "domain": UriReference, 
                "route": InboundRoute, 
              },  
              "memberCount": Number, 
              "selfUri": String, 
            },  
            "neverRelease": Boolean, 
            "resourceId": String, 
            "resourceType": String, 
            "redacted": Boolean, 
            "isScoringIndex": Boolean, 
            "selfUri": String, 
          },  
          "evaluators": User, 
          "scoringIndex": { 
            "id": String, 
            "name": String, 
            "conversation": { 
              "id": String, 
              "name": String, 
              "startTime": Date, 
              "endTime": Date, 
              "address": String, 
              "participants": { 
                "id": String, 
                "startTime": Date, 
                "endTime": Date, 
                "connectedTime": Date, 
                "name": String, 
                "userUri": String, 
                "userId": String, 
                "externalContactId": String, 
                "externalOrganizationId": String, 
                "queueId": String, 
                "groupId": String, 
                "queueName": String, 
                "purpose": String, 
                "participantType": String, 
                "consultParticipantId": String, 
                "address": String, 
                "ani": String, 
                "aniName": String, 
                "dnis": String, 
                "locale": String, 
                "wrapupRequired": Boolean, 
                "wrapupPrompt": String, 
                "wrapupTimeoutMs": Number, 
                "wrapupSkipped": Boolean, 
                "wrapup": Wrapup, 
                "monitoredParticipantId": String, 
                "attributes": {String: String}, 
                "calls": [Call], 
                "callbacks": [Callback], 
                "chats": [ConversationChat], 
                "cobrowsesessions": [Cobrowsesession], 
                "emails": [Email], 
                "messages": [Message], 
                "screenshares": [Screenshare], 
                "socialExpressions": [SocialExpression], 
                "videos": [Video], 
                "evaluations": [Evaluation], 
                "screenRecordingState": String, 
                "flaggedReason": String, 
              },  
              "conversationIds": [String], 
              "maxParticipants": Number, 
              "recordingState": String, 
              "state": String, 
              "selfUri": String, 
            },  
            "evaluationForm": { 
              "id": String, 
              "name": String, 
              "modifiedDate": Date, 
              "published": Boolean, 
              "contextId": String, 
              "questionGroups": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "defaultAnswersToHighest": Boolean, 
                "defaultAnswersToNA": Boolean, 
                "naEnabled": Boolean, 
                "weight": Number, 
                "manualWeight": Boolean, 
                "questions": [Question], 
                "visibilityCondition": VisibilityCondition, 
              },  
              "publishedVersions": { 
                "entities": [EvaluationForm], 
                "pageSize": Number, 
                "pageNumber": Number, 
                "total": Number, 
                "selfUri": String, 
                "firstUri": String, 
                "previousUri": String, 
                "nextUri": String, 
                "lastUri": String, 
                "pageCount": Number, 
              },  
              "selfUri": String, 
            },  
            "evaluator": { 
              "id": String, 
              "name": String, 
              "chat": { 
                "jabberId": String, 
              },  
              "department": String, 
              "email": String, 
              "primaryContactInfo": { 
                "address": String, 
                "display": String, 
                "mediaType": String, 
                "type": String, 
                "extension": String, 
              },  
              "addresses": { 
                "address": String, 
                "display": String, 
                "mediaType": String, 
                "type": String, 
                "extension": String, 
              },  
              "state": String, 
              "title": String, 
              "username": String, 
              "manager": User, 
              "images": { 
                "resolution": String, 
                "imageUri": String, 
              },  
              "version": Number, 
              "routingStatus": { 
                "userId": String, 
                "status": String, 
                "startTime": Date, 
              },  
              "presence": { 
                "id": String, 
                "name": String, 
                "source": String, 
                "primary": Boolean, 
                "presenceDefinition": PresenceDefinition, 
                "message": String, 
                "modifiedDate": Date, 
                "selfUri": String, 
              },  
              "conversationSummary": { 
                "userId": String, 
                "call": MediaSummary, 
                "callback": MediaSummary, 
                "email": MediaSummary, 
                "message": MediaSummary, 
                "chat": MediaSummary, 
                "socialExpression": MediaSummary, 
                "video": MediaSummary, 
              },  
              "outOfOffice": { 
                "id": String, 
                "name": String, 
                "user": User, 
                "startDate": Date, 
                "endDate": Date, 
                "active": Boolean, 
                "indefinite": Boolean, 
                "selfUri": String, 
              },  
              "geolocation": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "primary": Boolean, 
                "latitude": Number, 
                "longitude": Number, 
                "country": String, 
                "region": String, 
                "city": String, 
                "locations": [LocationDefinition], 
                "selfUri": String, 
              },  
              "station": { 
                "associatedStation": UserStation, 
                "effectiveStation": UserStation, 
                "defaultStation": UserStation, 
                "lastAssociatedStation": UserStation, 
              },  
              "authorization": { 
                "roles": [DomainRole], 
                "permissions": [String], 
                "permissionPolicies": [ResourcePermissionPolicy], 
              },  
              "profileSkills": [String], 
              "locations": { 
                "id": String, 
                "floorplanId": String, 
                "coordinates": {String: Number}, 
                "notes": String, 
                "locationDefinition": LocationDefinition, 
              },  
              "groups": { 
                "id": String, 
                "name": String, 
                "description": String, 
                "dateModified": Date, 
                "memberCount": Number, 
                "state": String, 
                "version": Number, 
                "type": String, 
                "images": [UserImage], 
                "addresses": [GroupContact], 
                "rulesVisible": Boolean, 
                "visibility": String, 
                "owners": [User], 
                "selfUri": String, 
              },  
              "acdAutoAnswer": Boolean, 
              "selfUri": String, 
            },  
            "agent": { 
              "id": String, 
              "name": String, 
              "chat": { 
                "jabberId": String, 
              },  
              "department": String, 
              "email": String, 
              "primaryContactInfo": { 
                "address": String, 
                "display": String, 
                "mediaType": String, 
                "type": String, 
                "extension": String, 
              },  
              "addresses": { 
                "address": String, 
                "display": String, 
                "mediaType": String, 
                "type": String, 
                "extension": String, 
              },  
              "state": String, 
              "title": String, 
              "username": String, 
              "manager": User, 
              "images": { 
                "resolution": String, 
                "imageUri": String, 
              },  
              "version": Number, 
              "routingStatus": { 
                "userId": String, 
                "status": String, 
                "startTime": Date, 
              },  
              "presence": { 
                "id": String, 
                "name": String, 
                "source": String, 
                "primary": Boolean, 
                "presenceDefinition": PresenceDefinition, 
                "message": String, 
                "modifiedDate": Date, 
                "selfUri": String, 
              },  
              "conversationSummary": { 
                "userId": String, 
                "call": MediaSummary, 
                "callback": MediaSummary, 
                "email": MediaSummary, 
                "message": MediaSummary, 
                "chat": MediaSummary, 
                "socialExpression": MediaSummary, 
                "video": MediaSummary, 
              },  
              "outOfOffice": { 
                "id": String, 
                "name": String, 
                "user": User, 
                "startDate": Date, 
                "endDate": Date, 
                "active": Boolean, 
                "indefinite": Boolean, 
                "selfUri": String, 
              },  
              "geolocation": { 
                "id": String, 
                "name": String, 
                "type": String, 
                "primary": Boolean, 
                "latitude": Number, 
                "longitude": Number, 
                "country": String, 
                "region": String, 
                "city": String, 
                "locations": [LocationDefinition], 
                "selfUri": String, 
              },  
              "station": { 
                "associatedStation": UserStation, 
                "effectiveStation": UserStation, 
                "defaultStation": UserStation, 
                "lastAssociatedStation": UserStation, 
              },  
              "authorization": { 
                "roles": [DomainRole], 
                "permissions": [String], 
                "permissionPolicies": [ResourcePermissionPolicy], 
              },  
              "profileSkills": [String], 
              "locations": { 
                "id": String, 
                "floorplanId": String, 
                "coordinates": {String: Number}, 
                "notes": String, 
                "locationDefinition": LocationDefinition, 
              },  
              "groups": { 
                "id": String, 
                "name": String, 
                "description": String, 
                "dateModified": Date, 
                "memberCount": Number, 
                "state": String, 
                "version": Number, 
                "type": String, 
                "images": [UserImage], 
                "addresses": [GroupContact], 
                "rulesVisible": Boolean, 
                "visibility": String, 
                "owners": [User], 
                "selfUri": String, 
              },  
              "acdAutoAnswer": Boolean, 
              "selfUri": String, 
            },  
            "calibration": { 
              "id": String, 
              "name": String, 
              "calibrator": { 
                "id": String, 
                "name": String, 
                "chat": Chat, 
                "department": String, 
                "email": String, 
                "primaryContactInfo": [Contact], 
                "addresses": [Contact], 
                "state": String, 
                "title": String, 
                "username": String, 
                "manager": User, 
                "images": [UserImage], 
                "version": Number, 
                "routingStatus": RoutingStatus, 
                "presence": UserPresence, 
                "conversationSummary": UserConversationSummary, 
                "outOfOffice": OutOfOffice, 
                "geolocation": Geolocation, 
                "station": UserStations, 
                "authorization": UserAuthorization, 
                "profileSkills": [String], 
                "locations": [Location], 
                "groups": [Group], 
                "acdAutoAnswer": Boolean, 
                "selfUri": String, 
              },  
              "agent": User, 
              "conversation": { 
                "id": String, 
                "name": String, 
                "startTime": Date, 
                "endTime": Date, 
                "address": String, 
                "participants": [Participant], 
                "conversationIds": [String], 
                "maxParticipants": Number, 
                "recordingState": String, 
                "state": String, 
                "selfUri": String, 
              },  
              "evaluationForm": { 
                "id": String, 
                "name": String, 
                "modifiedDate": Date, 
                "published": Boolean, 
                "contextId": String, 
                "questionGroups": [QuestionGroup], 
                "publishedVersions": DomainEntityListingEvaluationForm, 
                "selfUri": String, 
              },  
              "contextId": String, 
              "averageScore": Number, 
              "highScore": Number, 
              "lowScore": Number, 
              "createdDate": Date, 
              "evaluations": { 
                "id": String, 
                "name": String, 
                "conversation": Conversation, 
                "evaluationForm": EvaluationForm, 
                "evaluator": User, 
                "agent": User, 
                "calibration": Calibration, 
                "status": String, 
                "answers": EvaluationScoringSet, 
                "agentHasRead": Boolean, 
                "releaseDate": Date, 
                "assignedDate": Date, 
                "changedDate": Date, 
                "queue": Queue, 
                "neverRelease": Boolean, 
                "resourceId": String, 
                "resourceType": String, 
                "redacted": Boolean, 
                "isScoringIndex": Boolean, 
                "selfUri": String, 
              },  
              "evaluators": User, 
              "scoringIndex": { 
                "id": String, 
                "name": String, 
                "conversation": Conversation, 
                "evaluationForm": EvaluationForm, 
                "evaluator": User, 
                "agent": User, 
                "calibration": Calibration, 
                "status": String, 
                "answers": EvaluationScoringSet, 
                "agentHasRead": Boolean, 
                "releaseDate": Date, 
                "assignedDate": Date, 
                "changedDate": Date, 
                "queue": Queue, 
                "neverRelease": Boolean, 
                "resourceId": String, 
                "resourceType": String, 
                "redacted": Boolean, 
                "isScoringIndex": Boolean, 
                "selfUri": String, 
              },  
              "expertEvaluator": User, 
              "selfUri": String, 
            },  
            "status": String, 
            "answers": { 
              "totalScore": Number, 
              "totalCriticalScore": Number, 
              "questionGroupScores": { 
                "questionGroupId": String, 
                "totalScore": Number, 
                "maxTotalScore": Number, 
                "totalCriticalScore": Number, 
                "maxTotalCriticalScore": Number, 
                "totalScoreUnweighted": Number, 
                "maxTotalScoreUnweighted": Number, 
                "totalCriticalScoreUnweighted": Number, 
                "maxTotalCriticalScoreUnweighted": Number, 
                "markedNA": Boolean, 
                "questionScores": [QuestionScore], 
              },  
              "anyFailedKillQuestions": Boolean, 
              "comments": String, 
              "agentComments": String, 
            },  
            "agentHasRead": Boolean, 
            "releaseDate": Date, 
            "assignedDate": Date, 
            "changedDate": Date, 
            "queue": { 
              "id": String, 
              "name": String, 
              "division": { 
                "id": String, 
                "name": String, 
                "selfUri": String, 
              },  
              "description": String, 
              "version": Number, 
              "dateCreated": Date, 
              "dateModified": Date, 
              "modifiedBy": String, 
              "createdBy": String, 
              "state": String, 
              "modifiedByApp": String, 
              "createdByApp": String, 
              "mediaSettings": { 
                "alertingTimeoutSeconds": Number, 
                "serviceLevel": ServiceLevel, 
              },  
              "bullseye": { 
                "rings": [Ring], 
              },  
              "acwSettings": { 
                "wrapupPrompt": String, 
                "timeoutMs": Number, 
              },  
              "skillEvaluationMethod": String, 
              "queueFlow": { 
                "id": String, 
                "name": String, 
                "selfUri": String, 
              },  
              "whisperPrompt": { 
                "id": String, 
                "name": String, 
                "selfUri": String, 
              },  
              "autoAnswerOnly": Boolean, 
              "callingPartyName": String, 
              "callingPartyNumber": String, 
              "defaultScripts": { 
                "id": String, 
                "name": String, 
                "versionId": String, 
                "createdDate": Date, 
                "modifiedDate": Date, 
                "publishedDate": Date, 
                "versionDate": Date, 
                "startPageId": String, 
                "startPageName": String, 
                "features": Object, 
                "variables": Object, 
                "customActions": Object, 
                "pages": [Page], 
                "selfUri": String, 
              },  
              "outboundEmailAddress": { 
                "domain": UriReference, 
                "route": InboundRoute, 
              },  
              "memberCount": Number, 
              "selfUri": String, 
            },  
            "neverRelease": Boolean, 
            "resourceId": String, 
            "resourceType": String, 
            "redacted": Boolean, 
            "isScoringIndex": Boolean, 
            "selfUri": String, 
          },  
          "expertEvaluator": User, 
          "selfUri": String, 
        },  
        "status": String, 
        "answers": { 
          "totalScore": Number, 
          "totalCriticalScore": Number, 
          "questionGroupScores": { 
            "questionGroupId": String, 
            "totalScore": Number, 
            "maxTotalScore": Number, 
            "totalCriticalScore": Number, 
            "maxTotalCriticalScore": Number, 
            "totalScoreUnweighted": Number, 
            "maxTotalScoreUnweighted": Number, 
            "totalCriticalScoreUnweighted": Number, 
            "maxTotalCriticalScoreUnweighted": Number, 
            "markedNA": Boolean, 
            "questionScores": { 
              "questionId": String, 
              "answerId": String, 
              "score": Number, 
              "markedNA": Boolean, 
              "failedKillQuestion": Boolean, 
              "comments": String, 
            },  
          },  
          "anyFailedKillQuestions": Boolean, 
          "comments": String, 
          "agentComments": String, 
        },  
        "agentHasRead": Boolean, 
        "releaseDate": Date, 
        "assignedDate": Date, 
        "changedDate": Date, 
        "queue": { 
          "id": String, 
          "name": String, 
          "division": { 
            "id": String, 
            "name": String, 
            "selfUri": String, 
          },  
          "description": String, 
          "version": Number, 
          "dateCreated": Date, 
          "dateModified": Date, 
          "modifiedBy": String, 
          "createdBy": String, 
          "state": String, 
          "modifiedByApp": String, 
          "createdByApp": String, 
          "mediaSettings": { 
            "alertingTimeoutSeconds": Number, 
            "serviceLevel": { 
              "percentage": Number, 
              "durationMs": Number, 
            },  
          },  
          "bullseye": { 
            "rings": { 
              "expansionCriteria": { 
                "type": String, 
                "threshold": Number, 
              },  
              "actions": { 
                "skillsToRemove": [SkillsToRemove], 
              },  
            },  
          },  
          "acwSettings": { 
            "wrapupPrompt": String, 
            "timeoutMs": Number, 
          },  
          "skillEvaluationMethod": String, 
          "queueFlow": { 
            "id": String, 
            "name": String, 
            "selfUri": String, 
          },  
          "whisperPrompt": { 
            "id": String, 
            "name": String, 
            "selfUri": String, 
          },  
          "autoAnswerOnly": Boolean, 
          "callingPartyName": String, 
          "callingPartyNumber": String, 
          "defaultScripts": { 
            "id": String, 
            "name": String, 
            "versionId": String, 
            "createdDate": Date, 
            "modifiedDate": Date, 
            "publishedDate": Date, 
            "versionDate": Date, 
            "startPageId": String, 
            "startPageName": String, 
            "features": Object, 
            "variables": Object, 
            "customActions": Object, 
            "pages": { 
              "id": String, 
              "name": String, 
              "versionId": String, 
              "createdDate": Date, 
              "modifiedDate": Date, 
              "rootContainer": {String: Object}, 
              "properties": {String: Object}, 
              "selfUri": String, 
            },  
            "selfUri": String, 
          },  
          "outboundEmailAddress": { 
            "domain": { 
              "id": String, 
              "name": String, 
              "selfUri": String, 
            },  
            "route": { 
              "id": String, 
              "name": String, 
              "pattern": String, 
              "queue": { 
                "id": String, 
                "name": String, 
                "selfUri": String, 
              },  
              "priority": Number, 
              "skills": { 
                "id": String, 
                "name": String, 
                "selfUri": String, 
              },  
              "language": { 
                "id": String, 
                "name": String, 
                "selfUri": String, 
              },  
              "fromName": String, 
              "fromEmail": String, 
              "flow": { 
                "id": String, 
                "name": String, 
                "selfUri": String, 
              },  
              "replyEmailAddress": { 
                "domain": UriReference, 
                "route": InboundRoute, 
              },  
              "selfUri": String, 
            },  
          },  
          "memberCount": Number, 
          "selfUri": String, 
        },  
        "neverRelease": Boolean, 
        "resourceId": String, 
        "resourceType": String, 
        "redacted": Boolean, 
        "isScoringIndex": Boolean, 
        "selfUri": String, 
      },  
      "screenRecordingState": String, 
      "flaggedReason": String, 
    },  
    "conversationIds": [String], 
    "maxParticipants": Number, 
    "recordingState": String, 
    "state": String, 
    "selfUri": String, 
  },  
  "contentLength": Number, 
  "durationMilliseconds": Number, 
  "thumbnails": { 
    "resolution": String, 
    "imageUri": String, 
    "height": Number, 
    "width": Number, 
  },  
  "read": Boolean, 
  "selfUri": String, 
}
~~~
</div>


### Example Usage

~~~ javascript
// Browser
const platformClient = require('platformClient');
// Node
const platformClient = require('purecloud-platform-client-v2');

// Configure OAuth2 access token for authorization: PureCloud Auth
platformClient.ApiClient.instance.authentications['PureCloud Auth'].accessToken = 'YOUR ACCESS TOKEN';

var apiInstance = new platformClient.UserRecordingsApi();

var recordingId = "recordingId_example"; // String | User Recording ID

var body = {}; // Object | UserRecording

var opts = { 
  'expand': ["expand_example"] // [String] | Which fields, if any, to expand.
};
apiInstance.putUserrecording(recordingId, body, opts)
  .then(function(data) {
    console.log(`putUserrecording success! data: ${JSON.stringify(data, null, 2)}`);
  })
  .catch(function(err) {
  	console.log('There was a failure calling putUserrecording');
    console.error(err);
  });

~~~

### Parameters


| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
 **recordingId** | **String** | User Recording ID |  |
 **body** | **Object** | UserRecording |  |
 **expand** | **[String]** | Which fields, if any, to expand. | [optional] <br />**Values**: conversation |
{: class="table table-striped"}

### Return type

**UserRecording**

