# ![LOGO](logo.png) Cloud Tasks **flow**ground Connector

## Description

A generated **flow**ground connector for the Cloud Tasks API (version v2beta3).

Generated from: https://api.apis.guru/v2/specs/googleapis.com/cloudtasks/v2beta3/swagger.json<br/>
Generated at: 2019-05-07T17:41:21+03:00

## API Description

Manages the execution of large numbers of distributed requests.

## Authorization

Supported authorization schemes:
- OAuth2

For OAuth 2.0 you need to specify OAuth Client credentials as environment variables in the connector repository:
* `OAUTH_CLIENT_ID` - your OAuth client id
* `OAUTH_CLIENT_SECRET` - your OAuth client secret

## Actions

### Deletes a task.<br/>
> <br/>
> A task can be deleted if it is scheduled or dispatched. A task<br/>
> cannot be deleted if it has executed successfully or permanently<br/>
> failed.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Required.

The task name. For example:
`projects/PROJECT_ID/locations/LOCATION_ID/queues/QUEUE_ID/tasks/TASK_ID`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets a task.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Required.

The task name. For example:
`projects/PROJECT_ID/locations/LOCATION_ID/queues/QUEUE_ID/tasks/TASK_ID`
* `responseView` - _optional_ - The response_view specifies which subset of the Task will be
returned.

By default response_view is BASIC; not all
information is retrieved by default because some data, such as
payloads, might be desirable to return only when needed because
of its large size or because of the sensitivity of data that it
contains.

Authorization for FULL requires
`cloudtasks.tasks.fullView` [Google IAM](https://cloud.google.com/iam/)
permission on the Task resource.
    Possible values: VIEW_UNSPECIFIED, BASIC, FULL.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Updates a queue.<br/>
> <br/>
> This method creates the queue if it does not exist and updates<br/>
> the queue if it does exist.<br/>
> <br/>
> Queues created with this method allow tasks to live for a maximum of 31<br/>
> days. After a task is 31 days old, the task will be deleted regardless of whether<br/>
> it was dispatched or not.<br/>
> <br/>
> WARNING: Using this method may have unintended side effects if you are<br/>
> using an App Engine `queue.yaml` or `queue.xml` file to manage your queues.<br/>
> Read<br/>
> [Overview of Queue Management and queue.yaml](https://cloud.google.com/tasks/docs/queue-yaml)<br/>
> before using this method.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Caller-specified and required in CreateQueue,
after which it becomes output only.

The queue name.

The queue name must have the following format:
`projects/PROJECT_ID/locations/LOCATION_ID/queues/QUEUE_ID`

* `PROJECT_ID` can contain letters ([A-Za-z]), numbers ([0-9]),
   hyphens (-), colons (:), or periods (.).
   For more information, see
   [Identifying projects](https://cloud.google.com/resource-manager/docs/creating-managing-projects#identifying_projects)
* `LOCATION_ID` is the canonical ID for the queue's location.
   The list of available locations can be obtained by calling
   ListLocations.
   For more information, see https://cloud.google.com/about/locations/.
* `QUEUE_ID` can contain letters ([A-Za-z]), numbers ([0-9]), or
  hyphens (-). The maximum length is 100 characters.
* `updateMask` - _optional_ - A mask used to specify which fields of the queue are being updated.

If empty, then all fields will be updated.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists information about the supported locations for this service.

*Tags:* `projects`

#### Input Parameters
* `filter` - _optional_ - The standard list filter.
* `name` - _required_ - The resource that owns the locations collection, if applicable.
* `pageSize` - _optional_ - The standard list page size.
* `pageToken` - _optional_ - The standard list page token.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Pauses the queue.<br/>
> <br/>
> If a queue is paused then the system will stop dispatching tasks<br/>
> until the queue is resumed via<br/>
> ResumeQueue. Tasks can still be added<br/>
> when the queue is paused. A queue is paused if its<br/>
> state is PAUSED.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Required.

The queue name. For example:
`projects/PROJECT_ID/location/LOCATION_ID/queues/QUEUE_ID`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Purges a queue by deleting all of its tasks.<br/>
> <br/>
> All tasks created before this method is called are permanently deleted.<br/>
> <br/>
> Purge operations can take up to one minute to take effect. Tasks<br/>
> might be dispatched before the purge takes effect. A purge is irreversible.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Required.

The queue name. For example:
`projects/PROJECT_ID/location/LOCATION_ID/queues/QUEUE_ID`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Resume a queue.<br/>
> <br/>
> This method resumes a queue after it has been<br/>
> PAUSED or<br/>
> DISABLED. The state of a queue is stored<br/>
> in the queue's state; after calling this method it<br/>
> will be set to RUNNING.<br/>
> <br/>
> WARNING: Resuming many high-QPS queues at the same time can<br/>
> lead to target overloading. If you are resuming high-QPS<br/>
> queues, follow the 500/50/5 pattern described in<br/>
> [Managing Cloud Tasks Scaling Risks](https://cloud.google.com/tasks/docs/manage-cloud-task-scaling).

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Required.

The queue name. For example:
`projects/PROJECT_ID/location/LOCATION_ID/queues/QUEUE_ID`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Forces a task to run now.<br/>
> <br/>
> When this method is called, Cloud Tasks will dispatch the task, even if<br/>
> the task is already running, the queue has reached its RateLimits or<br/>
> is PAUSED.<br/>
> <br/>
> This command is meant to be used for manual debugging. For<br/>
> example, RunTask can be used to retry a failed<br/>
> task after a fix has been made or to manually force a task to be<br/>
> dispatched now.<br/>
> <br/>
> The dispatched task is returned. That is, the task that is returned<br/>
> contains the status after the task is dispatched but<br/>
> before the task is received by its target.<br/>
> <br/>
> If Cloud Tasks receives a successful response from the task's<br/>
> target, then the task will be deleted; otherwise the task's<br/>
> schedule_time will be reset to the time that<br/>
> RunTask was called plus the retry delay specified<br/>
> in the queue's RetryConfig.<br/>
> <br/>
> RunTask returns<br/>
> NOT_FOUND when it is called on a<br/>
> task that has already succeeded or permanently failed.

*Tags:* `projects`

#### Input Parameters
* `name` - _required_ - Required.

The task name. For example:
`projects/PROJECT_ID/locations/LOCATION_ID/queues/QUEUE_ID/tasks/TASK_ID`
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists queues.<br/>
> <br/>
> Queues are returned in lexicographical order.

*Tags:* `projects`

#### Input Parameters
* `filter` - _optional_ - `filter` can be used to specify a subset of queues. Any Queue
field can be used as a filter and several operators as supported.
For example: `<=, <, >=, >, !=, =, :`. The filter syntax is the same as
described in
[Stackdriver's Advanced Logs Filters](https://cloud.google.com/logging/docs/view/advanced_filters).

Sample filter "state: PAUSED".

Note that using filters might cause fewer queues than the
requested page_size to be returned.
* `pageSize` - _optional_ - Requested page size.

The maximum page size is 9800. If unspecified, the page size will
be the maximum. Fewer queues than requested might be returned,
even if more queues exist; use the
next_page_token in the
response to determine if more queues exist.
* `pageToken` - _optional_ - A token identifying the page of results to return.

To request the first page results, page_token must be empty. To
request the next page of results, page_token must be the value of
next_page_token returned
from the previous call to ListQueues
method. It is an error to switch the value of the
filter while iterating through pages.
* `parent` - _required_ - Required.

The location name.
For example: `projects/PROJECT_ID/locations/LOCATION_ID`
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a queue.<br/>
> <br/>
> Queues created with this method allow tasks to live for a maximum of 31<br/>
> days. After a task is 31 days old, the task will be deleted regardless of whether<br/>
> it was dispatched or not.<br/>
> <br/>
> WARNING: Using this method may have unintended side effects if you are<br/>
> using an App Engine `queue.yaml` or `queue.xml` file to manage your queues.<br/>
> Read<br/>
> [Overview of Queue Management and queue.yaml](https://cloud.google.com/tasks/docs/queue-yaml)<br/>
> before using this method.

*Tags:* `projects`

#### Input Parameters
* `parent` - _required_ - Required.

The location name in which the queue will be created.
For example: `projects/PROJECT_ID/locations/LOCATION_ID`

The list of allowed locations can be obtained by calling Cloud
Tasks' implementation of
ListLocations.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Lists the tasks in a queue.<br/>
> <br/>
> By default, only the BASIC view is retrieved<br/>
> due to performance considerations;<br/>
> response_view controls the<br/>
> subset of information which is returned.<br/>
> <br/>
> The tasks may be returned in any order. The ordering may change at any<br/>
> time.

*Tags:* `projects`

#### Input Parameters
* `pageSize` - _optional_ - Requested page size. Fewer tasks than requested might be returned.

The maximum page size is 1000. If unspecified, the page size will
be the maximum. Fewer tasks than requested might be returned,
even if more tasks exist; use
next_page_token in the
response to determine if more tasks exist.
* `pageToken` - _optional_ - A token identifying the page of results to return.

To request the first page results, page_token must be empty. To
request the next page of results, page_token must be the value of
next_page_token returned
from the previous call to ListTasks
method.

The page token is valid for only 2 hours.
* `parent` - _required_ - Required.

The queue name. For example:
`projects/PROJECT_ID/locations/LOCATION_ID/queues/QUEUE_ID`
* `responseView` - _optional_ - The response_view specifies which subset of the Task will be
returned.

By default response_view is BASIC; not all
information is retrieved by default because some data, such as
payloads, might be desirable to return only when needed because
of its large size or because of the sensitivity of data that it
contains.

Authorization for FULL requires
`cloudtasks.tasks.fullView` [Google IAM](https://cloud.google.com/iam/)
permission on the Task resource.
    Possible values: VIEW_UNSPECIFIED, BASIC, FULL.
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Creates a task and adds it to a queue.<br/>
> <br/>
> Tasks cannot be updated after creation; there is no UpdateTask command.<br/>
> <br/>
> * For App Engine queues, the maximum task size is<br/>
>   100KB.

*Tags:* `projects`

#### Input Parameters
* `parent` - _required_ - Required.

The queue name. For example:
`projects/PROJECT_ID/locations/LOCATION_ID/queues/QUEUE_ID`

The queue must already exist.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Gets the access control policy for a Queue.<br/>
> Returns an empty policy if the resource exists and does not have a policy<br/>
> set.<br/>
> <br/>
> Authorization requires the following<br/>
> [Google IAM](https://cloud.google.com/iam) permission on the specified<br/>
> resource parent:<br/>
> <br/>
> * `cloudtasks.queues.getIamPolicy`

*Tags:* `projects`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy is being requested.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Sets the access control policy for a Queue. Replaces any existing<br/>
> policy.<br/>
> <br/>
> Note: The Cloud Console does not check queue-level IAM permissions yet.<br/>
> Project-level permissions are required to use the Cloud Console.<br/>
> <br/>
> Authorization requires the following<br/>
> [Google IAM](https://cloud.google.com/iam) permission on the specified<br/>
> resource parent:<br/>
> <br/>
> * `cloudtasks.queues.setIamPolicy`

*Tags:* `projects`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy is being specified.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

### Returns permissions that a caller has on a Queue.<br/>
> If the resource does not exist, this will return an empty set of<br/>
> permissions, not a NOT_FOUND error.<br/>
> <br/>
> Note: This operation is designed to be used for building permission-aware<br/>
> UIs and command-line tools, not for authorization checking. This operation<br/>
> may "fail open" without warning.

*Tags:* `projects`

#### Input Parameters
* `resource` - _required_ - REQUIRED: The resource for which the policy detail is being requested.
See the operation documentation for the appropriate value for this field.
* `access_token` - _optional_ - OAuth access token.
* `alt` - _optional_ - Data format for response.
    Possible values: json, media, proto.
* `callback` - _optional_ - JSONP
* `fields` - _optional_ - Selector specifying which fields to include in a partial response.
* `key` - _optional_ - API key. Your API key identifies your project and provides you with API access, quota, and reports. Required unless you provide an OAuth 2.0 token.
* `oauth_token` - _optional_ - OAuth 2.0 token for the current user.
* `prettyPrint` - _optional_ - Returns response with indentations and line breaks.
* `quotaUser` - _optional_ - Available to use for quota purposes for server-side applications. Can be any arbitrary string assigned to a user, but should not exceed 40 characters.
* `uploadType` - _optional_ - Legacy upload protocol for media (e.g. "media", "multipart").
* `upload_protocol` - _optional_ - Upload protocol for media (e.g. "raw", "multipart").

## License

**flow**ground :- Telekom iPaaS / googleapis-com-cloudtasks-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
